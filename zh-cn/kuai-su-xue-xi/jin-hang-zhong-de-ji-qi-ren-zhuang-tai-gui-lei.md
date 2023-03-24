# 進行中的機器人狀態歸類

[Skip to content](https://www.antrade.io/guide/docs/cn/cn-1do89q0srd22l/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/cn/)[首页](https://www.antrade.io/guide/docs/cn/)[免费使用AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/cn)
* [快速学习](https://www.antrade.io/guide/docs/cn/cn-1dnmtb50vo4uf/)
* [進行中的機器人狀態歸類](https://www.antrade.io/guide/docs/cn/cn-1do89q0srd22l/)

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

## 進行中的機器人狀態歸類

6月 ago[AntBot](https://www.antrade.io/guide/docs/cn/author/antbot/)1 minute

#### “交易正常”的機器人狀態歸類如下： <a href="#g7ikd1" id="g7ikd1"></a>

**等待開倉**

**馬丁格爾AI、經典網格、馬丁格爾：**\
這幾類機器人啟動後如果顯示“等待開倉”，則機器人處於監聽狀態，稍等片刻會完成開倉。正常情況下無需處理，如遇到該狀態持續超過3分鐘，請查看[首次使用，機器人無法買入或開倉？](https://antrade.io/guide/docs/cn/cn-1dofnr94b4pee)

**貝塔AI：**\
機器人啟動後如果顯示“等待開倉”，則表示機器人正在等待開倉的信號派發，當前行情並沒有滿足機器人開倉的條件。請耐心等待，可能需要等待幾個小時，甚至是幾天。

**通道震盪：**\
機器人啟動後如果顯示“等待開倉”，則表示機器人正在等待最新市價觸及上軌價格或者下軌價格，請耐心等待。您也可以通過自身對行情的判斷，調整上軌價格和下軌價格，已達到快速開倉的目的。

**交易正常**

表示機器人狀態正常，無需干預。

#### “交易異常”的機器人狀態歸類如下： <a href="#8mo5nb" id="8mo5nb"></a>

**持倉不足**

機器人記錄的持倉數量和交易所實際持倉數量不一致，一般是因為用戶從交易所手動減倉或全部賣出了。這種情況下，建議對機器人進行“清倉終止”操作後再重新開啟該幣種的機器人。

**USDT不足**

您在交易所裡面的USDT餘額不足，機器人無法再開倉。建議去交易所充值USDT。

**等待補倉信號**

在馬丁機器人開啟了智能補倉選項下，在持續單邊行情中，小蟻會根據當前倉位情況自動判斷停止補倉，直到行情重回多空對峙時才進行補倉，目標是最大概率最大限度壓低倉位虧損比例。

**保證金不足**

表示您在交易所合約賬戶U本位裡面的保證金餘額已不足，機器人無法再進行開倉操作。建議您前往交易所增加保證金，避免強平風險。

**超出風控倉位**

系統風控限制了機器人開倉，如果繼續開倉將超過『現貨風控倉位』或者『合約風控倉位』的预设值。如要機器人繼續開倉請在交易所增加本金或者調整对应的风控值。

備註：一般來說，遇到現貨機器人被風控倉位攔截不補倉則不用著急調大參數。遇到暴跌行情，等有反彈跡象再調大參數，補倉完畢再調回25%。風控倉位設計的目的就是留足時間給用戶去做決策。人和機器人進行配合，才可能在底部補倉。

**突破價格上限**

當幣價突破預設的『價格上限』，機器人將不再開倉。

* AI機器人會根據行情自動調整該預設價格，需要等待幾個小時甚至幾天的時間。
* 非AI機器人需等待價格回撤或者手動修改該預設價格才會恢復開倉。

**跌穿價格下限**

當幣價跌破預設的『價格下限』，機器人將不再開倉。

* AI機器人會根據行情自動調整該預設價格，需要等待幾個小時甚至幾天的時間。
* 非AI機器人需等待價格反彈或者手動修改該預設價格才會恢復開倉。

**超出預計投入**

最大總投入限制了機器人開倉，如果繼續開倉將超過『預計總投入』。通過增加『最大單數』可以增加『預計總投入』。

補充說明：這是因為**待補倉額**加上**持倉估值**大於**預計投入**。一般做空的機器人才會出現此狀態。做空的機器人原先計劃投入的張數價值變大，而補倉是基於張數計算預計投入，那麼後面的實際投入會超過原先的計劃投入，這種情況下機器人不會再補倉。您可根據可用資金情況和行情判斷是否需要取消該限制，調大預計總投入即可，從而達到補倉目的。

**超出做單次數**

超出預設『最大單數』系統停止開倉。您需要根據個人資金情況增加做單次數。

**交易超額**

出現該狀態時，一般是因為當前持倉額已經接近交易所的最大持倉額限制，無法再補倉，只平倉。可繼續等待達到止盈條件後觸發自動平倉。

[幣安合約持倉限制調整說明](https://www.binance.com/zh-CN/support/faq/13163f41fe2b44af982e612dfe7e6709)

**交易出錯**

出現該狀態無法自動修復，一般是交易所拒絕了您的交易請求，機器人無法正常交易。請聯繫AntBot在線客服尋求幫助。

**最小持倉小於15u**

***

[機器人暫停原因](https://antrade.io/guide/docs/cn/cn-paused)

[#AntBot](https://www.antrade.io/guide/docs/cn/tag/antbot/)@AntBot free trading bot\
