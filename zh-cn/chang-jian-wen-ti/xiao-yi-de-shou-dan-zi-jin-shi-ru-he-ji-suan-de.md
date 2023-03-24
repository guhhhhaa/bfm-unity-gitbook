# 小蚁的首单资金是如何计算的？

[Skip to content](https://www.antrade.io/guide/docs/cn/how-is-antbots-initial-positions-calculated/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/cn/)[首页](https://www.antrade.io/guide/docs/cn/)[免费使用AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/cn)
* [常见问题](https://www.antrade.io/guide/docs/cn/cn-1dpg3cthijkng/)
* [小蚁的首单资金是如何计算的？](https://www.antrade.io/guide/docs/cn/how-is-antbots-initial-positions-calculated/)

Search for:

常见问题

*
  * [如何绑定Bitget API？](https://www.antrade.io/guide/docs/cn/binding\_bitget/)
  * [如何绑定MEXC API？](https://www.antrade.io/guide/docs/cn/binding\_mexc/)
  * [如何绑定Gate.io API?](https://www.antrade.io/guide/docs/cn/binding\_gateio/)
  * [如何重新进行快速授权？](https://www.antrade.io/guide/docs/cn/quickly-reauthorize-binance/)
  * [同个币种可以同时运行多个机器人吗？](https://www.antrade.io/guide/docs/cn/one-crypto-run-multiple-bots/)
  * [在一个账户下可以导入两个交易所的API Key吗？](https://www.antrade.io/guide/docs/cn/two-api-keys-under-one-account/)
  * [智能网格的盈利和交易所的盈利怎么不一样?](https://www.antrade.io/guide/docs/cn/the-profit-difference-in-ai-grid-and-exchange/)
  * [因能量不足机器人暂停了，但充值能量后机器人为何还是处于暂停状态？](https://www.antrade.io/guide/docs/cn/bots-are-stopped-when-purchased-energy/)
  * [系统会不会卖掉我在交易所手动购买的币？](https://www.antrade.io/guide/docs/cn/will-antbot-sell-funds-i-bought/)
  * [什么是双向持仓模式？](https://www.antrade.io/guide/docs/cn/hedge-mode/)
  * [交易所账户持仓限额，怎么办？](https://www.antrade.io/guide/docs/cn/position-limit-of-exchange-account/)
  * [为什么价格已经到达加仓价格而系统没有进行加仓？](https://www.antrade.io/guide/docs/cn/why-is-position-not-added/)
  * [能量可以兑换成USDT吗？](https://www.antrade.io/guide/docs/cn/energy-exchange-usdt/)
  * [API密钥交易权限不足：如何修改API密钥交易权限？](https://www.antrade.io/guide/docs/cn/insufficient-api-trading-permissions/)
  * [如何在币安中填写IP地址？](https://www.antrade.io/guide/docs/cn/ip-address-of-binance/)
  * [如何绑定Kucoin API?](https://www.antrade.io/guide/docs/cn/binding\_kucoin/)
  * [量化交易机器人真能赚到钱吗?](https://www.antrade.io/guide/docs/cn/can-quantitative-trading-robots-really-make-money/)
  * [小蚁的首单资金是如何计算的？](https://www.antrade.io/guide/docs/cn/how-is-antbots-initial-positions-calculated/)
  * [新手应该选择启动哪个机器人，选择哪些币种？](https://www.antrade.io/guide/docs/cn/which-robot-should-a-novice-choose-to-start/)
  * [如何减少手币安交易手续费？](https://www.antrade.io/guide/docs/cn/reducing-trading-fees/)

## 小蚁的首单资金是如何计算的？

4月 ago[AntBot](https://www.antrade.io/guide/docs/cn/author/antbot/)1 minute

小蚁中的仓位管理方法，是以ATR指标为核心的。

**ATR是什么，如何计算获得？**

均幅指标(ATR)是取一定时间周期内的股价波动幅度的移动平均值。\
ATR计算公式如下：

**1、真实波幅（TR）：** TR = MAX（∣最高价-最低价∣，∣最高价-昨收∣，∣昨收-最低价∣）

**2、真实波幅均值（ATR）：** ATR = TR的N日简单移动平均

**以ATR制定头寸规模**

一般认为，交易品种的平均波动幅度ATR越大，其风险也越大。因此，波动越大的品种，头寸配比应该越小。

**首单资金 = M**\***总资金的1%/ATR**

前面公式中的变量M根据策略类型而定。

[#AntBot](https://www.antrade.io/guide/docs/cn/tag/antbot/)[#learner](https://www.antrade.io/guide/docs/cn/tag/learner/)[#strategy](https://www.antrade.io/guide/docs/cn/tag/strategy/)[#trading](https://www.antrade.io/guide/docs/cn/tag/trading/)[#trend-following](https://www.antrade.io/guide/docs/cn/tag/trend-following/)@AntBot free trading bot\
