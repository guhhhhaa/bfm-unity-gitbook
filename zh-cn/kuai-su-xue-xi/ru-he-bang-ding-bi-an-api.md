# 如何绑定币安API？

[Skip to content](https://www.antrade.io/guide/docs/cn/binding\_binance/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/cn/)[首页](https://www.antrade.io/guide/docs/cn/)[免费使用AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/cn)
* [快速学习](https://www.antrade.io/guide/docs/cn/cn-1dnmtb50vo4uf/)
* [如何绑定币安API？](https://www.antrade.io/guide/docs/cn/binding\_binance/)

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

## 如何绑定币安API？

5月 ago[AntBot](https://www.antrade.io/guide/docs/cn/author/antbot/)1 minute

在开始之前，请确保你的现货账户和期货账户有充足的余额。如果账户余额不足，需要先进行划转操作。这样才能在小蚁顺利开启现货或者期货机器人。

<figure><img src="https://www.antrade.io/guide/docs/cn/wp-content/uploads/2023/03/71aa87b1d1482ee0db34915bc690828.jpg" alt=""><figcaption></figcaption></figure>

<figure><img src="https://www.antrade.io/guide/docs/cn/wp-content/uploads/2023/03/dd792ced2644b79efd3174937c940ec.jpg" alt=""><figcaption></figcaption></figure>

#### 如何创建Binance API Key并绑定到AntBot？

YouTube 视频教学：[https://youtu.be/ajvXcuYqBYU](https://youtu.be/ajvXcuYqBYU)

**1、在Binance应用程序上登录您的账户后，在【首页】上单击【更多】。**

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2023/02/1-2.jpg" alt=""><figcaption></figcaption></figure>

**2、在【服务】页面上向下滚动到底部找到【API管理】。**

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2023/02/2.1jpg.jpg" alt=""><figcaption></figcaption></figure>

**3、点击【创建API】。**

安全提示：在创建API之前，您需要在账户上启用**双重认证（2FA）**。

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2023/02/3.jpg" alt=""><figcaption></figcaption></figure>

**4、勾选【系统生成】，然后单击【下一步】。**

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2023/02/4-2.jpg" alt=""><figcaption></figcaption></figure>

**5、为您的API密钥输入一个标签/名称（例如：AntBot），然后单击【下一步】。**

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2023/02/5.jpg" alt=""><figcaption></figcaption></figure>

**6、在安全验证页面上，点击【获取验证码】，输入手机验证码、电子邮件验证码和谷歌/Binance验证码，然后点击【提交】。**

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2023/02/6.jpg" alt=""><figcaption></figcaption></figure>

**7、您的API已创建。单击【编辑】按钮修改API权限。**

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2023/02/8.jpg" alt=""><figcaption></figcaption></figure>

**8、首先，选择【仅限受信任的IP访问】。然后填入小蚁的IP地址，勾选【启用现货&杠杆交易】和【启用期货】选项。最后，单击【保存】。**

输入IP白名单地址：**101.36.117.216 165.154.41.100 36.255.222.23 165.154.60.7 101.36.127.124 101.36.108.79 122.10.161.141 165.154.60.119 165.154.44.65**

提示：在勾选【启用期货】选项之前，您必须先拥有期货账户并完成期货风险测试。请妥善保管您的秘密密钥，因为它不会再次显示。如果您忘记了API密码密钥，则需要删除API并创建新的API密钥。

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2023/02/9-1.jpg" alt=""><figcaption></figcaption></figure>

**9、复制并粘贴API密钥和密码密钥到AntBot，然后单击【绑定】。**

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2023/02/9.jpg" alt=""><figcaption></figcaption></figure>

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2023/02/10.jpg" alt=""><figcaption></figcaption></figure>

成功了！

如果您已成功完成这些步骤，现在您可以开始在AntBot上使用机器人赚钱了。

[#AntBot](https://www.antrade.io/guide/docs/cn/tag/antbot/)@AntBot free trading bot\
