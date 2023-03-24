# 歷史機器人停止原因

[Skip to content](https://www.antrade.io/guide/docs/cn/cn-1do8ag27eusj1/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/cn/)[首页](https://www.antrade.io/guide/docs/cn/)[免费使用AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/cn)
* [快速学习](https://www.antrade.io/guide/docs/cn/cn-1dnmtb50vo4uf/)
* [歷史機器人停止原因](https://www.antrade.io/guide/docs/cn/cn-1do8ag27eusj1/)

Search for:

快速学习

*
  * [启动机器人需要多少资金？](https://www.antrade.io/guide/docs/cn/how-much-capital-do-i-need-to-start-a-bot/)
  * [如何减少手币安交易手续费？](https://www.antrade.io/guide/docs/cn/reducing-trading-fees/)
  * [常见问题和解答](https://www.antrade.io/guide/docs/cn/frequently-asked-questions/)
  * [如何绑定欧易API？](https://www.antrade.io/guide/docs/cn/binding\_okx/)
  * [如何绑定币安API？](https://www.antrade.io/guide/docs/cn/binding\_binance/)
  * [如何绑定Bybit API？](https://www.antrade.io/guide/docs/cn/binding\_bybit/)
  * [如何绑定火币 API？](https://www.antrade.io/guide/docs/cn/binding\_huobi/)
  * [軟件內彈窗提示說明](https://www.antrade.io/guide/docs/cn/cn-1dpdt50h9f5om/)
  * [使用合約機器人需要注意哪些事項？](https://www.antrade.io/guide/docs/cn/cn-1dodlqdr1oqlj/)
  * [多少資金可以啟動多少個機器人？](https://www.antrade.io/guide/docs/cn/cn-1dodllk5easg6/)
  * [如何做資金規劃和倉位管理？](https://www.antrade.io/guide/docs/cn/cn-1dodkr7b4qkps/)
  * [机器人暂停原因](https://www.antrade.io/guide/docs/cn/cn-paused/)
  * [AntBot的常见问题](https://www.antrade.io/guide/docs/cn/faq/)
  * [歷史機器人停止原因](https://www.antrade.io/guide/docs/cn/cn-1do8ag27eusj1/)
  * [進行中的機器人狀態歸類](https://www.antrade.io/guide/docs/cn/cn-1do89q0srd22l/)
  * [新手如何绑定API并启动机器人](https://www.antrade.io/guide/docs/cn/beginner-guides/)

## 歷史機器人停止原因

6月 ago[AntBot](https://www.antrade.io/guide/docs/cn/author/antbot/)0 minutes

#### 歷史機器人停止原因 <a href="#w0jfm" id="w0jfm"></a>

**運行單次**

您對該機器人設置了**單次運行**，機器人達到本次止盈條件並已經平倉。

**總收益止盈**

您對該機器人設置了止盈，機器人達到總收益止盈條件並已經平倉。

**總虧損止損**

您對該機器人設置了止損，機器人達到總虧損止損條件並已經平倉。

**清倉終止**

您手動終止了機器人。

**持倉不足不能平倉**

您在交易所的持頭寸小於機器人記錄的頭寸，因此機器人無法根據其記錄的頭寸平倉。

**訂單不存在了**

您在交易所的倉位已平倉，沒有剩餘倉位，機器人無法為您完成交易。\
[使用合約機器人需要注意哪些事項？](https://antrade.io/guide/docs/cn/cn-1dodlqdr1oqlj)

**非法持倉數額交易出錯**

機器人平倉的時候檢測到您在交易所的倉位數量低於機器人記錄的倉位數量。機器人無法按原計劃平倉。請到交易所檢測該倉位是否還存在，如果存在請手動平倉後再去重新啟動機器人。

**掛單或持倉超出當前初始槓桿下的最大值**

**訂單的持倉方向和用戶設置不一致**

一般是首次使用小蟻的時候才出現。原因是您在交易所有合約倉位存在，則機器人無法幫您切換到雙向持倉模式，請先在交易所手動平倉，再去啟動機器人。如果機器人還是無法正常運行，那麼需要您去交易所手動設置雙向持倉模式。\
[如何將幣安的倉位模式修改為雙向持倉？](https://antrade.io/guide/docs/cn/cn-1dpb4g9gjmprv)\
[如何將歐意的倉位模式修改為雙向持倉？](https://antrade.io/guide/docs/cn/cn-1dpd5kq9vn7e7)

**無效的交易對**

**當前賬戶模式不支持此操作**

交易所主动拒绝了机器人的交易请求。请联系交易所的客服，确认您是否拥有现货和合约的交易权益。

**交易对已下架**

当前硬币已经下架，机器人无法正常交易。请去选择其他硬币。

**未知原因**

未知的原因导致机器人无法正常交易。如果多次出现，请联系小蚁客服进行咨询。

@AntBot free trading bot\
