# 什么是R-Breaker交易策略?

[Skip to content](https://www.antrade.io/guide/docs/cn/r-breaker/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/cn/)[首页](https://www.antrade.io/guide/docs/cn/)[免费使用AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/cn)
* [策略学习](https://www.antrade.io/guide/docs/cn/cn-strategy/)
* [什么是R-Breaker交易策略?](https://www.antrade.io/guide/docs/cn/r-breaker/)

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

## 什么是R-Breaker交易策略?

4月 ago[AntBot](https://www.antrade.io/guide/docs/cn/author/antbot/)1 minute

**目录：**

* [**什么是R-Breaker交易策略？**](https://www.antrade.io/guide/docs/cn/r-breaker/#%E4%BB%80%E4%B9%88%E6%98%AFR-Breaker%E4%BA%A4%E6%98%93%E7%AD%96%E7%95%A5%EF%BC%9F)\

* [**阻力位与支撑位**](https://www.antrade.io/guide/docs/cn/r-breaker/#%E9%98%BB%E5%8A%9B%E4%BD%8D%E4%B8%8E%E6%94%AF%E6%92%91%E4%BD%8D)\

* [**策略逻辑解析**](https://www.antrade.io/guide/docs/cn/r-breaker/#%E7%AD%96%E7%95%A5%E9%80%BB%E8%BE%91%E8%A7%A3%E6%9E%90)\

* [**如何启动R-Breaker策略机器人？**](https://www.antrade.io/guide/docs/cn/r-breaker/#%E5%A6%82%E4%BD%95%E5%90%AF%E5%8A%A8R-Breaker%E7%AD%96%E7%95%A5%E6%9C%BA%E5%99%A8%E4%BA%BA%EF%BC%9F)\

* [**R-Breaker策略回测**](https://www.antrade.io/guide/docs/cn/r-breaker/#R-Breaker%E7%AD%96%E7%95%A5%E5%9B%9E%E6%B5%8B)\

* [**策略的优缺点**](https://www.antrade.io/guide/docs/cn/r-breaker/#%E7%AD%96%E7%95%A5%E7%9A%84%E4%BC%98%E7%BC%BA%E7%82%B9)

**什么是R-Breaker交易策略？**

R-Breaker策略由Richard Saidenberg开发，并于1994年公布于世。在之后连续十五年被美国《Futures Truth》杂志评选为前十大最赚钱的交易策略之一。与其他策略相比，R-Breaker是**趋势**与**反转**相结合的交易策略。不仅可以**捕捉趋势行情**获得大利润，还可以在行情反转的时候，及时**主动止盈**并**顺势反手**。

R-Breaker主要分为分为**反转**和**趋势**两部分。**空仓**时进行**趋势跟随**，**持仓**时等待反转信号**反向开仓**。

**阻力位与支撑位**

简单的说，R-Breaker策略就是一个支撑位和阻力位策略，它根据昨日的最高价、最低价和收盘价，计算出七个价格：一个中心价位(pivot)、三个支撑位(s1、s2、s3)、三个阻力位(r1、r2、r3)。然后根据当前价格与这些支撑位和阻力位的位置关系，以形成买卖的触发条件，并且通过一定的算法调整，调节这七个价格之间的距离，进一步改变交易的触发值。

| 指标计算方法                      |
| --------------------------- |
| 突破买入价(阻力位r3) = H + 2P -2L   |
| 观察卖出价(阻力位r2) = P + H – L    |
| 反转卖出价(阻力位r1)= 2P – L        |
| 中心价位(pivot) = （H + C + L）/3 |
| 反转买入价(支撑位s1) = 2P – H       |
| 观察买入价(支撑位s2) = P – (H – L)  |
| 突破卖出价(支撑位s3) = L – 2(H – P) |

由此我们可以看到，R-Breaker策略是根据昨天的价格绘制了一个类似网格的价格线，并且每天更新一次这些价格线。在技术分析上有支撑位和阻力位，并且两者的作用可以互相转换。当价格成功向上突破阻力位时，阻力位变成了支撑位；当价格成功向下突破支撑位时，支撑位变成了阻力位。

在实际交易中，这些支撑位和阻力位为交易者指出了开平仓方向和精确等买卖点位。交易者可以根据盘中价格、中心价、阻力位、支撑位灵活定制具体的开平仓条件，也可以根据这些网格价格线进行加减仓。

**策略逻辑解析**

接下来，让我们看一下R-Breaker策略是怎样利用这些支撑位和阻力位的。

如果当前没有持仓就进入趋势模式，当价格大于突破买入价就开仓做多；当价格小于突破卖出价就开仓做空。

* 趋势模式
  * 多头开仓：如果无持仓，并且价格大于突破买入价。
  * 空头开仓：如果无持仓，并且价格小于突破卖出价。
  * 多头平仓：如果持多单，并且当日最高价大于观察卖出价，并且价格小于反转卖出价。
  * 空头平仓：如果持空单，并且当日最低价小于观察买入价，并且价格大于反转买入价。

如果有持仓时就进入反转模式，当持有多单时，并且当日最高价大于观察卖出价，并且价格跌破反转卖出价就平掉多头持仓反手做空。当持有空单时，并当日最低价小于观察买入价，并且价格突破反转买入价就平掉空头持仓反手做多。

* 反转模式
  * 多头开仓：如果持空单，并且当日最低价小于观察买入价，并且价格大于反转买入价。
  * 空头开仓：如果持多单，并且当日最高价大于观察卖出价，并且价格小于反转卖出价。
  * 多头平仓：如果持多单，并且价格小于突破卖出价。
  * 空头平仓：如果持空单，并且价格大于突破买入价。

如下图所示：\


<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/attach_16417be280731bd9.png" alt=""><figcaption></figcaption></figure>

首先看一下这6个价格与前一日价格之间的关系。

* 反转卖出价和反转买入价\
  根据公式推导，发现这两个价格和前一日最高最低价没有确定的大小关系。
* 观察卖出价和观察买入价\
  用观察卖出价 – 前一交易日最高价发现，(H+P-L)-H = P – L >0,说明观察卖出价>前一交易日最高价；同理可证，观察买入价<前一交易日最低价。
* 突破买入价和突破卖出价\
  突破买入价>观察卖出价>前一交易日最高价，可以说明突破买入价>>前一交易日最高价。做差后可以发现，突破买入价 – 前一交易日最高价 = 2\[(C-L)+(H-L)]/3。

用K线形态表示：

前一交易日K线越长，下影线越长，突破买入价越高。\
前一交易日K线越长，上影线越长，突破卖入价越高。

这样一来就可以解释R-Breaker背后的逻辑了。

当今日的价格突破前一交易日的最高点，从形态上来看会是上涨趋势，具备一定的开多仓条件，但光凭这个条件还不够充分。若前一交易日的下影线越长，说明多空方博弈激烈，多方力量强大。因此可以设置更高的突破买入价，一旦突破说明多方力量稳稳地占据了上风，那么就有理由相信未来会继续上涨。同理可解释突破卖出价背后的逻辑。

* 持有多仓时，若标的价格持续走高，则在当天收盘之前平仓获利离场。若价格不升反降，跌破观察卖出价时，此时价格仍处于前一交易日最高价之上，继续观望。若继续下跌，直到跌破反转卖出价时，平仓止损。
* 持有空仓时，若标的价格持续走低，则在当天收盘之前平仓获利离场。若价格不降反升，升至观察买入价时，此时价格仍处于前一交易日最低价之下，继续观望。若继续上涨，直到升至反转买入价时，平仓止损。

下图是TradingView平台下的R-Breaker策略形态

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/1668482276769.png" alt=""><figcaption></figcaption></figure>

**如何启动R-Breaker策略机器人？**

1\. 登录AntBot账号，在【交易】界面的【机器人】里找到【R-Breaker】。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/12/1.jpg" alt=""><figcaption></figcaption></figure>

2\. 点击【运行】按钮，进入参数设置页面。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/12/2.jpg" alt=""><figcaption></figcaption></figure>

3\. 根据个人标准和偏好选择币种。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/12/3.jpg" alt=""><figcaption></figcaption></figure>

4\. 填入【首张单数】。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/12/4.jpg" alt=""><figcaption></figcaption></figure>

* 【首张单数】机器人从未持仓状态下首次开仓时的持仓量。建议初学者保持默认值。

5\. 设置【杠杆率 】【最大单数】 以及【运行方式】。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/12/5.jpg" alt=""><figcaption></figcaption></figure>

* 【杠杆率】：加杠杆可以当做向交易所借入资金去持仓，这份持仓资金相对于本金的倍数即为杠杆率，加杠杆会放大盈亏。建议初学者保持5倍杠杆率的默认值。
* 【最大单数】：机器人从没有持仓开始允许连续加仓的最大次数。
* 【运行方式】：分为循环运行和单次运行。循环运行是指每次止盈平仓后机器人会重复下一轮开仓，机器人只会在达到止盈比例或止损比例后才会停止。单次运行是指机器人在完成一次全仓止盈后将自动终止运行。

6\. 选择【开单方向】。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/12/6.jpg" alt=""><figcaption></figcaption></figure>

* 【自动】：机器人会根据策略信号自动变更多空头寸开单。
* 【只多】：机器人只接收多头信号开单。
* 【只空】：机器人只接收空头信号开单。

7\. 设置【止盈比例】与 【止损比例】。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/12/7.jpg" alt=""><figcaption></figcaption></figure>

* 【止盈比例】

1、默认【系统追踪】值，机器人每间隔30分钟计算策略信号。当信号反转时将会平仓止盈，机器人进入下一循环。\
2、如有预设比例值，机器人持仓收益率达到此预设值将会平仓止盈，机器人进入下一循环。

* 【止损比例】

1、默认【系统追踪】值，机器人在建仓时会根据30分钟周期的价格真实波动预埋止损比例，当持仓亏损率达到此预设值将会平仓止损，机器人进入下一循环。\
2、如有预设比例值，机器人持仓亏损率达到此预设值将会平仓止损，机器人进入下一循环。

8\. 点击【启动】即可成功创建R-Breaker机器人。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/12/8.jpg" alt=""><figcaption></figcaption></figure>

**R-Breaker策略回测**

周期 – 30分钟线\
起始金额$1000，每次进场交易金额为100%cash\
交易时间：2022/1/1\~2022/10/1\
标的：ETHUSDTPERP\
交易手续费：0.04%

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/1668482199318.png" alt=""><figcaption></figcaption></figure>

**策略的优缺点**

优点：

1、在市场处于盘整期时，过滤掉一些小幅波动，即在观察买入价和观察卖出价之间波动时不轻易进场。

2、观察买入价与观察卖出价之间的距离会随着波动变化。如果连续几天盘整波动缩小，R-Breaker的六个价位之间的距离也会跟着缩小。当盘整突破时，会发出进场信号，抢夺优势点位。

3、R-Breaker由趋势和反手两个子策略组合而成，容易掌握盘势的平衡。例如趋势策略回档时，反手策略可以先平仓守住获利，甚至反手开仓抓逆势行情。

缺点：

1、在一段时间急涨急跌的行情中，比较容易触发六个价位，止损频繁。

2、在长期盘整期间，需要加上过滤条件控制六价位之间的距离不要过小，避免频繁开仓。

3、需添加一段时间内过度频繁交易的机制。比如前一日波动幅度较小，造成六价位距离较近，次日价位上下冲击严重，也会造成频繁开平仓。

**参考文档**:

[https://medium.com/@FMZ\_Quant/commodity-futures-r-breaker-strategy-f9275c360aa](https://medium.com/@FMZ\_Quant/commodity-futures-r-breaker-strategy-f9275c360aa)

[https://www.myquant.cn/docs/python\_strategyies/425](https://www.myquant.cn/docs/python\_strategyies/425)

[https://www.tradingview.com/script/fYqAT2ys-blackcat-L2-Intraday-R-Breaker-Indicator/](https://www.tradingview.com/script/fYqAT2ys-blackcat-L2-Intraday-R-Breaker-Indicator/)

[#AntBot](https://www.antrade.io/guide/docs/cn/tag/antbot/)[#bot](https://www.antrade.io/guide/docs/cn/tag/bot/)[#R-Breaker](https://www.antrade.io/guide/docs/cn/tag/r-breaker/)[#strategy](https://www.antrade.io/guide/docs/cn/tag/strategy/)[#trading](https://www.antrade.io/guide/docs/cn/tag/trading/)@AntBot free trading bot\
