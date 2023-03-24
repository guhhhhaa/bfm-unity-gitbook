# 马丁格尔策略参数详解

[Skip to content](https://www.antrade.io/guide/docs/cn/parameters\_dca/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/cn/)[首页](https://www.antrade.io/guide/docs/cn/)[免费使用AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/cn)
* [进阶学习](https://www.antrade.io/guide/docs/cn/cn-learning/)
* [马丁格尔策略参数详解](https://www.antrade.io/guide/docs/cn/parameters\_dca/)

Search for:

进阶学习

*
  * [支撑和阻力原理详解](https://www.antrade.io/guide/docs/cn/support-resistance/)
  * [如何减少手币安交易手续费？](https://www.antrade.io/guide/docs/cn/reducing-trading-fees/)
  * [常见问题和解答](https://www.antrade.io/guide/docs/cn/frequently-asked-questions/)
  * [什么叫阳包阴形态？](https://www.antrade.io/guide/docs/cn/engulfing-bullish-patterns/)
  * [什么叫三只乌鸦形态？](https://www.antrade.io/guide/docs/cn/three-black-crows-patterns/)
  * [什么叫红三兵形态？](https://www.antrade.io/guide/docs/cn/three-white-soldiers-patterns/)
  * [什么叫锤子线形态？](https://www.antrade.io/guide/docs/cn/long-lower-shadow-patterns/)
  * [什么叫倒锤子线形态？](https://www.antrade.io/guide/docs/cn/long-upper-shadow-patterns/)
  * [什么是BBW(Bollinger Bands Width)指标？](https://www.antrade.io/guide/docs/cn/bbw-indicator/)
  * [什么是RSI(Relative Strength Index)指标?](https://www.antrade.io/guide/docs/cn/rsi-indicator/)
  * [什么是SMA(Simple Moving Average)指标？](https://www.antrade.io/guide/docs/cn/ma-indicator/)
  * [什么是KDJ指标？](https://www.antrade.io/guide/docs/cn/kdj-indicator/)
  * [什么是MACD指标?](https://www.antrade.io/guide/docs/cn/macd-indicator/)
  * [马丁格尔策略参数详解](https://www.antrade.io/guide/docs/cn/parameters\_dca/)
  * [小蟻會不會賣掉我在交易所手動購買的幣？](https://www.antrade.io/guide/docs/cn/cn-1dorqc18qo443/)
  * [為什麼價格已經到達補倉價格後系統沒有進行補倉？](https://www.antrade.io/guide/docs/cn/cn-1dornfm25vrsh/)
  * [機器人的浮盈比例和回報率如何理解？](https://www.antrade.io/guide/docs/cn/cn-1dorp3kchr9kb/)
  * [最安全且高利潤率的投資組合是什麼？](https://www.antrade.io/guide/docs/cn/cn-1dorrv0hrpbui/)
  * [如何對幣安賬戶進行持倉限制調整？](https://www.antrade.io/guide/docs/cn/cn-1dpggek6iesdu/)
  * [如何理解機器人的暫停功能？](https://www.antrade.io/guide/docs/cn/cn-1doii6uupa9m8/)

## 马丁格尔策略参数详解

5月 ago[AntBot](https://www.antrade.io/guide/docs/cn/author/antbot/)1 minute

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/d9e09e75dd375c1d4a27e52544c71a8.jpg" alt=""><figcaption></figcaption></figure>

**多**

运行做多的机器人。

**空**

运行做空的机器人。

**震荡**

同时运行做多和做空的机器人。

**杠杆率**

加杠杆可以当做向交易所借入资金去持仓，这份持仓资金相对于本金的倍数即为杠杆率，加杠杆会放大盈亏。建议初学者保持5倍杠杆率的默认值。

**首单数量**

机器人从未持仓状态下首次开仓时的持仓量。建议初学者保持默认值。

**最大持仓**

即在完成『最大单数』后的总持仓额。

**循环运行**

每次止盈平仓后机器人会重复下一轮开仓，机器人只会在达到『其他』设置里的止盈或者止损的预设的盈亏条件后才会停止。

**单次运行**

机器人在完成一次全仓止盈后将自动终止运行。

**风险偏好**

风险越大加仓时价格间隔和止盈比例也越大，风险大小依次是激进>稳健>保守。

**最大单数**

机器人从没有持仓开始允许连续加仓的最大次数。

**补仓倍数**

下次开仓量按照本开仓量的倍数进行开仓，也认作：下次开仓量=本次开仓量X『补仓倍数』。

**补仓间隔(%)**

以多头机器人为例，参照上次开仓价，市价跌幅达到此预设比例将会加仓，反之对空头机器人市价涨幅达到此预设值将会加仓。 (可配合『补仓回调』使用)

**补仓回调(%)**

以多头机器人为例，市价从新低回撤，回撤比例到此预设值，并且此时市价满足补仓比例才进行补仓；对空头机器人市价从新高回撤，回撤比例到此预设值，并且此时市价满足补仓比例才进行补仓。

**止盈比例(%)**

机器人持仓资产收益率达到此预设值将会平仓止盈，机器人进入下一循环。 （可配合『止盈回调』使用）

**止盈回调(%)**

以多头机器人为例，市价从新高回撤，回撤比例到此预设值，并且此时市价满足止盈比例才进行平仓；对空头机器人市价从新低回撤，回撤比例到此预设值，并且此时市价满足止盈比例才进行平仓。

**价格上限**

当市价高于该预设价格，多空机器人都将不会开仓，只会执行平仓，直到价格跌回预设价格内，机器人才重新恢复开仓。

**价格下限**

当市价低于该预设价格，多空机器人都将不会开仓，只会执行平仓，直到价格涨回预设价格内，机器人才重新恢复开仓。

**首单加倍**

机器人每次从没仓开仓时，按用户设置首单额度的双倍金额开仓，这里需要注意，后续的补仓额度还按原来的首单计算。这个设定在小波幅震荡行情能显著增加收益。

**智能补仓**

如果当前持仓额超过预计投入的25%，即使市价达到补仓条件，AI系统也不会立即补仓,需要等待MACD指标(4小时)出现多空力量僵持或逆转时才进行补仓。

**按比例止盈**

对多头机器人，如果市价高于预设价格或者对空仓机器人如果市价低于预设价格，机器人将自动清仓止盈并停止。

**按比例止损**

对多头机器人，如果市价低于预设价格或者对空仓机器人如果市价高于预设价格，机器人将自动清仓止损并停止。

**按金额止盈**

实现盈亏+浮动盈亏>该预设金额，满足上述条件机器人将会自动清仓止盈并停止。

**按金额止损**

浮动盈亏 < 该预设金额的负值，满足上述条件机器人将会自动清仓止损并停止。

[#AntBot](https://www.antrade.io/guide/docs/cn/tag/antbot/)@AntBot free trading bot\
