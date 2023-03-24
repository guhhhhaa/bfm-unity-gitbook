# 什么是经典网格交易策略?

[Skip to content](https://www.antrade.io/guide/docs/cn/cn\_strategy\_grid/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/cn/)[首页](https://www.antrade.io/guide/docs/cn/)[免费使用AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/cn)
* [策略学习](https://www.antrade.io/guide/docs/cn/cn-strategy/)
* [什么是经典网格交易策略?](https://www.antrade.io/guide/docs/cn/cn\_strategy\_grid/)

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

## 什么是经典网格交易策略?

5月 ago[AntBot](https://www.antrade.io/guide/docs/cn/author/antbot/)1 minute

**目录：**

* [**网格策略原理**](https://www.antrade.io/guide/docs/cn/cn\_strategy\_grid/#%E7%BD%91%E6%A0%BC%E7%AD%96%E7%95%A5%E5%8E%9F%E7%90%86)\

* [**如何降低风险**](https://www.antrade.io/guide/docs/cn/cn\_strategy\_grid/#%E5%A6%82%E4%BD%95%E9%99%8D%E4%BD%8E%E9%A3%8E%E9%99%A9)\

* [**如何放大受益**](https://www.antrade.io/guide/docs/cn/cn\_strategy\_grid/#%E5%A6%82%E4%BD%95%E6%94%BE%E5%A4%A7%E5%8F%97%E7%9B%8A)\

* [**如何启动经典网格机器人**](https://www.antrade.io/guide/docs/cn/cn\_strategy\_grid/#%E5%A6%82%E4%BD%95%E5%90%AF%E5%8A%A8%E7%BB%8F%E5%85%B8%E7%BD%91%E6%A0%BC%E6%9C%BA%E5%99%A8%E4%BA%BA)

**网格策略原理**

经典网格是最传统的、最能代表网格策略精髓的版本。

网格交易策略本质上是一种机械式低买高卖的交易系统。设定合适的区间和格子大小，再配套对应的资金和仓位，价格下跌分批买入，价格上涨分批卖出。 通过重复性低买高卖对价格涨跌波动进行利润收割的一种交易方法。

方便大家理解，提供下面示意图参考：

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/10/%E4%BB%80%E9%BA%BC%E6%98%AF%E7%B6%B2%E6%A0%BC%E4%BA%A4%E6%98%93%E7%AD%96%E7%95%A5.gif" alt=""><figcaption></figcaption></figure>

网格交易法不依赖人为的思考，不需要研判行情不需要盘感，完全是一种程序行为，非常适合计算机自动化，利用行情的波动在网格区间内低买高卖，通过反复循环产生差价来赚取利润。

网格交易法属于左侧交易的一种。与右侧交易不同，网格交易法并非跟随行情，追涨杀跌，而是逆势而为，在价格下跌时买入，价格上涨时卖出。

**如何降低风险**

* 选择长周期趋势向上、价格不断创新高的资产，标的选对了，基本也就锁定了利润，最多只亏时间成本。\

* 尽量选择偏低估值横盘震荡区域开启机器人，目的是为了降低时间成本。\
  如果在高估区域划定的网格，遇到市场行情急转直下，可能较长周期内股价无法再回来，只能静待标的内生增长或者下一次市场情绪带动的股价回升，需要付出较大的时间成本和心理成本。

**如何放大受益**

**1、在相同波动频率的标的中，选择波动幅度大的品种**。

在相同波动频率的标的中，波动幅度大的品种，网格间距设定可以更大一些，也就是相同的时间段内每个网格所收割的收益更高，简单示意图如下：

<figure><img src="https://www.antrade.io/guide/docs/cn/wp-content/uploads/2022/12/image.png" alt=""><figcaption></figcaption></figure>

上图中，B代表网格买入，S代表网格卖出，黑线为波幅小的标的，红线为波幅大的标的，很显然，红线走势下的网格操作收益更高。

**2、在相同波动幅度的标的中，选择波动频率越高的品种**。

在相同波动幅度的标的中，波动频率越高的品种，利润收割的频次越高，收益也就更高，简单示意图如下：

<figure><img src="https://www.antrade.io/guide/docs/cn/wp-content/uploads/2022/12/image-1.png" alt=""><figcaption></figcaption></figure>

上图中，B代表网格买入，S代表网格卖出，黑线为波动频率低的标的，红线为波动频率高的标的，很显然，红线走势下的日润收割的频次更高，从而收益更高。

结合以上两种情况，也就是在横盘震荡的市场中，波动幅度越大，波动频率越高，收割的利润也就越多。

那如何选择波动幅度大、波动频率高的品种呢？

除了通过一些量化数据，对于普通交易者，有个简单的方法：把备选操作的几个标的的K线重叠到一起，很容易就能对比分辨出波幅和波频相对占优的标的。

**一句话总结网格交易操作标的选择的关键要素：波动幅度大、波动频率高的优质偏低估值资产。**

**如何启动经典网格机器人**

<figure><img src="https://www.antrade.io/guide/docs/cn/wp-content/uploads/2022/12/%E6%9C%AA%E6%A0%87%E9%A2%98-1.jpg" alt=""><figcaption></figcaption></figure>

[#AntBot](https://www.antrade.io/guide/docs/cn/tag/antbot/)[#bot](https://www.antrade.io/guide/docs/cn/tag/bot/)[#Grid](https://www.antrade.io/guide/docs/cn/tag/grid/)[#regression strategy](https://www.antrade.io/guide/docs/cn/tag/regression-strategy/)[#strategy](https://www.antrade.io/guide/docs/cn/tag/strategy/)[#trading](https://www.antrade.io/guide/docs/cn/tag/trading/)@AntBot free trading bot\
