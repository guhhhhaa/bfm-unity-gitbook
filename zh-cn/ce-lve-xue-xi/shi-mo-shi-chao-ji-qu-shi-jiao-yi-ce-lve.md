# 什么是超级趋势交易策略？

[Skip to content](https://www.antrade.io/guide/docs/cn/supertrend/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/cn/)[首页](https://www.antrade.io/guide/docs/cn/)[免费使用AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/cn)
* [策略学习](https://www.antrade.io/guide/docs/cn/cn-strategy/)
* [什么是超级趋势交易策略？](https://www.antrade.io/guide/docs/cn/supertrend/)

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

## 什么是超级趋势交易策略？

4月 ago[AntBot](https://www.antrade.io/guide/docs/cn/author/antbot/)1 minute

**目录:**

* [**什么是超级趋势交易策略？**](https://www.antrade.io/guide/docs/cn/supertrend/#%E4%BB%80%E4%B9%88%E6%98%AFSuperTrend%E4%BA%A4%E6%98%93%E7%AD%96%E7%95%A5%EF%BC%9F)\

* [**ATR指标的计算方法**](https://www.antrade.io/guide/docs/cn/supertrend/#ATR%E6%8C%87%E6%A0%87%E7%9A%84%E8%AE%A1%E7%AE%97%E6%96%B9%E6%B3%95)\

* [**超级趋势策略的计算公式**](https://www.antrade.io/guide/docs/cn/supertrend/#SuperTrend%20%E7%AD%96%E7%95%A5%E7%9A%84%E8%AE%A1%E7%AE%97%E5%85%AC%E5%BC%8F)\

* [**如何启动超级趋势策略机器人？**](https://www.antrade.io/guide/docs/cn/supertrend/#%E5%A6%82%E4%BD%95%E5%90%AF%E5%8A%A8SuperTrend%E7%AD%96%E7%95%A5%E6%9C%BA%E5%99%A8%E4%BA%BA%EF%BC%9F)\

* [**超级趋势策略的优势和风险**](https://www.antrade.io/guide/docs/cn/supertrend/#SuperTrend%E7%AD%96%E7%95%A5%E7%9A%84%E4%BC%98%E5%8A%BF%E5%92%8C%E9%A3%8E%E9%99%A9)\

* [**对超级趋势策略的优化**](https://www.antrade.io/guide/docs/cn/supertrend/#%E5%AF%B9SuperTrend%E7%AD%96%E7%95%A5%E7%9A%84%E4%BC%98%E5%8C%96)\

* [**超级趋势的策略回测**](https://www.antrade.io/guide/docs/cn/supertrend/#SuperTrend%E7%AD%96%E7%95%A5%E5%9B%9E%E6%B5%8B)

**什么是SuperTrend交易策略？**

超级趋势交易策略是基于**超级趋势技术指标**的交易策略，该指标是一款基于**真实波动幅度均值（ATR）**N倍的趋势**自动跟踪止损型**(Trailing Stop)指标，直观提供**买入卖出**信号的趋势指标。ATR通道突破，定义了中轨(hl/2)、上轨(hl/2 + N\*ATR(M))和下轨(hl/2 – N\*ATR(M))，如收盘价**跌破下轨**则趋势转为向下，则**做空**；如收盘价**突破上轨**则趋势转为向上，则**做多**。

**ATR指标的计算方法**

ATR（平均真实波幅）衡量的是在过去一段时间内价格的波动幅度大小，以平均值作为结果。而这里的幅度大小则是以下面三者中的最大者为准：

1.当天最高点和最低点间的距离\
2.前一天收盘价和当天最高价间的距离\
3.前一天收盘价和当天最低价间的距离

**超级趋势策略的计算公式：**

在做多时：

超级趋势 =（最高价+最低价）/2 – N\*ATR(M)

在作图中，这个值只上移不下移，就是取近期的最高值。

在做空时：

超级趋势 = （最高价+最低价）/2 + N\*ATR(M)

其中N = 3 ， M = 10

**如何启动超级趋势策略机器人？**

1\. 登录AntBot账号，在【交易】界面的【机器人】里找到【超级趋势机器人】。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/1-2.jpg" alt=""><figcaption></figcaption></figure>

2\. 点击【运行】按钮，进入参数设置页面。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/2-2.jpg" alt=""><figcaption></figcaption></figure>

3\. 根据个人标准和偏好选择币种。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/3-2.jpg" alt=""><figcaption></figcaption></figure>

4\. 设置【首张单数】。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/4-2.jpg" alt=""><figcaption></figcaption></figure>

* 【首单张数】：机器人在空仓状态下开仓的第一笔仓位大小。建议初学者保持默认值。

5\. 设置【运行方式】。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/5-2.jpg" alt=""><figcaption></figcaption></figure>

* 【运行方式】：分为循环运行和单次运行。循环运行是指每次止盈平仓后机器人会重复下一轮开仓，机器人只会在达到『其他设置』里的止盈或者止损里所预设的盈亏条件后才会停止。单次运行是指机器人在完成一次全仓止盈后将自动终止运行。

6\. 选择【自动】，【只多】或者【只空】。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/6-2.jpg" alt=""><figcaption></figcaption></figure>

* 【自动】：根据交易信号，发布多仓信号时做多，发布空仓信号时做空。
* 【只多】：只运行多仓信号。
* 【只空】：只运行空仓信号。

7\. 设置【杠杆率】。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/7-2.jpg" alt=""><figcaption></figcaption></figure>

* 【杠杆率】：加杠杆可以当做向交易所借入资金去持仓，这个份持仓资金相对于本金的倍数即为杠杆率，加杠杆会放大盈亏，杠杆率越大放大作用越大。建议初学者保持5倍杠杆率的默认值。

8\. 自行选填【其他设置】里的【止盈】和【止损】。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/8-2.jpg" alt=""><figcaption></figcaption></figure>

* 【止盈】：
  * 按比例止盈：浮盈比例＞该预设比例时，机器人将会自动清仓并停止运行。
  * 按金额止盈：实现盈亏+浮动盈亏>该预设金额时，机器人将会自动清仓并停止运行。
* 【止损】：
  * 按比例止损：浮亏比例>该预设比例时，机器人将会自动清仓并停止运行。
  * 按金额止损：浮亏金额>该预设金额时，机器人将会自动清仓并停止运行。

9\. 点击【启动】即可成功SuperTrend机器人

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/9-1.jpg" alt=""><figcaption></figcaption></figure>

**超级趋势策略的优势和风险**\
超级趋势具有非常好的趋势跟踪性，但是信号过少，交易不够灵活。我们在原策略的基础上加入类轨道算法和移动出场，适用于30分钟周期或日线以下周期，适用于小资金跑，该策略无未来函数无偷价问题。

**对超级趋势策略的优化**

经典的超级趋势策略面对缓慢持续单边行情，会无法感知价格突破信号导致账户持续亏损，对交易员的心理负担比较大。AntBot对超级趋势策略的每笔订单记录了开仓价格，当价格持续单边到达3倍ATR的幅度，将会平仓止损。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/1668150086539.png" alt=""><figcaption></figcaption></figure>

**超级趋势策略回测**

周期 – 30分钟线\
参数 – ATR M=10, N = 3\
上升趋势做多，跌破则出场; 只做多单；\
起始金额$1000，每次进场交易金额为100%cash;\
交易时间: 2022/1/1\~2022/10/1\
标的：ETHUSDTPERP\
手续费：0.04%

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/1668150004677.png" alt=""><figcaption></figcaption></figure>

**参考文档：**

[https://fintastic.trading/wisdom\_box/supertrend-指標](https://fintastic.trading/wisdom\_box/supertrend-%E6%8C%87%E6%A8%99)

[https://elearnmarkets.com/blog/supertrend-indicator-strategy-trading](https://elearnmarkets.com/blog/supertrend-indicator-strategy-trading)

[https://www.tradingview.com/script/r6dAP7yi/](https://www.tradingview.com/script/r6dAP7yi/)

[#AntBot](https://www.antrade.io/guide/docs/cn/tag/antbot/)[#bot](https://www.antrade.io/guide/docs/cn/tag/bot/)[#strategy](https://www.antrade.io/guide/docs/cn/tag/strategy/)[#SuperTrend](https://www.antrade.io/guide/docs/cn/tag/supertrend/)[#trading](https://www.antrade.io/guide/docs/cn/tag/trading/)[#trend-following](https://www.antrade.io/guide/docs/cn/tag/trend-following/)@AntBot free trading bot\
