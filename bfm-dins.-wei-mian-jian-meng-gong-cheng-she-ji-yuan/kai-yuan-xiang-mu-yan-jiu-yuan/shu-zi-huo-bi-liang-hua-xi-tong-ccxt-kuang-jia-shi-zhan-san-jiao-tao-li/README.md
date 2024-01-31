# CCXT 领域级重点实验室🚩

[**数字货币量化系统 CCXT 框架实战三角套利**](http://www.digtime.cn/articles/282/shu-zi-huo-bi-liang-hua-xi-tong-ccxt-kuang-jia-shi-zhan-san-jiao-tao-li) **|** [**本地链接**](https://www.bfm-unity.com/command-room-discovery/san-jiao-tao-li-shi-yan-shi/shu-zi-huo-bi-liang-hua-xi-tong-ccxt-kuang-jia-shi-zhan-san-jiao-tao-li) **|** [**课程地址**](https://study.163.com/course/courseMain.htm?courseId=1006162003) **|** [**源码**](https://github.com/guhhhhaa/Bitcoin-Quant/tree/main)\*\*\*\*

[**CCXT中文文档**](http://cw.hubwiz.com/card/c/ccxt-dev-manual/1/1/1/) **|** [**CCXT英文文档**](https://github.com/ccxt/ccxt/wiki)

[**CCXT公有API课程**](https://www.bilibili.com/video/av57636895/) **🚩**

[**CCXT私有API课程**](https://www.bilibili.com/video/BV1L4411w7iv/) **🚩**

\*\*\*\*[**CCXT Example - Github**](https://github.com/ccxt/ccxt/tree/master/examples) **🚩**

{% content-ref url="ccxt-ke-ti-zu-1.md" %}
[ccxt-ke-ti-zu-1.md](ccxt-ke-ti-zu-1.md)
{% endcontent-ref %}

{% content-ref url="ccxt-zhong-wen-kai-fa-shou-ce.md" %}
[ccxt-zhong-wen-kai-fa-shou-ce.md](ccxt-zhong-wen-kai-fa-shou-ce.md)
{% endcontent-ref %}

{% embed url="https://github.com/bilibilihuangyifan/cryptohedging/blob/master/blockhedging.py" %}

## 数字货币量化系统 CCXT 框架实战三角套利

> 本篇博文将使用CCXT来进行三角套利实战。

### 原理 <a href="#yuan-li" id="yuan-li"></a>

针对`同一个币种`，由于`计价币种（市场）`不同而带来的`价差`进行套利。

**BTC/USDT**

* 持仓 10000 个USDT
* 可买入 0.7052 个BTC（10000/14179.95）

**BCH/BTC**

* 可买入 4.0824个BCH（0.7052/0.172743）

**BCH/USDT**

* 卖出所有BCH，得到 10010.6671 个USDT(4.0824 x 2452.10)

**获利**

* (10010.6671 - 10000) / 10000 = 1.06671 ‰

![](../../../.gitbook/assets/37FyOotLeD.png)

实际套利转化流程：\
USDT -> BTC -> BCH -> USDT

上边的可以通过简单的套利公式计算出套利收益：

```
Profit = P3/(P1xP2) - 1 # 公式的推到可以看下边的套利步骤
```

说明： P1 为 BTC/USDT = 14179.95, P2 为 BCH/BTC = 0.172743, P3 为 BCH/USDT = 2452.10, 通过上边的公式即可算的收益率为：2452.10 / (14179.95 x 0.172743) - 1 = 0.00106671，可以看到和我们上边通过每笔交易算出来的结果一样。

#### 三角套利步骤[#](http://www.digtime.cn/articles/282/shu-zi-huo-bi-liang-hua-xi-tong-ccxt-kuang-jia-shi-zhan-san-jiao-tao-li#%E4%B8%89%E8%A7%92%E5%A5%97%E5%88%A9%E6%AD%A5%E9%AA%A4) <a href="#san-jiao-tao-li-bu-zhou" id="san-jiao-tao-li-bu-zhou"></a>

![](../../../.gitbook/assets/U6oLVaGCRV.png)

P1 表示 A 的价格，P2 表示 ？的价格，P3 表示 ?/A 的价格

#### 注意事项[#](http://www.digtime.cn/articles/282/shu-zi-huo-bi-liang-hua-xi-tong-ccxt-kuang-jia-shi-zhan-san-jiao-tao-li#%E6%B3%A8%E6%84%8F%E4%BA%8B%E9%A1%B9) <a href="#zhu-yi-shi-xiang" id="zhu-yi-shi-xiang"></a>

* 行情获取的时刻：尽量确保获取的行情数据是`同一时刻`的
* 交易成本：三个币的手续费，如果扣除手续费后依旧有利润，那木就可以进行套利

#### 优势[#](http://www.digtime.cn/articles/282/shu-zi-huo-bi-liang-hua-xi-tong-ccxt-kuang-jia-shi-zhan-san-jiao-tao-li#%E4%BC%98%E5%8A%BF) <a href="#you-shi" id="you-shi"></a>

* 目前市场上大部分套利集中关注双边套利或搬砖，竞争相对比较少
* 相对来说，套利空间更大，利润也更多

#### 劣势[#](http://www.digtime.cn/articles/282/shu-zi-huo-bi-liang-hua-xi-tong-ccxt-kuang-jia-shi-zhan-san-jiao-tao-li#%E5%8A%A3%E5%8A%BF) <a href="#lie-shi" id="lie-shi"></a>

* 同时监控所有三角套利机会比较难
* 同时成交的难度更高
* 对交易系统的并发能力要求很高

### 代码实战 <a href="#dai-ma-shi-zhan" id="dai-ma-shi-zhan"></a>

`tri_arbitrage.py`

```python
import ccxt
import pandas as pd
import time

pd.set_option('expand_frame_repr', False)

def main():
    """
        主函数
    """
    # 初始化交易所
    binance_exchange = ccxt.binance({
        'timeout': 15000,
        'enableRateLimit': True,
        'proxies': {'https': "http://127.0.0.1:1087", 'http': "http://127.0.0.1:1087"}
    })

    # 加载行情
    markets = binance_exchange.load_markets()

    # == Step.1 选择两个交易市场 A, B
    market_a = 'BTC'
    market_b = 'ETH'
    # == Step.1 END =================

    # == Step.2 找到所有同时以 A 和 B 都作为计价的货币
    # 市场内的交易对
    symbols = list(markets.keys())

    # 存放到DataFrame中
    symbols_df = pd.DataFrame(data=symbols, columns=['symbol'])

    # 分割字符串得到 基础货币/计价货币
    base_quote_df = symbols_df['symbol'].str.split(pat='/', expand=True)
    base_quote_df.columns = ['base', 'quote']

    # 过滤得到以 A, B 计价的计价货币
    base_a_list = base_quote_df[base_quote_df['quote'] == market_a]['base'].values.tolist()
    base_b_list = base_quote_df[base_quote_df['quote'] == market_b]['base'].values.tolist()

    # 获取相同的基础货币列表
    common_base_list = list(set(base_a_list).intersection(set(base_b_list)))
    print('{}和{}共有{}个相同的计价货币'.format(market_a, market_b, len(common_base_list)))
    # == Step.2 END =================

    # == Step.3 执行套利步骤

    # 结果保存到DataFrame中，注意，这里的Profit为千分位 ‰（因为利润一般都比较小）
    columns = ['Market A',
               'Market B',
               'Market C',
               'P1',
               'P2',
               'P3',
               'Profit']

    results_df = pd.DataFrame(columns=columns)

    # 获取前一分钟的close价格
    last_min = binance_exchange.milliseconds() - 60 * 1000  # 前一分钟

    for base_coin in common_base_list:
        market_c = base_coin
        market_a2b_symbol = '{}/{}'.format(market_b, market_a)
        market_b2c_symbol = '{}/{}'.format(market_c, market_b)
        market_a2c_symbol = '{}/{}'.format(market_c, market_a)

        # 获取行情前一分钟的K线数据
        market_a2b_kline = binance_exchange.fetch_ohlcv(market_a2b_symbol, since=last_min, limit=1, timeframe='1m')
        market_b2c_kline = binance_exchange.fetch_ohlcv(market_b2c_symbol, since=last_min, limit=1, timeframe='1m')
        market_a2c_kline = binance_exchange.fetch_ohlcv(market_a2c_symbol, since=last_min, limit=1, timeframe='1m')

        if len(market_a2b_kline) == 0 or len(market_b2c_kline) == 0 or market_a2c_kline == 0:
            continue

        try:

            # 获取行情前一分钟的交易对价格
            p1 = market_a2b_kline[0][4]
            p2 = market_b2c_kline[0][4]
            p3 = market_a2c_kline[0][4]
        except IndexError:
            continue

        # 价差
        profit = (p3 / (p1 * p2) - 1) * 1000

        results_df = results_df.append({
            'Market A': market_a,
            'Market B': market_b,
            'Market C': market_c,
            'P1': p1,
            'P2': p2,
            'P3': p3,
            'Profit': profit
        }, ignore_index=True)

        # 显示信息
        print(results_df.tail(1))

        # 防止超过rate limit
        time.sleep(binance_exchange.rateLimit / 1000)
    # == Step.3 END =================

    # 按照收益由高到低排序
    # @see https://www.jianshu.com/p/d12af2b287b6
    results_df = results_df.sort_values(by="Profit", ascending=False)
    # print(new_sort)

    results_df.to_csv('./tri_arbitrage_results.csv', index=None)

if __name__ == '__main__':
    main()
```

## 运行结果：

{% embed url="https://nbviewer.jupyter.org/github/guhhhhaa/TensorAct-of-Stars/blob/main/BFM.ipynb" %}

结果：

![](../../../.gitbook/assets/kVc6cwOUeE.png)

BTC -> ETH -> AION -> BTC

通过运行的结果我们可以看到，前几个交易对表现非常好，利润率达到了 59.14 ‰，即将近 6%，除去手续费，还是有利可图的。

#### 相关名词说明[#](http://www.digtime.cn/articles/282/shu-zi-huo-bi-liang-hua-xi-tong-ccxt-kuang-jia-shi-zhan-san-jiao-tao-li#%E7%9B%B8%E5%85%B3%E5%90%8D%E8%AF%8D%E8%AF%B4%E6%98%8E) <a href="#xiang-guan-ming-ci-shuo-ming" id="xiang-guan-ming-ci-shuo-ming"></a>

交易对：用一种资产（quote currency）去定价另一种资产（base currency）,比如用比特币（BTC）去定价莱特币（LTC），\
就形成了一个LTC/BTC的交易对，\
交易对的价格代表的是买入1单位的base currency（比如LTC）\
需要支付多少单位的quote currency（比如BTC），\
或者卖出一个单位的base currency（比如LTC）\
可以获得多少单位的quote currency（比如BTC）。\
当LTC对BTC的价格上涨时，同等单位的LTC能够兑换的BTC是增加的，而同等单位的BTC能够兑换的LTC是减少的。

base currency：基准资产\
quote currency：定价资产

在外汇交易中，每一次交易买卖是同时在进行着的，在买进基本货币（Base currency）的同时也卖出了报价货币（Quote currency）。
