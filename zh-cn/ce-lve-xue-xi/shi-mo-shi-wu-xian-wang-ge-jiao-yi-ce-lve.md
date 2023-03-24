# 什么是无限网格交易策略？

[Skip to content](https://www.antrade.io/guide/docs/cn/infinity\_grid/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/cn/)[首页](https://www.antrade.io/guide/docs/cn/)[免费使用AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/cn)
* [策略学习](https://www.antrade.io/guide/docs/cn/cn-strategy/)
* [什么是无限网格交易策略？](https://www.antrade.io/guide/docs/cn/infinity\_grid/)

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

## 什么是无限网格交易策略？

2月 ago[AntBot](https://www.antrade.io/guide/docs/cn/author/antbot/)1 minute

#### 什么是无限网格交易策略？

**无限网格交易策略是针对震荡上涨行情优化的现货交易策略**，无论价格涨幅多大永远都会持有一部分资产可以卖出获利，完美地避免了行情持续上涨时没有持仓资产可以卖出的情况。在震荡上涨的行情中，无限网格只会卖出资产升值后的“利润”，确保交易者始终握有与初始仓位等值的资产**。只要这个资产保持震荡上涨，你用无限网格不仅仅能够收益震荡的利润，也可以获得单边上涨的趋势利润。**

#### 无限网格策略的交易原理

AntBot的无限网格原理非常简单，就是让你的现货保持在一定的金额。

举例假设以1,000USDT建立一个BTC的无限网格。在目前的价格买入价值为500USDT的BTC,剩下的500USDT保留。假定设置单个网格为10%。（忽略手续费不计）

如果BTC的价值上涨10%达到550USDT,就卖出50USDT的BTC。此时持有500USDT的BTC和550USDT。其中50USDT就是网格利润，每次交易就会卖出一部分BTC。卖出后USDT会增加，总利润也会增加。

<figure><img src="https://www.antrade.io/guide/docs/cn/wp-content/uploads/2023/01/up@2x.jpg" alt=""><figcaption></figcaption></figure>

如果BTC的价值下跌10%达到450USDT,就拿出保留的50USDT购买BTC，使BTC维持在500USDT。此时整体价值变成950USDT, USDT数量减少，而BTC数量增加。总利润减少50USDT。

<figure><img src="https://www.antrade.io/guide/docs/cn/wp-content/uploads/2023/01/down@2x.jpg" alt=""><figcaption></figcaption></figure>

由于BTC的价值一直维持在500USDT, 只要它的价格不归零，那么网格就可以循环往复低买高卖产出网格利润，称作无限网格。

#### AntBot无限网格的特点

* **首先AntBot的无限网格策略只支持现货机器人**。
* **系统默认按标的资产波动率制定网格区间（网格间隔可低至0.25%）。**
* **AntBot的无限网格支持小资金启动机器人**。**例如，以200USDT就可以开启无限网格机器人。**
* **自动寻找标的资产近期支撑位作为最低价限制价格以实现最大收益风险比。（为了降低风险低于此价格后停止购入资产。）**
*

#### 如何降低无限网格的风险？

当价格长期下跌时依然会造成浮动亏损。因为当价格不断下跌时，系统会不断地帮你买入该币以维持手中资产总值，但如此一来本金就会被不断消耗，而且也会出现较大的浮亏。所以在开启无限网格机器人之前，要**选择长期看好未来预期涨幅的币种, 并且根据自己的资金情况合理设置无限网格运行的最低价格来降低风险**，同时也可以设置止盈和止损作为机器人的出场条件。

#### 如何开启无限网格机器人？

<figure><img src="https://www.antrade.io/guide/docs/cn/wp-content/uploads/2023/01/%E5%90%AF%E5%8A%A8%E6%AD%A5%E9%AA%A4@1.25x.jpg" alt=""><figcaption></figcaption></figure>

#### 优点：

1、因为市场波动性的存在，无限网格机器人获得的总利润要比持有现货资产要高得多。

2、适合长期投资，不会像经典网格交易那样超过价格区间就会停止交易，无限网格会比经典网格交易更加适合放置长时间投资。

3、无视价格区间，只设置网格的交易方式。只要价格的波动达到策略设置的网格间隔，就能够不断地高抛低吸以套取利润。

4、不管币价怎么涨跌，无限网格都始终持有等值的加密资产。

5、不管价格涨多高都有永远卖不完的资产，即便最后涨了一万倍还是会留有一部分可以继续卖出，因为过程中并没有任何一次交易是全部卖掉的。

6、适合长期持有某个交易对，譬如BTC/USDT、ETH/USDT等。

#### 缺点：

1、无限网格交易不存在价格区间，所以会有资金处于闲置状态。对比经典网格，无限网格资金利用率较低。短期内很难看到很高的利润。

2、投资金额比较大。无限网格不存在价格上限，交易区间更广泛，所以需要更大的资金量才能保证交易顺利进行。

@AntBot free trading bot\
