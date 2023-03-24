# 什么是双向网格交易策略？

[Skip to content](https://www.antrade.io/guide/docs/cn/cn\_strategy\_dual\_grid/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/cn/)[首页](https://www.antrade.io/guide/docs/cn/)[免费使用AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/cn)
* [策略学习](https://www.antrade.io/guide/docs/cn/cn-strategy/)
* [什么是双向网格交易策略？](https://www.antrade.io/guide/docs/cn/cn\_strategy\_dual\_grid/)

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

## 什么是双向网格交易策略？

5月 ago[AntBot](https://www.antrade.io/guide/docs/cn/author/antbot/)1 minute

**目录：**

* [**双向网格盈利原理**](https://www.antrade.io/guide/docs/cn/cn\_strategy\_dual\_grid/#2d6ygh)\

* [**小蚁的双向网格AI有何特性**](https://www.antrade.io/guide/docs/cn/cn\_strategy\_dual\_grid/#7owm0t)\

* [**双向网格策略它解决了什么问题**](https://www.antrade.io/guide/docs/cn/cn\_strategy\_dual\_grid/#cljkt2)\

* [**双向网格的优缺点**](https://www.antrade.io/guide/docs/cn/cn\_strategy\_dual\_grid/#1v6rwz)\

* [**如何启动双向网格机器人**](https://www.antrade.io/guide/docs/cn/cn\_strategy\_dual\_grid/#how\_to\_start)

#### 双向网格的盈利原理 <a href="#2d6ygh" id="2d6ygh"></a>

双向网格策略是针对震荡行情可以同时做多和做空的合约网格策略。它是在小蚁[现货网格AI](https://www.antrade.io/guide/docs/cn/cn\_strategy\_grid\_ai/)上延伸而来的策略，可以把双向网格看作两个独立运行5倍杠杆率且方向相反两个网格AI机器人。

当多头机器人的网格头寸达到止盈比例被止盈时，空头机器人将以刚刚多头机器人的止盈价相同的价购入一格空头头寸，这样每当一个网格在当前趋势的方向上产生利润时，另一个网格就会亏损，反之亦然。这个就是双向网格运行特点。

在这种情况下，网格的每一边都应该有自己的利润和止损，在波动行情中，独立管理两个网格的交易，实现利润锁定。

这个就是双向网格盈利原理。双向网格策略有助于更快地达到总利润目标并最小化回撤。

如下图所示：

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2022/12/double_grid_setup.webp" alt=""><figcaption></figcaption></figure>

**双向网格策略解决了什么问题**

小蚁双向网格是AntBot团队独创策略之一。它完美解决了经典网格策略三大问题。\
\
**1、超出网格区间不产生利润。**\
双向网格同时运行多和空两个方向的机器人，不管价格涨还是跌都会有利润产生。\
\
**2、资金效率低。**\
单边网格遇到持续反方向行情，持续投入资金加仓，并且只能等待价格回归才有利润产出。\
因为双向网格同时运行相同期货资产的多和空两个方向的机器人，假如价格持续下跌多头机器人加仓，此时空头机器人会持续平仓盈利，反之，假如价格持续上涨空头机器人加仓，此时多头机器人会持续平仓盈利。同一时间只需准备一份资金给一个方向上的机器人加仓，承担一份资金风险获得两份利润回报。\
另外小蚁双向网格策略会根据不同标的支撑阻力位和波动率制定各自的网格区间，平衡风险和收益比。\
\
**3、突破价格区间（破网）后无法及时自动调整**\
小蚁双向网格是没有上下价格边界的，在突破一边的网格后，AI系统会重新计算支撑阻力位，再次购入初始仓位，价格持续单边时逐格止盈跟踪行情获利。

**小蚁的双向网格AI有何特性**

1、没有挂限价单，共享保证金防止爆仓。\
2、每个格子的止盈是独立计算和执行，进行分仓止盈，提高资金流动性。\
3、两个独立运行的多头网格和空头网格被视为两个独立的系统，因为两者都有明确的盈利和卖出界限。\
4、小蚁和交易所两者交易记录中盈亏显示有差别，因为小蚁是根据每个格子的开仓价和成交价计算该格子的盈亏，而交易所是根据持仓均价计算每份订单的盈亏。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/10/%E4%BB%80%E9%BA%BC%E6%98%AF%E9%9B%99%E5%90%91%E7%B6%B2%E6%A0%BC%E5%90%88%E7%B4%84%E4%BA%A4%E6%98%93%E7%AD%96%E7%95%A52.jpg" alt=""><figcaption></figcaption></figure>

**双向网格的优点**

* 无需预测市场的走势。
* 在动荡、无方向的市场中运作良好。
* 在适当的条件下可能非常有效——尤其是价格在网格区间内快速波动时。

**双向网格的缺点**

* 网格策略要求对每个订单资产的交易独立结算盈亏，这种结算方式和交易所按均价结算盈亏的方式不同，导致交易者不理解和不方便对账。
* 多个网格意味着需要更复杂的交易和资金管理。
* 当有强烈的方向性趋势时，突破网格区间时,会出现比较大的浮亏。

**如何启动双向网格机器人**

<figure><img src="https://www.antrade.io/guide/docs/cn/wp-content/uploads/2022/12/%E6%9C%AA%E6%A0%87%E9%A2%98-2.jpg" alt=""><figcaption></figcaption></figure>

只多：只会开多和平多，适合于震荡向上的行情。

只空：只会开空和平空，适合于震荡向下的行情。

震荡：在策略开启时的市场价格的上方开空或者平空，下方开多或者平多，适用于区间横盘震荡行情。

[#ai grid](https://www.antrade.io/guide/docs/cn/tag/ai-grid/)[#AntBot](https://www.antrade.io/guide/docs/cn/tag/antbot/)[#dual grid](https://www.antrade.io/guide/docs/cn/tag/dual-grid/)[#strategy](https://www.antrade.io/guide/docs/cn/tag/strategy/)[#trading](https://www.antrade.io/guide/docs/cn/tag/trading/)@AntBot free trading bot\
