# 什么是动量交易策略？

[Skip to content](https://www.antrade.io/guide/docs/cn/strategy-momentum/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/cn/)[首页](https://www.antrade.io/guide/docs/cn/)[免费使用AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/cn)
* [策略学习](https://www.antrade.io/guide/docs/cn/cn-strategy/)
* [什么是动量交易策略？](https://www.antrade.io/guide/docs/cn/strategy-momentum/)

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

## 什么是动量交易策略？

3月 ago[AntBot](https://www.antrade.io/guide/docs/cn/author/antbot/)1 minute

**什么是动量交易策略？**

AntBot的动量策略是一种分析价格惯性作用捕获交易优势的趋势交易策略。通过计算价格波动的速度，得出价格进入强势的高峰和转入弱势的低谷等信号。**动量策略是投资界当之无愧最流行的策略之一**了，当下在期货的 CTA 策略中绝大多数都是动量策略。

**动量策略为什么有效呢**？

**动量效应是动量策略的基础**。**动量效应(Momentum Effect)又称”惯性效应”**，指**资产价格具有延续原来运动方向的趋势**，也就是说，过去一段时间收益较高的资产在未来仍将会获得较高的收益，因此**投资者可以通过购买历史表现好的资产、卖出表现差的资产，获得低成本的超额收益**。

**AntBot动量策略实现原理**

**AntBot通过线性回归建模实现对期货价格动量绘制得到动量强弱判断价格大概率走势**。线性回归是一种成熟的统计技术，可轻松应用于软件和计算。企业可使用线性回归以可靠和可预测的方式将原始数据转换为商业智能和切实可行的见解。许多领域（包括生物学以及行为、环境和社会科学）的科学家都使用线性回归进行初步数据分析并预测未来趋势。许多数据科学方法（例如机器学习和人工智能）都使用线性回归来解决复杂问题。

**动量策略风险**

1、AntBot的动量策略对行情实时监控在进入横盘阶段时主动减少趋势策略的开单数量，会导致机器人需要漫长的入场等待，对交易者要求有足够的耐心。

2、在极端不利的行情下，比如在价格波动频率高，波动幅度大，会导致账户出现持续亏损的情况。AntBot的动量策略默认内置2个平均波幅实时跟踪止损规避风险，交易者可以根据自己的资金情况，适度减少开单额度，等待行情回暖再恢复开单额度。\


**动量策略回测结果与稳健性分析**

周期：120分钟线\
入场金额：$1000，每次进场交易金额为100%cash\
交易时间：2022/1/1\~2022/12/23\
标的：ETHUSDTPER\
手续费：0.04%

<figure><img src="https://www.antrade.io/guide/docs/cn/wp-content/uploads/2022/12/1671787697919.png" alt=""><figcaption></figcaption></figure>

**如何开启动量策略机器人**

@AntBot free trading bot\
