# 什么是智能马丁交易策略？

[Skip to content](https://www.antrade.io/guide/docs/cn/cn\_strategy\_dca/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/cn/)[首页](https://www.antrade.io/guide/docs/cn/)[免费使用AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/cn)
* [策略学习](https://www.antrade.io/guide/docs/cn/cn-strategy/)
* [什么是智能马丁交易策略？](https://www.antrade.io/guide/docs/cn/cn\_strategy\_dca/)

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

## 什么是智能马丁交易策略？

6月 ago[AntBot](https://www.antrade.io/guide/docs/cn/author/antbot/)1 minute

**马丁格尔策略盈利原理**

马丁格尔交易策略是一种平均成本法交易策略，它简单易懂，类似定投的逻辑，适合新手的使用的策略，在下跌中不断倍投加仓拉低均价，价格反弹中可以比普通的定投更快速回本。

马丁格尔交易原理示意图：

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/09/%E4%BB%80%E9%BA%BC%E6%98%AF%E9%A6%AC%E4%B8%81%E6%A0%BC%E7%88%BE%E4%BA%A4%E6%98%93%E7%AD%96%E7%95%A5%EF%BC%9F.png" alt=""><figcaption></figcaption></figure>

机器人参数设定：\
头寸翻倍增加会越来越大，风险也随之加大，严格来说马丁格尔是一种仓位管理方法，要使用马丁格尔策略，一定要解决三个问题：

1、首单额度\
2、加仓倍数\
3、加仓距离

加仓倍数小蚁app里默认设定是2倍，目的在是头寸规模比较小的前几单补仓能最大幅度压低仓位浮亏比例，实现尽早止盈平仓。\
首单额度根据每个用户自身的本金而定，小蚁根据每种加密货币近期行情波动大小制定最大可以加仓幅度，根据这个幅度和7次补仓次数再确定每笔加仓距离，充分考虑每种资产的风险情况，根据波动风险，再合理分配资金，提高每笔资金的利用率。

手动机器人参数设定：

如果你是合约马丁，为了减少风险，强烈建议你开启趋势补仓功能，趋势补仓能帮你在持续单边行情中暂停补仓，直到多空力量再度僵持才恢复补仓功能。

#### 什么是双向马丁 <a href="#8zyera" id="8zyera"></a>

简单说就是同时做多跟做空，多空同时持仓。

假设价格往下跌，多单会继续持仓并且跌幅在达到设定比例时进行补仓，那么空单在跌幅达到设定比例时会止盈获利，\
反之，假设价格往上涨，空单会继续持仓并且在涨幅达到设定比例时进行补仓，那么多单在涨幅达到设定比例时会止盈获利。

这个种双向持仓做法，规避了单向马丁在单边行情下，账户长时间扛浮亏没有利润产出的缺点，双向持仓情况下一边被套，另外一边震荡时，一定会持续盈利的。这样大大提高了资金利用率。

可以说双向马丁把回归型策略发挥到了极致。

#### 智能分仓有什么作用？ <a href="#6jxe6b" id="6jxe6b"></a>

智能分仓（又名网格止盈，尾单止盈）

尾单止盈是相对整仓止盈而言的，整仓止盈就是当前价格达到预定的止盈比例，整体清仓卖出止盈。\
智能分仓是对尾单止盈的进一步优化，在系统持仓达到预计总持仓的25%，并且价格上涨达到最后一单持仓的止盈点就触发尾单卖出盈利。

#### 智能分仓利与弊 <a href="#g1hgrh" id="g1hgrh"></a>

开启智能分仓后，即使当前价格没有达到策略整体止盈点位，也可收单获利，特别适用于半边行情后，长时间停留在整盘的阶段。

若价格在尾单点位附近震荡，则可能进行尾单建仓、尾单止盈、尾单建仓、尾单止盈…，在震荡行情中不断获利。

但开启智能分仓后，当价格达快速回归到整体止盈点，此时分仓策略收益要比整体止盈低；另外尾单被止盈后，持仓均价上升，整体止盈点位上移，距离当前价格较远，影响整体止盈周期。

你可以根据当前行情和自身需求，选择是否开启智能分仓策略。

**智能补仓有什么作用？**

正常情况下，价格跌幅达到预设比例后，系统就会正常补仓，开启智能补仓开关后，当前持仓超过预定总投入的25%时系统不会马上进行补仓行为，需要等待4小时周期的MACD指标恢复到多空力量持平或逆转时才进行补仓。

#### 智能补仓的利与弊 <a href="#5h212j" id="5h212j"></a>

智能补仓设定的目的是规避持续单边行情过早补仓，智能补仓可以进一步拉低持仓均价，防止重仓在高位。\
特别是对合约策略，高杠杆情况下，价格高位持续补仓，如遇到持续下行行情，大大加重爆仓风险。

当然风险和收益总是成正比，开启智能补仓会错过下行后回调的行情。小蚁是一款策略工具，怎么发挥他的最大效用，还得看个人怎么使用。

@AntBot free trading bot\
