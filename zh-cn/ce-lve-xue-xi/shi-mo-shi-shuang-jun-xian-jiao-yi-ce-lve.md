# 什么是双均线交易策略?

[Skip to content](https://www.antrade.io/guide/docs/cn/d-kama/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/cn/)[首页](https://www.antrade.io/guide/docs/cn/)[免费使用AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/cn)
* [策略学习](https://www.antrade.io/guide/docs/cn/cn-strategy/)
* [什么是双均线交易策略?](https://www.antrade.io/guide/docs/cn/d-kama/)

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

## 什么是双均线交易策略?

4月 ago[AntBot](https://www.antrade.io/guide/docs/cn/author/antbot/)1 minute

**目录：**

* [**双均线策略原理**](https://www.antrade.io/guide/docs/cn/d-kama/#%E5%8F%8C%E5%9D%87%E7%BA%BF%E7%AD%96%E7%95%A5%E5%8E%9F%E7%90%86)\

* [**均线策略为什么有效？**](https://www.antrade.io/guide/docs/cn/d-kama/#%E5%9D%87%E7%BA%BF%E7%AD%96%E7%95%A5%E4%B8%BA%E4%BB%80%E4%B9%88%E6%9C%89%E6%95%88%EF%BC%9F)\

* [**均线策略的缺陷**](https://www.antrade.io/guide/docs/cn/d-kama/#%E5%9D%87%E7%BA%BF%E7%AD%96%E7%95%A5%E7%9A%84%E7%BC%BA%E9%99%B7)\

* [**卡夫曼自适应移动均线对双均线策略的改进**](http://ka/#MA-%E5%8D%A1%E5%A4%AB%E6%9B%BC%E8%87%AA%E9%80%82%E5%BA%94%E7%A7%BB%E5%8A%A8%E5%9D%87%E7%BA%BF%E5%AF%B9%E5%8F%8C%E5%9D%87%E7%BA%BF%E7%AD%96%E7%95%A5%E7%9A%84%E6%94%B9%E8%BF%9B)\

* [**双均线趋势策略逻辑**](https://www.antrade.io/guide/docs/cn/d-kama/#D-KAMA%E8%B6%8B%E5%8A%BF%E7%AD%96%E7%95%A5%E9%80%BB%E8%BE%91)\

* [**如何启动双均线策略机器人？**](https://www.antrade.io/guide/docs/cn/d-kama/#%E5%A6%82%E4%BD%95%E5%90%AF%E5%8A%A8D-KAMA%E7%AD%96%E7%95%A5%E6%9C%BA%E5%99%A8%E4%BA%BA%EF%BC%9F)\

* [**TradingView展示的可视化的双均线策略**\
  ](https://www.antrade.io/guide/docs/cn/d-kama/#TradingView%E5%B1%95%E7%A4%BA%E7%9A%84%E5%8F%AF%E8%A7%86%E5%8C%96%E7%9A%84D-KAMA%E7%AD%96%E7%95%A5)
* [**双均线策略回测结果与稳健性分析**](https://www.antrade.io/guide/docs/cn/d-kama/#D-KAMA%E7%AD%96%E7%95%A5%E5%9B%9E%E6%B5%8B%E7%BB%93%E6%9E%9C%E4%B8%8E%E7%A8%B3%E5%81%A5%E6%80%A7%E5%88%86%E6%9E%90)

**双均线策略原理**

双均线是深度改进后的双均线交易策略。

均线最早由美国投资专家Joseph E.Granville(格兰威尔)于20世纪中期提出，现在仍然广泛为人们使用，成为判断买卖信号的一大重要指标。从统计角度来说，均线就是历史价格的平均值，可以代表过去N日价格的平均走势。

1962年7月，Joseph E.Granville在他的书中提出了著名的Granville八大买卖法则。只利用价格和均线即可进行择时，方法简单有效，一经提出，迅速受到市场追捧。尤其是其中的金叉和死叉信号，更是沿用至今。

Granville 八大法则其中有四条是用于判断买进时机，另外四条是用于判断卖出时机。买进和卖出法则一一对应，分布在高点的左右两侧（除买4和卖4以外）。法则内容如下所示：

买1：均线整体上行，价格由下至上上穿均线，此为黄金交叉，形成第一个买点。\
买2：价格出现下跌迹象，但尚未跌破均线，此时均线变成支撑线，形成第二个买点。\
买3：价格仍处于均线上方，但呈现急剧下跌趋势。当跌破均线时，出现第三个买点。\
买4：（右侧）价格和均线都处于下降通道，且价格处于均线下方，严重远离均线，出现第四个买点。

卖1：均线由上升状态变为缓慢下降的状态，价格也开始下降。当价格跌破均线时，此为死亡交叉，形成第一个卖点。\
卖2：价格仍处于均线之下，但价格开始呈现上涨趋势，当价格无限接近均线但尚未突破时，此时均线变成阻力线，形成第二个卖点。\
卖3：价格终于突破均线，处于均线上方。但持续时间不长，价格开始下跌，直至再一次跌破均线，此为第三个卖点。\
卖4：（左侧）价格和均线都在上涨，价格上涨的速度远快于均线上涨的速度。当价格严重偏离均线时，出现第四个卖点。

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/12/attach_16402fcc49ff5d9b.jpg" alt=""><figcaption></figcaption></figure>

#### 均线策略为什么有效？ <a href="#jun-xian-ce-lve-wei-shen-me-you-xiao" id="jun-xian-ce-lve-wei-shen-me-you-xiao"></a>

Shiller（1981）在研究中发现，资产的长期价格呈现均值回复的特征，**即从长期来看，资产的价格会回归均值。这也是均线理论被广泛应用的前提。**

#### 均线策略的缺陷 <a href="#jun-xian-ce-lve-de-que-xian" id="jun-xian-ce-lve-de-que-xian"></a>

均线归根到底是一种平均值，平均值在应用过程中存在最大的问题就是其**滞后性**。当出现买入卖出信号时，最佳时机早已过去。举例来说，如果A股票最新价格出现了较大的涨幅，股价和均线都上涨，但均线的速度慢于股价上涨速度。此时，从形态上来看，金叉出现，为买入信号。次日，股价回调，股价下降的速度快于均线下降的速度，形成死叉，为卖点。这样一买一卖不仅没有盈利，反而出现亏损。

另外，价格变化的速度本身就在变化，传统简单均线受困于固定周期参数，这使得不论市场的走势如何，短期均线灵敏度高，更贴近价格走势，但在市场震荡时期反复转向时，会造成频繁发出错误开平仓信号；长期均线在趋势判断上更加可靠，但在市场加速上涨或下跌时反应迟钝，会造成错过最佳的买卖点。

**KAMA-卡夫曼自适应移动均线对双均线策略的改进**

在《精明交易者》中，作者卡夫曼（Kaufman）提出了“自适应移动平均线”，简称AMA。该均线考虑到了市场价格变化速率，在普通均线的基础上增加了平滑系数，并自适应动态调整均线的灵敏度，可以在慢速趋势和快速趋势之间自我调整。

当市场出现盘整、趋势不明显时期，AMA倾向于慢速移动平均线。

**当市场波动较大，趋势明显，价格沿一个方向快速移动时，AMA倾向于快速移动平均线。**

**双均线趋势策略逻辑**

* 计算30分钟周期KAMA(120，250)卡夫曼自适算法均线
* 120均线上穿250均线开多(平空)，120均线下穿250均线开空(平多)
* 动态的止损策略，监控入场价格突破3倍平滑ATR支撑实时止损

**如何启动双均线策略机器人？**

1\. 登录AntBot账号，在【交易】界面的【机器人】里找到【双均线】。

2\. 点击右侧按钮，进入参数设置页面。

3\. 根据个人标准和偏好选择币种。

4\. 设置【首张单数】【杠杆率 】【最大单数】【运行方式】【开单方向】【止盈比例】与 【止损比例】。

* 【首张单数】机器人从未持仓状态下首次开仓时的持仓量。建议初学者保持默认值。
* 【杠杆率】：加杠杆可以当做向交易所借入资金去持仓，这份持仓资金相对于本金的倍数即为杠杆率，加杠杆会放大盈亏。建议初学者保持5倍杠杆率的默认值。
* 【最大单数】：机器人从没有持仓开始允许连续加仓的最大次数。
* 【运行方式】：分为循环运行和单次运行。循环运行是指每次止盈平仓后机器人会重复下一轮开仓，机器人只会在达到止盈比例或止损比例后才会停止。单次运行是指机器人在完成一次全仓止盈后将自动终止运行。
* 【自动】：机器人会根据策略信号自动变更多空头寸开单。
* 【只多】：机器人只接收多头信号开单。
* 【只空】：机器人只接收空头信号开单。
* 【止盈比例】

1、默认【系统追踪】值，机器人每间隔30分钟计算策略信号。当信号反转时将会平仓止盈，机器人进入下一循环。\
2、如有预设比例值，机器人持仓收益率达到此预设值将会平仓止盈，机器人进入下一循环。

* 【止损比例】

1、默认【系统追踪】值，机器人在建仓时会根据30分钟周期的价格真实波动预埋止损比例，当持仓亏损率达到此预设值将会平仓止损，机器人进入下一循环。\
2、如有预设比例值，机器人持仓亏损率达到此预设值将会平仓止损，机器人进入下一循环。

5\. 点击【启动】即可成功创建双均线机器人。

<figure><img src="https://www.antrade.io/guide/docs/cn/wp-content/uploads/2022/12/3-3.jpg" alt=""><figcaption></figcaption></figure>

**TradingView展示的可视化的双均线策略**

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/1668644820964.png" alt=""><figcaption></figcaption></figure>

**双均线策略回测结果与稳健性分析**

周期 – 30分钟线\
入场金额$1000，每次进场交易金额为100%cash\
交易时间：2022/1/1\~2022/10/31\
标的：ETHUSDTPER\
手续费：0.04%

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/1668644722659.png" alt=""><figcaption></figcaption></figure>

**参考文档**：

[https://www.mianshigee.com/note/detail/5040rdw/](https://www.mianshigee.com/note/detail/5040rdw/)\
[https://www.freesion.com/article/72541078443/](https://www.freesion.com/article/72541078443/)\
[http://www.360doc.com/content/19/1105/21/32762466\_871317844.shtml](http://www.360doc.com/content/19/1105/21/32762466\_871317844.shtml)

[#AntBot](https://www.antrade.io/guide/docs/cn/tag/antbot/)[#bot](https://www.antrade.io/guide/docs/cn/tag/bot/)[#D-KAMA](https://www.antrade.io/guide/docs/cn/tag/d-kama/)[#strategy](https://www.antrade.io/guide/docs/cn/tag/strategy/)[#trading](https://www.antrade.io/guide/docs/cn/tag/trading/)[#trend-following](https://www.antrade.io/guide/docs/cn/tag/trend-following/)@AntBot free trading bot\
