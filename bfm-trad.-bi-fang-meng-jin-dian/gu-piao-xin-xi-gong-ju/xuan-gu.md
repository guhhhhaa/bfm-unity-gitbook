# 选股

{% hint style="info" %}
NOTE: 策略推荐市盈率，市净率策略，

**该策略的特点是 —— 抗跌不跟涨，跟涨选指数**
{% endhint %}

## 大盘

### 沪深300

沪深300-市净率

[https://robo.datayes.com/v2/landing/monitor\_detail?slotId=238422](https://robo.datayes.com/v2/landing/monitor\_detail?slotId=238422)

沪深300-市盈率

[https://robo.datayes.com/v2/landing/monitor\_detail?slotId=238421](https://robo.datayes.com/v2/landing/monitor\_detail?slotId=238421)

### 上证综指

上证综指-市净率

[https://robo.datayes.com/v2/landing/monitor\_detail?slotId=238420](https://robo.datayes.com/v2/landing/monitor\_detail?slotId=238420)

上证综指-市盈率

[https://robo.datayes.com/v2/landing/monitor\_detail?slotId=238419](https://robo.datayes.com/v2/landing/monitor\_detail?slotId=238419)

## 选股

### 因子看板——风险因子，风格因子

[https://www.joinquant.com/view/factorlib/list](https://www.joinquant.com/view/factorlib/list)

### 市净率因子 book\_to\_price\_ratio

（教科书上是价格/净值，这个是净值/价格，所以教科书上选小的，这个选大的）\
**（回测区间选10年）**\
**（策略：按照市值比例购买。预计未来下跌时选择最大分位数的股票，预计上涨时选指数）**\
[https://www.joinquant.com/view/factorlib/detail/f297b9704818db80ad7fde91fe42b493?buildtype=0\&universetype=aHMzMDA%3D\&period=M3k%3D\&commisionFee=MA%3D%3D\&skipPaused=MQ%3D%3D](https://www.joinquant.com/view/factorlib/detail/bb3b7b42b7425d4ada99603b008724d4?buildtype=0\&universetype=aHMzMDA%3D\&period=M3k%3D\&commisionFee=MA%3D%3D\&skipPaused=MQ%3D%3D)

### 预期市盈率 predicted\_earnings\_to\_price\_ratio

（教科书上是价格/收益，这个是收益/价格，所以教科书上选小的，这个选大的）\
**（回测区间选10年）**\
**（策略：按照市值比例购买。预计未来下跌时选择最大分位数的股票，预计上涨时选指数）**\
[https://www.joinquant.com/view/factorlib/detail/bb3b7b42b7425d4ada99603b008724d4?buildtype=0\&universetype=aHMzMDA%3D\&period=M3k%3D\&commisionFee=MA%3D%3D\&skipPaused=MQ%3D%3D](https://www.joinquant.com/view/factorlib/detail/bb3b7b42b7425d4ada99603b008724d4?buildtype=0\&universetype=aHMzMDA%3D\&period=M3k%3D\&commisionFee=MA%3D%3D\&skipPaused=MQ%3D%3D)

## 投资建议

选股是没有必要的，技术分析一概不靠谱。最好的选股就是指数。至于个股，和个基金，我是从来不推荐的。推荐买入股票指数基金和债券基金。

真正需要做的是，股票指数和债券的配比关系。而股票指数和债券的配比关系是按照大盘的市净率和市盈率来决定的。

一切通过技术分析，想要跑赢沪深300和纳指100的尝试都是徒劳的。选股和操作没有用，噪声操作会加大你的亏损，不信你做个10年回测就明白——[https://www.joinquant.com/view/factorlib/list](https://www.joinquant.com/view/factorlib/list) 这个是因子分析，可以选择你的选股策略进行回测，如果你把周期拉到10年，你会发现，相比技术分析指数才是真正有效的选择。

如果说什么有用，也就是，市净率，市盈率，才有用。 而且市净率，市盈率只有下跌行情有用，能抗跌，

上涨行情都偏离价值，所以市净率，市盈率无法用来追涨。

{% embed url="https://guhhhhaa.gitbook.io/joinquant/jin-rong-li-lun-zong-jie/ji-ben-mian-xuan-gu" %}

{% hint style="success" %}
### 选股，成长性：

净资产收益率ROE＞15%（\*\*>10%\*\*就不错）（ROE=PB/PE），\
且用杜邦分析剔除杠杆（权益乘数<3）。

股息率＞5%，（[不绝对](https://xueqiu.com/4195046382/148444383)，可以不加）

市盈率相对盈利增长比率[PEG](https://xueqiu.com/8287840120/74917276)＜0.5。（<1也可）（[参考](https://xueqiu.com/8287840120/83909262)）

### 确定买卖点，相对估值，低估高估：

介绍：[估值和资本结构因子](https://xueqiu.com/8287840120/102600210)

市盈率P/E＜10，—— 0 - 12买入，>20卖出

市净率P/B＜2， —— 0 - 1.2买入，>2卖出

[**https://www.ricequant.com/quant/wizard/**](https://www.ricequant.com/quant/wizard/)

[**https://www.joinquant.com/wizardstock/index/generateStock**](https://www.joinquant.com/wizardstock/index/generateStock)

[**回测结果**](https://www.ricequant.com/quant/backtest/6224534)
{% endhint %}

![](<../../.gitbook/assets/屏幕快照 2021-02-28 下午1.29.34.png>)

![](<../../.gitbook/assets/屏幕快照 2021-02-28 下午1.24.27.png>)

![横轴是估值，纵轴是仓位和操作](../../.gitbook/assets/0E2ABFCC2987F6AAEB09ECE758F3E8AC.jpg)

## 林园投资

![](<../../.gitbook/assets/image (50).png>)

## 海龟交易法则

{% embed url="https://www.zhihu.com/zvideo/1408466616892313601" %}

{% embed url="https://www.zhihu.com/zvideo/1386620312193126400" %}

\+0.5ATR加仓，-2ATR减仓

![](<../../.gitbook/assets/image (46).png>)

突破20日最高点做多，跌破10日最低点平多。

跌破20日最低点做空，突破10日最高点平空。
