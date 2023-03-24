# 軟件內彈窗提示說明

[Skip to content](https://www.antrade.io/guide/docs/cn/cn-1dpdt50h9f5om/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/cn/)[首页](https://www.antrade.io/guide/docs/cn/)[免费使用AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/cn)
* [快速学习](https://www.antrade.io/guide/docs/cn/cn-1dnmtb50vo4uf/)
* [軟件內彈窗提示說明](https://www.antrade.io/guide/docs/cn/cn-1dpdt50h9f5om/)

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

## 軟件內彈窗提示說明

5月 ago[AntBot](https://www.antrade.io/guide/docs/cn/author/antbot/)1 minute

#### 軟件內彈窗提示說明 <a href="#69dgti" id="69dgti"></a>

**小蟻賬戶餘額不足**

_解釋：_\
小蟻賬戶的USDT餘額不足，無法完成能量購買。

_解決方法：_\
請先充值足夠的USDT。

**當前權限不足**

_解釋：_\
您的API權限不足，請去交易所核對相應權限是否開通。

_解決方法：_

* 連接幣安API的用戶請檢查允許讀取、允許現貨及槓桿交易和允許合約三項權限是否已經勾選；
* 連接歐意API的用戶請檢查是否已經開啟交易權限；

**可開張數不足 / 可用張數不足**

_解釋：_\
表示您的可用資金超出預計投入，在當前參數條件下無法啟動機器人。

_解決方法：_\
增加資金\
調小最大單數\
修改補倉倍數（AI類型的機器人無法修改）

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/10/%E8%BB%9F%E4%BB%B6%E5%85%A7%E5%BD%88%E7%AA%97%E6%8F%90%E7%A4%BA%E8%AA%AA%E6%98%8E.jpg" alt=""><figcaption></figcaption></figure>

**已經有相同的機器人正在運行**

_解釋：_\
同一個幣已經運行了同類型機器人，或者您在交易所已經有倉位存在。

解決方法：

* 去交易所檢查期貨倉位，是否已經有相同的幣存在。需要手動平倉才能去啟動機器人。
* 請查看：[同一個幣可以運行多個機器人嗎？](https://antrade.io/guide/docs/cn/cn-1dpd17mhjenfc)

**最小持倉不能小於15u**

_解決方法_\
現貨機器人首單金額最小是 16 USDT；\
合約機器人首單金額使用默認的，如果出現該提示，嘗試調大，直到可以啟動機器人。

**該交易對處於持倉狀態,清倉後才能切換成震盪模式**

_解決方法：_\
[如何將幣安的倉位模式修改為雙向持倉？](https://antrade.io/guide/docs/cn/cn-1dpb4g9gjmprv)\
[如何將歐意的倉位模式修改為雙向持倉？](https://antrade.io/guide/docs/cn/cn-1dpd5kq9vn7e7)\
[如何將Bybit的倉位模式修改為雙向持倉？](https://antrade.io/guide/docs/cn/cn-1dq8go52c8iu5)

**該交易對處於持倉狀態,清倉後才能切換成全倉模式**

_解決方法：_\
[如何將幣安的保證金模式改成全倉？](https://antrade.io/guide/docs/cn/cn-1dppgema4qa1d)\
[如何將歐意的保證金模式改成全倉？](https://antrade.io/guide/docs/cn/cn-1dppnqdn7l8t4)

**超出風控倉位,不能啟動新機器人**

_解決方法：_

**該交易對已經持倉,請平倉後再添加機器人**

_解決方法：_

* 去交易所檢查期貨倉位，查看該交易對是否已經存在倉位。需要手動平倉才能去啟動機器人。
* 請查看：[同一個幣可以運行多個機器人嗎？](https://antrade.io/guide/docs/cn/cn-1dpd17mhjenfc)

**期貨賬戶註冊不到60天不可以使用20倍以上的槓桿**

_解釋：_\
重要通知：幣安合約對註冊合約賬戶少於 60 天的用戶實行槓桿限制。\
自2021年07月27日生效之日起，註冊合約賬戶少於60天的新用戶將不允許開倉槓桿超過20倍。\
新的槓桿限制也將適用於註冊合約賬戶少於60天的現有用戶：\
對於未平倉且頭寸低於20倍槓桿的用戶，將不允許將其未平倉頭寸調整到超過20倍槓桿。\
持倉且槓桿超過20倍的用戶可以選擇維持現有的槓桿，但不允許進一步提高槓桿倍數。他們只能將未平倉頭寸的槓桿調整至20倍及以下。\
對於沒有持倉的新合約用戶，所有新開倉位的槓桿不得超過20倍。\
新合約用戶的槓桿限制將在註冊滿60天後逐漸增加。

_解決方法：_\
等待您的幣安合約賬戶取消槓桿限制

**暫停的機器人不能修改策略**

_解決方法：_\
請先恢復機器人正常運行，然後再修改機器人。

**您的現貨賬戶可用資金不足，不能啟動新的機器人。建議去交易所增加資金**

_解決方法：_\
根據提示操作

**您的合约账户风险评估(较高),建议降低参数或减少机器人**

_解決方法：_

* 去交易所增加资金
* 通过修改最大单数和补仓倍数减少预计投入，首单金额使用默认值
* 减少机器人数量

[#AntBot](https://www.antrade.io/guide/docs/cn/tag/antbot/)@AntBot free trading bot\
