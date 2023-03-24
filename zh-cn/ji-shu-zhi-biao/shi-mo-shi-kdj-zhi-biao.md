# 什么是KDJ指标？

[Skip to content](https://www.antrade.io/guide/docs/cn/kdj-indicator/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/cn/)[首页](https://www.antrade.io/guide/docs/cn/)[免费使用AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/cn)
* [技术指标](https://www.antrade.io/guide/docs/cn/indicator/)
* [进阶学习](https://www.antrade.io/guide/docs/cn/cn-learning/)
* [什么是KDJ指标？](https://www.antrade.io/guide/docs/cn/kdj-indicator/)

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

## 什么是KDJ指标？

4月 ago[AntBot](https://www.antrade.io/guide/docs/cn/author/antbot/)1 minute

**目录：**

* [**什么是KDJ指标？**](https://www.antrade.io/guide/docs/cn/kdj-indicator/#%E4%BB%80%E4%B9%88%E6%98%AFKDJ%E6%8C%87%E6%A0%87%EF%BC%9F)\

* [**计算**](https://www.antrade.io/guide/docs/cn/kdj-indicator/#%E8%AE%A1%E7%AE%97)\

* [**应用法则**](https://www.antrade.io/guide/docs/cn/kdj-indicator/#%E5%BA%94%E7%94%A8%E6%B3%95%E5%88%99)\

* [**KDJ的局限性**](https://www.antrade.io/guide/docs/cn/kdj-indicator/#KDJ%E7%9A%84%E5%B1%80%E9%99%90%E6%80%A7)

**什么是KDJ指标？**

KDJ 指标是一种**技术指标**，用于分析和预测交易资产中的**趋势**和**价格模式**的变化。它是一种非常实用的技术指标，最常用于**中短期**的市场趋势分析。

KDJ的计算依据是**最高价**、**最低价**和**收盘价**。当价格**上涨**时，**收盘价**倾向于接近当日价格区间的**上端**；相反，在**下降**趋势中**收盘价**趋向于接近当日价格区间的**下端**。它可以从其中反映价格波动的**强度**，**超买**和**超卖**现象，并在价格上涨或下跌前给出**交易信号**。

KDJ 是**随机震荡指标**的派生形式，唯一的区别是有一条**额外**的线，称为 **J 线**。

KDJ总共包含三条线，分别是**K线**、**D线**和**J线**。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/Picture1.png" alt=""><figcaption></figcaption></figure>

**计算**

KDJ是通过计算特定时期内发生的最高价、最低价和收盘价之间的比例关系来获得未成熟随机值（RSV），然后根据平滑移动平均线的方法来计算K值、D值和J值，并绘制成图来研究价格走势。以每日 KDJ 值的计算为例，具体计算方法如下。

1\. 计算某个时期的RSV值：

n天RSV=（Cn-Ln）÷（Hn-Ln）×100。

在这个公式中，Cn是第n天的收盘价；Ln是n天内的最低价；Hn是n天内的最高价。RSV值总是在1到100之间波动。

2\. 当日K值=2/3×前一日K值+1/3×当日RSV

3\. 当日D值=2/3×前一日D值+1/3×当日K值

4\. 当日J值=3×当日K值-2×当日D值

注意：如果前一天没有K值和D值，可以用50代替。

**应用法则**

* **超买和超卖**

KDJ的值从0到100不等（J值有时会超过）。K线是快速确认线一一数值在90以上为超买，数值在10以下为超卖；D线是慢速主干线一一数值在80以上为超买，数值在20以下为超卖。

* **金叉与死叉**

当K线在图形上突破D线时，俗称金叉，这是一种买入信号。此外，当K线和D线在20以下向上交叉时，此时的短期买入信号比较准确；如果K值在50以下，在D值之上交叉两次，形成较高的金叉 “W “形态，则股价可能有相当大的上涨，市场前景看好。

当K值越来越小，然后从上面跌破D线时，通常被称为死叉，被视为卖出信号。此外，当K线和D线在80关口交叉向下时，此时的短期卖出信号更为准确。如果K值在50以上，在趋势中两次穿越D线以下，并从低位死叉 “M “形态，市场前景可能会有相当大的股价下跌。

* **短期头部与短期底部**

J线是一条方向性的敏感线。当J值大于90时，特别是连续5天以上，价格至少会形成一个短期高峰。相反，当J值小于10时，特别是连续几天，价格至少会形成一个短期的底部。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/KDJ-1.jpg" alt=""><figcaption></figcaption></figure>

## **KDJ的局限性** <a href="#kdj-de-ju-xian-xing" id="kdj-de-ju-xian-xing"></a>

KDJ的主要局限性在于对价格变化很敏感，在非常动荡的市场下，它可能会因此产生错误的交易信号，导致价格不会跟随信号上涨或下跌，从而使得交易者产生错误判断。

技术指标自身具有局限性，运用技术指标判断市场走势本身具备很大的灵活性，因此，投资者在使用KDJ指标时，应结合自身的风险偏好以投资品种综合考量。

**参考文档：**

[https://www.tradingview.com/script/BNpuF7dG-KDJ-stochastic-indicator/](https://www.tradingview.com/script/BNpuF7dG-KDJ-stochastic-indicator/)

[#AntBot](https://www.antrade.io/guide/docs/cn/tag/antbot/)[#Indicator](https://www.antrade.io/guide/docs/cn/tag/indicator/)[#KDJ](https://www.antrade.io/guide/docs/cn/tag/kdj/)[#trading](https://www.antrade.io/guide/docs/cn/tag/trading/)@AntBot free trading bot\
