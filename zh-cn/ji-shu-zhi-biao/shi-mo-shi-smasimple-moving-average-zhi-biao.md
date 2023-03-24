# 什么是SMA(Simple Moving Average)指标？

[Skip to content](https://www.antrade.io/guide/docs/cn/ma-indicator/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/cn/)[首页](https://www.antrade.io/guide/docs/cn/)[免费使用AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/cn)
* [技术指标](https://www.antrade.io/guide/docs/cn/indicator/)
* [进阶学习](https://www.antrade.io/guide/docs/cn/cn-learning/)
* [什么是SMA(Simple Moving Average)指标？](https://www.antrade.io/guide/docs/cn/ma-indicator/)

Search for:

技术指标

*
  * [支撑和阻力原理详解](https://www.antrade.io/guide/docs/cn/support-resistance/)
  * [什么叫阴包阳形态？](https://www.antrade.io/guide/docs/cn/engulfing-bearish-patterns/)
  * [什么叫阳包阴形态？](https://www.antrade.io/guide/docs/cn/engulfing-bullish-patterns/)
  * [什么叫三只乌鸦形态？](https://www.antrade.io/guide/docs/cn/three-black-crows-patterns/)
  * [什么叫锤子线形态？](https://www.antrade.io/guide/docs/cn/long-lower-shadow-patterns/)
  * [什么叫倒锤子线形态？](https://www.antrade.io/guide/docs/cn/long-upper-shadow-patterns/)
  * [什么是BBW(Bollinger Bands Width)指标？](https://www.antrade.io/guide/docs/cn/bbw-indicator/)
  * [什么是RSI(Relative Strength Index)指标?](https://www.antrade.io/guide/docs/cn/rsi-indicator/)
  * [什么是SMA(Simple Moving Average)指标？](https://www.antrade.io/guide/docs/cn/ma-indicator/)
  * [什么是KDJ指标？](https://www.antrade.io/guide/docs/cn/kdj-indicator/)
  * [什么是MACD指标?](https://www.antrade.io/guide/docs/cn/macd-indicator/)

## 什么是SMA(Simple Moving Average)指标？

4月 ago[AntBot](https://www.antrade.io/guide/docs/cn/author/antbot/)1 minute

**目录：**

* [**什么是SMA指标？**](https://www.antrade.io/guide/docs/cn/ma-indicator/#%E4%BB%80%E4%B9%88%E6%98%AFSMA%E6%8C%87%E6%A0%87%EF%BC%9F)\

* [**计算**](https://www.antrade.io/guide/docs/cn/ma-indicator/#%E8%AE%A1%E7%AE%97)\

* [**应用法则**](https://www.antrade.io/guide/docs/cn/ma-indicator/#%E5%BA%94%E7%94%A8%E6%B3%95%E5%88%99)\

* [**总结**](https://www.antrade.io/guide/docs/cn/ma-indicator/#%E6%80%BB%E7%BB%93)

**什么是SMA指标？**

移动平均线是**技术分析**的**核心指标**之一，有各种不同的版本。简单移动平均线（Simple Moving Average，简称SMA) 是最简单的也是最容易构建的移动平均线。它根据该范围内的**周期数**计算**选定价格**范围（通常是收盘价）的**平均值**，是通过添加最近的数据点集，然后将总数除以时间段的数量而得到的。均线之所以被称为 “移动”，是因为它被逐条绘制在图表上，形成一条线，随着平均值的变化沿图表移动。

简单移动平均线（SMA）是一个**滞后指标**，因为它是基于特定时期的过去价格数据，可以使用这一指标来帮助确定资产的**买入**、**卖出**信号，也有助于确定**支撑**和**阻力区**。

**计算**\
简单移动平均线（SMA）是一种非加权的移动平均线。这意味着数据集中的每一天都具有同等的重要性，并被赋予同等的权重。当每一个新的一天结束时，最古老的数据点被删除，最新的数据点会被添加到开头。

以3周期SMA的计算为例:

周期值之和/周期数：3\
收盘价：5, 6, 7, 8, 9\
3周期均线的第一天SMA：（5+6+7）/3=6\
3周期均线的第二天SMA：（6+7+8）/3=7\
3周期期均线的第三天SMA：（7+8+9）/3=8

基本上，时间框架较短的简单移动平均线倾向于贴近当前的价格水平，减少滞后性，并会在价格移动后立即移动。较长的时间框架有更多繁琐的数据，其移动会更明显地滞后于市场的移动,越能反映长期的整体价格趋势。通常情况下，任何低于20天的时间段都被认为是短期的，任何在20至60天之间的时间段都是中期的，当然任何超过60天的时间段都会被视为长期的。投资者可根据自身交易策略所聚焦的时间周期来选择不同的移动平均线。

**应用法则**

使用简单移动平均线来确认价格的趋势，确实是使用该指标的最基本但又最有效的方法之一。

**1. 一般的经验法则如下:**

* 长期简单移动平均线明显处于上升趋势是对看涨趋势的确认。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/%E7%9C%8B%E6%B6%A8.jpg" alt=""><figcaption></figcaption></figure>

* 长期简单移动平均线明显处于下行状态是对看跌趋势的确认。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/%E7%9C%8B%E8%B7%8C.jpg" alt=""><figcaption></figcaption></figure>

注意：由于在计算长期移动平均线时考虑了大量的数据，需要市场上有相当多的运动才能导致SMA改变其方向。在整体趋势方面，长期移动平均线不太容易受到价格快速变化的影响。

**2. 支撑和阻力**\
简单移动平均线的另一个相当基本的用途是识别支撑和阻力区域。一般来说，简单移动平均线可以在上升趋势中提供支撑，也可以在下降趋势中提供阻力。虽然这在短期内（20天或更短）是可行的，但在长期情况下，简单移动平均线所提供的支撑和阻力会变得更加明显。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/%E6%94%AF%E6%92%91.jpg" alt=""><figcaption></figcaption></figure>

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/%E9%98%BB%E5%8A%9B.jpg" alt=""><figcaption></figcaption></figure>

**3. 金叉与死叉**

交叉交易需要在同一图表上使用两条不同期限的简单移动平均线。当较短期的SMA在较长期的SMA之上或之下交叉时，就会出现信号或潜在的交易机会。

* 看涨交叉 – 当短期SMA在长期SMA上方时发生交叉。也被称为金叉。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/%E9%87%91%E5%8F%891-1.jpg" alt=""><figcaption></figcaption></figure>

* 看跌交叉 – 当短期SMA在长期SMA下方时发生交叉。也被称为死叉。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/%E6%AD%BB%E5%8F%89.jpg" alt=""><figcaption></figcaption></figure>

**4. 价格交叉点**\
如果你采用两条SMA的设置，并加入价格这一第三要素，就会出现另一种类型的设置，称为价格交叉。我们使用50天SMA和200天SMA为例。

* 看涨的价格交叉：价格在50SMA上方交叉，而50SMA在200SMA上方。200SMA正在确认这一趋势。价格和短期SMA产生的信号与趋势方向一致。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/%E9%87%91%E5%8F%892.jpg" alt=""><figcaption></figcaption></figure>

* 看跌的价格交叉：价格在50SMA下方交叉，而50SMA在200SMA下方。200SMA正在确认这一趋势。价格和短期SMA产生的信号与趋势方向一致。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/%E6%AD%BB%E5%8F%892.jpg" alt=""><figcaption></figcaption></figure>

**总结**

SMA（Simple Moving Average）作为衡量主力成本重要的参照指标，用以观察价格变动趋势和起到测试压力和支撑的作用。当作为趋势判断的时候，周期越长越有效。另一方面，需要注意的是，当SMA形成多头排列后，短期SMA才是作为持仓的依据。

交易者必须要认识到这些信号的内在缺陷。这是一个由滞后指标所发出的信号组合而成的系统。只对已经发生的事情做出反应，并不是为了进行预测。像这样的系统肯定是在非常强劲的趋势中效果最好。在强势趋势中，这个系统或类似的系统实际上是相当有价值的。

在使用简单移动平均线时应该小心谨慎（就像使用任何指标一样）。毋庸置疑，它们是趋势识别器，它们能做的就像其他许多经受住时间考验的指标一样，为交易策略或系统提供一个额外的信心水平。当与更积极的指标一起使用时，至少可以确定，你在长期趋势方面正在寻找正确的交易方向。

**参考文档：**

[https://www.tradingview.com/chart/?solution=43000502589](https://www.tradingview.com/chart/?solution=43000502589)

[#AntBot](https://www.antrade.io/guide/docs/cn/tag/antbot/)[#Indicator](https://www.antrade.io/guide/docs/cn/tag/indicator/)[#Simple Moving Average](https://www.antrade.io/guide/docs/cn/tag/simple-moving-average/)[#SMA](https://www.antrade.io/guide/docs/cn/tag/sma/)[#trading](https://www.antrade.io/guide/docs/cn/tag/trading/)@AntBot free trading bot\
