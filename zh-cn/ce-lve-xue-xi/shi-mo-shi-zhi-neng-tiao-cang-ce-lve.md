# 什么是智能调仓策略？

[Skip to content](https://www.antrade.io/guide/docs/cn/cn\_strategy\_rebalancing/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/cn/)[首页](https://www.antrade.io/guide/docs/cn/)[免费使用AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/cn)
* [策略学习](https://www.antrade.io/guide/docs/cn/cn-strategy/)
* [什么是智能调仓策略？](https://www.antrade.io/guide/docs/cn/cn\_strategy\_rebalancing/)

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

## 什么是智能调仓策略？

5月 ago[AntBot](https://www.antrade.io/guide/docs/cn/author/antbot/)1 minute

**目录：**

* [**为什么要进行调仓?**](https://www.antrade.io/guide/docs/cn/cn\_strategy\_rebalancing/#3cz241)\

* [**怎么配置调仓币种组合?**](https://www.antrade.io/guide/docs/cn/cn\_strategy\_rebalancing/#fkrkow)\

* [**调仓周期或者调仓阈值设置多少合理？**](https://www.antrade.io/guide/docs/cn/cn\_strategy\_rebalancing/#dt42lx)\

* [**智能调仓参数配置说明**](https://www.antrade.io/guide/docs/cn/cn\_strategy\_rebalancing/#br7ybh)

**为什么要进行调仓?**

智能调仓(Rebalancing)是按设定比例持有多种现货资产，当持仓价值占比变动超过调仓阈值时，卖出持仓占比较⾼资产，买⼊持仓占比较低资产，使得组合资产持仓占比回归到初始设定。

智能调仓具有多元持仓，分散风险和长期投资的特性。

短期而言高卖低买会使得部分资产数量变多，部分资产数量变少，针对⼤涨⼤跌的⾏情，通过持仓组合不断调整仓位，让持仓的数字资产占比在⼀定范围内震荡，可有效避免收益因行情而大幅波动。

某⼀数字资产⾏情强势上涨时，通过调仓将收益分配给持仓组合中的其他数字资产，组合持仓可以相对平稳的上涨;下跌时，组合持仓跌幅 可以小于某⼀数字资产的跌幅；最终获得相对平稳的收益。

由于市场波动会长期存在，您持仓的数字资产总量将会越来越多。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/10/%E4%BB%80%E9%BA%BC%E6%98%AF%E6%99%BA%E8%83%BD%E8%AA%BF%E5%80%89%E7%AD%96%E7%95%A51.png" alt=""><figcaption></figcaption></figure>

**怎么配置调仓币种组合?**

选择看好并长期持仓的币种\
选择有波动性的币种\
选择价格回归型的币种\
选择波动率相近的币种\
选择非相同领域、属性相差大的币种\
持仓币种价值均匀分布的组合

**调仓周期或者调仓阈值设置多少合理？**

调仓周期或者调仓阈值需要根据交易手续费来制定。

小蚁的智能调仓机器人是完全免费的，交易所的现货交易手续费一般是0.1%（币安），

小蚁智能调仓到达条件后，只交易差额部分，所以调仓引起的交易量一般是持仓的一小部分。

传统金融调仓比例一般设置在5%-15%，加密货币波动性比较高，建设设置在10%-20%，

具体还得根据不同的资产属性来设置调仓比例。

**智能调仓参数配置说明**

小蚁的只能调仓机器人设置有新建仓位和使用原有仓位两种模式。\
我们先介绍新建仓位模式，选择这个种模式启动策略时，会按添加的资产分配比例建仓

分配方式，即用户把资产币种添加进来后，每种资产价值占总预计投入的比例。小蚁提供以下3种方式对每种资产占比分配：\
1、均分，按币种价值均等分配，适合波动率相近的资产组合。

2、市值，按每个币种的流通市值占所选币种流通市值总和的比例。

3、波动率，按每个币种的真实波幅（ATR）占所选币种真实波幅总和的比例。

调仓阈值：按最新市价其中至少一个资产的估值比例和其初始比例的差额达到此预设值即引起调仓动作以恢复到初始比例状态。默认调仓阈值为5%。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/10/%E4%BB%80%E9%BA%BC%E6%98%AF%E6%99%BA%E8%83%BD%E8%AA%BF%E5%80%89%E7%AD%96%E7%95%A52-461x1024.jpg" alt=""><figcaption></figcaption></figure>

原有仓位模式下，策略会主动读取用户在交易所的现货资产，小蚁固定只读取价值大于200USDT的资产，然后按价值占比显示比例。启动策略后会在原有的资产按设定的比例进行调仓，不会再次建仓。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/10/%E4%BB%80%E9%BA%BC%E6%98%AF%E6%99%BA%E8%83%BD%E8%AA%BF%E5%80%89%E7%AD%96%E7%95%A53.jpg" alt=""><figcaption></figcaption></figure>

**参考文献:**

[Portfolio Rebalancing in Theory and Practice — Vanguard](https://personal.vanguard.com/pdf/flgprtp.pdf)

[The Art of Rebalancing — SmithBarney Consulting Group](https://www.retailinvestor.org/pdf/SmithBarney.pdf)

[There is a Rebalancing Bonus (False) — Retail Investor](https://www.retailinvestor.org/why.html#bonus)

[#AntBot](https://www.antrade.io/guide/docs/cn/tag/antbot/)@AntBot free trading bot\
