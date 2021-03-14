# 币安API实验室🚩



[https://www.binance.com](https://www.binance.com/)

[https://binance-docs.github.io/apidocs/spot/cn/](https://binance-docs.github.io/apidocs/spot/cn/)  
[![](https://github.com/fluidicon.png)sammchardy/python-binance-chain](https://github.com/sammchardy/python-binance-chain/)  
[![](https://github.com/fluidicon.png)binance-exchange/binance-official-api-docs](https://github.com/binance-exchange/binance-official-api-docs)

## [币安多币种自动化策略API操作指南](https://zhuanlan.zhihu.com/p/55109087)

币安虽然成立时间不长，但由于技术出色，API稳定高效，请求频率限制也宽松，上币很多，交易活跃，已经是现货交易的首选平台。币安目前仅以BTC定价的币种就超过了150种，还在不断增加中，这使得获取很多币种行情和K线变的困难。本文将主要介绍如何在FMZ量化平台上操作多币种策略，甚至操作所有币种都没问题，主要面向有一定基础的用户。

## **1.获取行情**

假如要同时操作150个币种，使用REST协议获取行情显然不合适，一遍轮询下来会浪费很多时间，websocket也无法同时订阅如此多的币种。币安意识到多品种策略获取行情的问题，提供了聚合行情接口，但直接使用这个REST接口（/api/v1/ticker/24hr）需要注意，它的权重是40，意思是一次访问相当于普通访问的40次，即使5、6秒访问这个接口一次，也有可能超出限制。

因此我们需要访问这个接口的websocket版，但要注意由于数据量巨大，数据只是固定1s推送一次有行情变化的数据，对于一些几分钟也没交易的冷门币种，可能很长时间也没推送，固定的推送时间对于高频策略也不合适，但对于一般的多币种策略是足够的。具体代码如下：

```cpp
function main() {
    var client = Dial("wss://stream.binance.com:9443/ws/!ticker@arr");
    while (true){
        var data = client.read();
        var msg = JSON.parse(data);
        updateTicker(msg);//updateTicker函数处理行情和交易，接下来介绍
    }
}
```

## **2.交易前的准备**

币安对交易的限制很多，最小交易价值，最小交易量，价格精度，交易量精度。这些都需要提前做好准备。

定义的全局变量：

```cpp
var totalbtc = 0;//总价值，不一定是btc
var baseCoin = ['BTC', 'ETH', 'BNB', 'USDT'][baseCoin_select];//基础货币选择baseCoin_select是下拉框的一个参数
var exceptList = Except_list_string.split(',');//排除的币种，Except_list_string是策略参数
//K线周期选择PERIOD_M1，PERIOD_M5是FMZ默认的全局变量
var period = [PERIOD_M1, PERIOD_M5, PERIOD_M15, PERIOD_M30, PERIOD_H1, PERIOD_H1, PERIOD_D1][period_select]
var periodSecond = [60, 300, 900, 1800, 3600, 3600*24][period_select]//各周期对应的秒数
var lastPeriodTime = 0;//最近周期时间，用于更新K线
var updateProfitTime = 0//最近更新收益时间，用于更新收益
var buyList = []//买单列表
var sellList = []//卖单列表
var accountInfo = {};//用于储存交易相关的数据列表
```

接下来主要是完善accountInfo的内容，所有与交易对相关的内容都储存到其中。

```cpp
if (!_G('accountInfo')){//如果accountInfo没有储存在数据库里，重新获取数据
    var exchangeInfo = JSON.parse(HttpQuery('https://api.binance.com/api/v1/exchangeInfo'));//获取交易相关数据
    var ticker = JSON.parse(HttpQuery('https://api.binance.com/api/v1/ticker/24hr'));//先用rest协议获取一次全量ticekr
    var tradeSymbol = exchangeInfo.symbols.filter(function(x){return x.quoteAsset == baseCoin});//筛选需要的交易对
    accountInfo[baseCoin] = {free:0, frozen:0, last:1, value:0};//基础货币的信息
    for (var i=0; i<tradeSymbol.length; i++){
        var info = tradeSymbol[i];
        if(exceptList.indexOf(info.symbol.slice(0,info.symbol.length-baseCoin.length)) >= 0){
            continue;//过滤掉踢出的币种
        }
        for (var j=0; j<ticker.length; j++){
            var symbol = info.symbol.slice(0,info.symbol.length-baseCoin.length)//币种名称
            if(ticker[j].symbol.slice(ticker[j].symbol.length-baseCoin.length) == baseCoin && ticker[j].symbol == info.symbol){
                //储存的exchangeInfo和ticker的内容，具体不过多解释
                accountInfo[symbol] = {
                    last:parseFloat(ticker[j].lastPrice), free:0, frozen:0, 
                    minQty:parseFloat(info.filters[2].minQty), minNotional:parseFloat(info.filters[3].minNotional)
                    tickerSize:parseFloat(info.filters[0].tickSize), stepSize:parseFloat(info.filters[2].stepSize),
                    ask:parseFloat(ticker[j].askPrice), bid:parseFloat(ticker[j].bidPrice), volume:parseFloat(ticker[j].quoteVolume), 
                    lowPrice:parseFloat(ticker[j].lowPrice), highPrice:parseFloat(ticker[j].highPrice),
                    priceChangePercent:parseFloat(ticker[j].priceChangePercent),
                    sellPrice:0, buyPrice:0, state:0, value:0, records:null
                }
                break;
            }
        }
    }
}else{
    accountInfo = _G('accountInfo');
}
//退出时自动保存accountInfo到数据库
function onexit(){
    _G('accountInfo', accountInfo);
}
```

## **3.更新账户和K线信息**

更新账户信息函数，不用实时更新。

```cpp
function updateAccount(){
    account = exchange.GetAccount();
    if (!account){
        Log('超时');
        return;//这里直接返回是为了节约时间，账户信息获取不及时影响不大
    }
    for (var i=0; i<account.Info.balances.length; i++){
        var symbol = account.Info.balances[i].asset
        //都储存在accountInfo里
        if (symbol in accountInfo){
            accountInfo[symbol].free = parseFloat(account.Info.balances[i].free);
            accountInfo[symbol].frozen = parseFloat(account.Info.balances[i].locked);
            accountInfo[symbol].value = (accountInfo[symbol].free + accountInfo[symbol].frozen)*accountInfo[symbol].last
        }
    }
}
//更新当前账户总值，以所选的基础货币为单位
function updateTotalBTC(){
    var btc = 0;
    for (var symbol in accountInfo){
        btc += accountInfo[symbol].value
    totalbtc = btc;
    }
}
```

更新K线，初次更新可以分次使用GetRecords函数，后期更新使用推送数据合成

```cpp
function initRecords(){    
    for (var symbol in accountInfo){
        if(symbol == baseCoin){continue}
        if(!accountInfo[symbol].records){
            var currency = symbol + '_' + baseCoin;
            //切换交易对
            exchange.IO("currency", currency)
            accountInfo[symbol].records = exchange.GetRecords(period)
            Log('更新', currency, 'K线', accountInfo[symbol].records[accountInfo[symbol].records.length-1])
            Sleep(250)//每秒更新四个，不会达到限制
        }
        //最近K线时间
        lastPeriodTime = Math.max(accountInfo[symbol].records[accountInfo[symbol].records.length-1].Time/1000, lastPeriodTime)
    }
}
//根据推送ticker数据更新K线
function updateRecords(msgTime){
    //如果当前时间大于最后更新的一个周期，说明需要产生新的K线
    if(parseFloat(msgTime)/1000 - lastPeriodTime > periodSecond){
        for (var symbol in accountInfo){
            if(symbol != baseCoin){
                //如果某交易对的K线差太多，就重新获取一次，可能是交易不活跃，ticker没推送
                if(parseFloat(msgTime)/1000 - accountInfo[symbol].records[accountInfo[symbol].records.length-1].Time/1000 > 1.5*periodSecond){
                    var currency = symbol + '_' + baseCoin;
                    exchange.IO("currency", currency)
                    var records = exchange.GetRecords(period)
                    if(records){
                        accountInfo[symbol].records = exchange.GetRecords(period)
                    }
                    Log(symbol, 'K线有缺失,重新获取')
                }else{
                    //推送一根新K线
                    accountInfo[symbol].records.push({"Time":parseInt(lastPeriodTime + periodSecond)*1000, "Open":accountInfo[symbol].last, "High":accountInfo[symbol].last,
                    "Low":accountInfo[symbol].last, "Close":accountInfo[symbol].last, "Volume":0})
                }
            }
        }
        lastPeriodTime = lastPeriodTime + periodSecond
        Log(parseFloat(msgTime)/1000, '添加K线')
    }else{
        //如果在当前K线周期内，更新当前K线
        for (var symbol in accountInfo){
            if(symbol != baseCoin){
                var length = accountInfo[symbol].records.length
                accountInfo[symbol].records[length-1].Close = accountInfo[symbol].last
                accountInfo[symbol].records[length-1].Volume += accountInfo[symbol].volume
                if(accountInfo[symbol].last > accountInfo[symbol].records[length-1].High){
                    accountInfo[symbol].records[length-1].High = accountInfo[symbol].last 
                }
                else if(accountInfo[symbol].last < accountInfo[symbol].records[length-1].Low){
                    accountInfo[symbol].records[length-1].Low = accountInfo[symbol].last
                }
            }
        }
    }
}
```

## **4.交易相关函数**

```c
//取消当前交易对订单
function CancelPendingOrders() {
    var orders = _C(exchange.GetOrders);
    for (var j = 0; j < orders.length; j++) {
        exchange.CancelOrder(orders[j].Id, orders[j]);
    }
}
//取消所有交易对订单
function cancellAll(){
    try{
        var openOrders = exchange.IO('api', 'GET', '/api/v3/openOrders');
        for (var i=0; i<openOrders.length; i++){
            var order = openOrders[i];
            var currency = order.symbol.slice(0,order.symbol.length-baseCoin.length) + '_' + baseCoin;
            exchange.IO("currency", currency);
            exchange.CancelOrder(order.orderId);
        }
    }
    catch(err){
        Log('取消订单失败');
    }
    for (var symbol in accountInfo){
        accountInfo[symbol].state = 0;
        accountInfo[symbol].buyprice = 0;
        accountInfo[symbol].sellPrice = 0;
    }
}
//下买单
function toBuy(){
    //需要买的币种都储存在buyList种
    if (buyList.length == 0){
        return;
    }
    for (var i=0; i<buyList.length; i++){
        var symbol =  buyList[i];
        //滑点是卖一价加最小交易单位，可能不会立即完全成交，可自行设置
        var buyPrice = accountInfo[symbol].ask + accountInfo[symbol].tickerSize;
        buyPrice = _N(buyPrice, parseInt((Math.log10(1.1/accountInfo[symbol].tickerSize))));//满足价格精度
        var currency = symbol + '_' + baseCoin;
        exchange.IO("currency", currency);//切换交易对
        //如果已经下单，并和本次价格相同，不操作
        if (accountInfo[symbol].state && accountInfo[symbol].bid == accountInfo[symbol].buyprice){
            continue;
        }else{
            //已下单先撤销
            if (accountInfo[symbol].state == 1){
                CancelPendingOrders();
                accountInfo[symbol].state = 0;
                accountInfo[symbol].buyprice = 0;
            }
            var amount = (accountInfo[symbol].free + accountInfo[symbol].frozen)*buyPrice; //现有币种的价值
            var needBuyBTC = HoldAmount - amount;/HoldAmount是全局参数，需要持有的价值
            var buyAmount = needBuyBTC/buyPrice;
            buyAmount = _N(scale*buyAmount, parseInt((Math.log10(1.1/accountInfo[symbol].stepSize))));//下单量精度
            //满足最小交易量和最小交易价值要求
            if (buyAmount > accountInfo[symbol].minQty && buyPrice*buyAmount > accountInfo[symbol].minNotional){
                if (accountInfo[baseCoin].free < buyPrice*buyAmount){return;}//有足够的基础货币购买
                var id = exchange.Buy(buyPrice, buyAmount, currency);//最终下单
                if(id){
                    accountInfo[symbol].buyprice = buyPrice;
                    accountInfo[symbol].state = 1;
                }
            }
        }
        //如果买单过多，需要休眠，币安1s最多下10单
        if(buyList.length > 5){
            Sleep(200)
        }
    }
}
//下卖单原理与买单相似
function toSell(){
    if (sellList.length == 0){
        return;
    }
    for (var i=0; i<sellList.length; i++){
        var currency = symbol + '_' + baseCoin;
        exchange.IO("currency", currency);
        var sellPrice = accountInfo[symbol].bid - accountInfo[symbol].tickerSize;
        sellPrice = _N(sellPrice, parseInt((Math.log10(1.1/accountInfo[symbol].tickerSize))));
        if (accountInfo[symbol].state == 1 && accountInfo[symbol].bid != accountInfo[symbol].buyprice){
            CancelPendingOrders();
            accountInfo[symbol].state = 0;
            accountInfo[symbol].sellPrice = 0;
        }
        var sellAmount = accountInfo[symbol].free;
        sellAmount = _N(Math.min(scale*sellAmount,accountInfo[symbol].free), parseInt((Math.log10(1.1/accountInfo[symbol].stepSize))));
        if (sellAmount > accountInfo[symbol].minQty && sellPrice*sellAmount > accountInfo[symbol].minNotional){
            var id = exchange.Sell(sellPrice, sellAmount, currency);
            if(id){
                accountInfo[symbol].state = 1;
                accountInfo[symbol].sellPrice = sellPrice;
            }
        }
        if(sellList.length > 5){
            Sleep(200)
        }
    }
}
```

## **5.交易的逻辑**

交易很简单，只要把买卖的币种推送到buyList和sellList中就可以了

```cpp
function checkTrade(){
    buyList = []
    sellList = []
    for(var symbol in accountInfo){
        if(symbol == baseCoin){
            continue
        }
        var length = accountInfo[symbol].records.length
        //简单均线，只做一个简单的演示例子，不要实盘使用，自己交易咯及放在这里就可以了
        var fast = TA.MA(accountInfo[symbol].records, FastPeriod)[length-1]
        var slow = TA.MA(accountInfo[symbol].records, SlowPeriod)[length-1]
        if(accountInfo[symbol].value > 2*accountInfo[symbol].minNotional && fast < 0.99*slow){
            sellList.push(symbol)
        }
        //HoldAmount策略参数
        if(accountInfo[symbol].value < 0.9*HoldAmount && fast > 1.01*slow){
            buyList.push(symbol)
        }
    }
}
```

## **6.更新机器人界面状态和ticker**

这么多交易币种如何展示也是个问题，幸好FMZ量化平台提供了完善的表格功能，还可以按照数字大小排序，简单直观方便。每次websocket推送ticker时更新，由于是事件驱动，交易和各类更新的逻辑也放在这里。

```cpp
function updateStatus(msgTime){
    //具体要展示的数据信息可以自己定义
    var table = {type: 'table', title: '持仓信息', 
             cols: ['币种', 'Bid', 'Ask','Last', '最低价','最高价','涨幅','成交量','买入价','卖出价', '冻结','可用','现值'],
             rows: []};
    for (var symbol in accountInfo){
        if(symbol == baseCoin){
            var infoList = [symbol,0, 0, 1,0, 0, 0,0, 0, 0, 0, _N(accountInfo[symbol].frozen,4),_N(accountInfo[symbol].free,4), _N(accountInfo[symbol].value,5)];
        }else{
            var infoList = [symbol,accountInfo[symbol].bid, accountInfo[symbol].ask, accountInfo[symbol].last,
                        accountInfo[symbol].lowPrice, accountInfo[symbol].highPrice, accountInfo[symbol].priceChangePercent,
                        _N(accountInfo[symbol].volume,2), accountInfo[symbol].buyPrice, accountInfo[symbol].sellPrice,
                        _N(accountInfo[symbol].frozen,4),_N(accountInfo[symbol].free,4), _N(accountInfo[symbol].value,5)];
        }
        table.rows.push(infoList);
    }
    var logString = _D() + ' 净值为:' + _N(totalbtc,6) + (typeof(msgTime) == 'number' ? (', 最新行情时间: ' + _D(msgTime)) : '') + '\n';
    logString += '将要买入的币：' + buyList.join(',') + ' \n';
    logString += '将要卖出的币：' + sellList.join(',') + ' \n';
    logString += '当前可用'+ baseCoin + '：' + _N(accountInfo[baseCoin].free,6) + ',冻结：' + _N(accountInfo[baseCoin].frozen,6)  + '\n';
    LogStatus(logString + '`' + JSON.stringify(table) + '`');//更新到机器人界面
}
//每次推送ticker时更新，由于是事件驱动，交易和各类更新的逻辑也放在这里
function updateTicker(msg){
    var ticker = msg;
    var msgTime = 0;
    for (var i=0; i<ticker.length; i++){
        msgTime = Math.max(msgTime, ticker[i].E);
        var symbol = ticker[i].s.slice(0,ticker[i].s.length-baseCoin.length)
        if (ticker[i].s.slice(ticker[i].s.length-baseCoin.length) == baseCoin && parseFloat(ticker[i].c) && symbol in accountInfo){
            accountInfo[symbol].last = parseFloat(ticker[i].c);
            accountInfo[symbol].volume = _N(parseFloat(ticker[i].q),1);
            accountInfo[symbol].lowPrice = parseFloat(ticker[i].l);
            accountInfo[symbol].highPrice = parseFloat(ticker[i].h);
            accountInfo[symbol].ask = parseFloat(ticker[i].a);
            accountInfo[symbol].bid = parseFloat(ticker[i].b);
            accountInfo[symbol].priceChangePercent = parseFloat(ticker[i].P);
            accountInfo[symbol].value = (accountInfo[symbol].free + accountInfo[symbol].frozen)*accountInfo[symbol].last
        }
    }
    if (Date.now() - updateProfitTime > LogProfitTime*1000){
        updateAccount();
        updateProfitTime = Date.now();//重置收益时间
        LogProfit(totalbtc);//更新收益
    }
    updateRecords(msgTime)//更新K线
    updateTotalBTC();//更新总市值
    updateStatus(msgTime);//更新机器人状态
    checkTrade()//检查需要下哪些订单
    toBuy();//下买单
    toSell();//下买单
}
```

## **7.执行汇总**

```python
function main() {
    cancellAll();
    initRecords()
    updateAccount();
    updateTotalBTC()
    Log('共交易数字货币:', Object.keys(accountInfo).length-1);
    updateStatus();
    var client = Dial("wss://stream.binance.com:9443/ws/!ticker@arr");
    while (true){
        var data = client.read();
        var msg = JSON.parse(data);
        updateTicker(msg);
    }
}
```

## **8.总结**

本文主要展示了一个基础的币安多币种交易框架，主要包含了如何储存交易信息、如何根据ticker合成K线、如何下单、如何展示策略图表以及基于ticker推送事件触发交易等。可以更改和定制的地方很多，整体由我个人策略摘录而来，可能隐含Bug，仅供有一定基础的用户参考。  


