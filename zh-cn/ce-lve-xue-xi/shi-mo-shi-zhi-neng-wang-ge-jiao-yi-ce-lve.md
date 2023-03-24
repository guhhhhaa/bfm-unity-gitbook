# 什么是智能网格交易策略？

[Skip to content](https://www.antrade.io/guide/docs/cn/cn\_strategy\_grid\_ai/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/cn/)[首页](https://www.antrade.io/guide/docs/cn/)[免费使用AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/cn)
* [策略学习](https://www.antrade.io/guide/docs/cn/cn-strategy/)
* [什么是智能网格交易策略？](https://www.antrade.io/guide/docs/cn/cn\_strategy\_grid\_ai/)

Search for:

策略学习

*
  * [什么是无限网格交易策略？](https://www.antrade.io/guide/docs/cn/infinity\_grid/)
  * [什么是定投策略？](https://www.antrade.io/guide/docs/cn/regular\_investment/)
  * [什么是阵型交易策略？](https://www.antrade.io/guide/docs/cn/strategy\_formation/)
  * [什么是动量交易策略？](https://www.antrade.io/guide/docs/cn/strategy-momentum/)
  * [什么是双均线交易策略?](https://www.antrade.io/guide/docs/cn/d-kama/)
  * [什么是R-Breaker交易策略?](https://www.antrade.io/guide/docs/cn/r-breaker/)
  * [什么是超级趋势交易策略？](https://www.antrade.io/guide/docs/cn/supertrend/)
  * [什么是相对价值交易策略?](https://www.antrade.io/guide/docs/cn/relative-value/)
  * [什么是双向网格交易策略？](https://www.antrade.io/guide/docs/cn/cn\_strategy\_dual\_grid/)
  * [什么是智能调仓策略？](https://www.antrade.io/guide/docs/cn/cn\_strategy\_rebalancing/)
  * [什么是经典网格交易策略?](https://www.antrade.io/guide/docs/cn/cn\_strategy\_grid/)
  * [什么是智能网格交易策略？](https://www.antrade.io/guide/docs/cn/cn\_strategy\_grid\_ai/)
  * [什么是智能马丁交易策略？](https://www.antrade.io/guide/docs/cn/cn\_strategy\_dca/)
  * [什么是贝塔策略？](https://www.antrade.io/guide/docs/cn/strategy\_ai\_beta/)

## 什么是智能网格交易策略？

6月 ago[AntBot](https://www.antrade.io/guide/docs/cn/author/antbot/)1 minute

#### 什么是现货智能网格策略 <a href="#3gvn9j" id="3gvn9j"></a>

现货网格AI交易策略是AntBot团队基于[经典网格策略](https://www.antrade.io/guide/docs/cn/cn\_strategy\_grid/)对收益/风险比深度优化的震荡交易策略。

智能网格策略本质是一个**滑动网格策略**，非常适用震荡和上涨行情，它解决了经典区间网格在持续上涨行情时的踏空问题，即网格持仓已全部止盈头寸为空时，市价持续上涨却没有利润产生。

网格AI策略是一种在特定的价格区间中执行低买高卖的自动化策略，用户只需要设定区间最高价和最低价，确定好要细分的网格数，即可开始运行策略。策略会计算每个小网格低买高卖的价格，自动挂单，随着市场波动，不断地低吸高抛赚取波动带来的收益。

**现货智能网格策略的盈利原理**

通过设定价格区间，机器人将把资金分成许多份，币价跌一格就买一份，然后挂上比买入价高一小格的卖单，当币价涨到这一段时就卖出去。每次的卖出价都比买入价高一点。如果一直跌，就一直买下去，直到设定的区间下限；如果一直涨，就一直卖出去，到设定的价格上限为止。如果价格涨涨跌跌，就低买高卖。如此随着市场波动而循环地挂单和成交，就可以不断赚取震荡行情中的波动收益。

<figure><img src="https://www.antrade.io/guide/docs/cn/wp-content/uploads/2022/12/%E6%88%AA%E5%B1%8F2022-10-27-14.55.07.png" alt=""><figcaption></figcaption></figure>

**现货智能网格是如何运作的？**

1\. 计算网格间隔

它先根据ATR算法计算当前品种的真实波动率，以这个波动率算出网格间隔比例。

2\. 计算首次持仓\
再采用Support/Resistance V2算法计算价格上方最近的一个阻力位，得到这个阻力位价格可以算出首次持仓大小（阻力位价格-当前价格）/ 网格间隔。

采用阻力位和真实波幅计算出来的首次持仓和网格间隔，能很大程度保证每个品种的网格间隔在吃到最多的波段的同时支持最低的价格下限，换句话说，支持价格最大跌幅时保证最大利润。

3\. 计算价格下限

根据以上结果,在指定网格数量情况下也就可以计算出最小能支持的价格下限，这里所说的的价格下限就是市价在跌入这个价格时，网格刚好全部持仓的价格。价格下限代表这个机器人所布置的网的大小，这个网越大，网格越密集能适应的行情越广泛，盈利能力越强。把网变大变密集的直接办法就是增加本金的投入,也就是增加网格数量，在指定本金的情况下，增加网格间隔也可以降低价格下限，但这么做机器人就会错过小波段的利润。AI可以平衡本金、风险和利润的关系。

**现货网格AI参数介绍**

* 每格投入：\
  每格开仓固定投入的资产(USDT)。
* 网格间隔(%)：\
  机器人将按照此设置的比率覆盖一个新的网格或平仓止盈一个网格。
* 网格数量：\
  网格数量的最大限制。
* 风险偏好：\
  支持3个等级的风险类型，保守、稳健、激进。风险偏好直接影响网格间隔，风险越高网格间隔越小。
* 价格下限：\
  固定价格上限后，根据网格间隔和网格数量得出，最大能支持网格布置到的价格下限位置。
* 网格布局\
  等差间隔: 每个网格的价格距离都是按照固定数值相加。\
  等比间隔: 每个网格的价格距离都是按照固定比例相乘。
* 首次持仓：\
  在启动机器人时或者机器人处于空仓状态下，执行一次性布局一定数量的网格，以应对价格持续上行而踏空。
* 入场价格：\
  限制机器人按所设定的价格启动。
* 止盈回调(%)：价格跟踪止盈功能，当价格上行到最高点回落此设定比例并且同时满足网格间隔比例才止盈。
* 补仓回调(%)：价格跟踪补仓功能，当价格下行到最低点回弹此设定比例并且同时满足网格间隔比例才补仓覆盖网格。

**止盈止损**

按金额止盈\
实现盈亏+浮动盈亏>该预设金额，满足上述条件机器人将会自动清仓止盈并停止运行。

按金额止损\
实现盈亏+浮动盈亏<-该预设金额，满足上述条件机器人将会自动清仓止损并停止运行。

**如何启动网格AI机器人**

<figure><img src="https://www.antrade.io/guide/docs/cn/wp-content/uploads/2022/12/%E6%9C%AA%E6%A0%87%E9%A2%98-1-1.jpg" alt=""><figcaption></figcaption></figure>

@AntBot free trading bot\
