# CCXT文档

## [CCXT](https://www.cnblogs.com/zyyhxbs/p/13803561.html)

* [一，简介](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label0)
* [二，特点](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label1)
* [三，安装](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label2)
* [四，用法](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label3)
  * [一，介绍](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label3_0)
  * [二，接口](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label3_1)
  * [三，实例化CCXT交易所类](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label3_2)
  * [四，交易所数据结构](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label3_3)
  * [五，交易所API限流](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label3_4)
  * [六，DDoS保护异常及处理办法](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label3_5)
* [五，CCXT市场模型](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label4)
  * [一，市场数据结构](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label4_0)
  * [二，数据精度和极限值](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label4_1)
  * [三，委托单数值要求和格式化方法](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label4_2)
  * [四，载入市场清单](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label4_3)
  * [五，交易符号和市场ID](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label4_4)
  * [六，货币命名的一致性](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label4_5)
  * [七，货币命名常见问题及解答](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label4_6)
  * [八，市场缓冲强制重载](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label4_7)
* [六，CCXT API](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label5)
  * [一，API方法与访问端节点](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label5_0)
  * [二，隐式API方法](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label5_1)
  * [三，公开/私有API](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label5_2)
  * [四，同步调用与异步调用](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label5_3)
  * [五，调用参数与返回值](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label5_4)
  * [六，API方法命名规范](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label5_5)
  * [七，统一API](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label5_6)
  * [八，改写统一API的参数](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label5_7)
  * [九，统一API结果的分页](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label5_8)
* [七，CCXT委托账本模型](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label6)
  * [一，交易委托账本](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label6_0)
  * [二，委托账本模型的结构](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label6_1)
  * [三，市场深度](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label6_2)
  * [四，获取市场价格](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label6_3)
* [八，CCXT市场行情](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label7)
  * [一，价格行情](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label7_0)
  * [二，实时行情数据结构](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label7_1)
  * [三，查询指定交易对实时行情](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label7_2)
* [九，CCXT烛线图数据](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label8)
  * [一，OHLCV烛线图](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label8_0)
  * [二，OHLCV烛线数据结构](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label8_1)
  * [三，OHLCV数据的模拟](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label8_2)
* [十，CCXT数字货币交易](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9)
  * [一，查询交易](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_0)
  * [二，交易身份验证](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_1)
  * [三，API Key设置](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_2)
  * [四，查询账户余额](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_3)
  * [五，查询委托单](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_4)
  * [六，查询交易](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_5)
  * [七，委托单缓存](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_6)
  * [八，清理缓存的委托单](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_7)
  * [九，查询指定ID的委托单](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_8)
  * [十，查询全部委托单 - fetchOrders](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_9)
  * [十一，查询全部敞口委托单](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_10)
  * [十二，查询全部已完结委托单](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_11)
  * [十三，委托单数据结构](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_12)
  * [十四，委托下单](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_13)
  * [十五，市价委托](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_14)
  * [十六，市价买入委托的特殊情况](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_15)
  * [十七，用限价单模拟市价单](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_16)
  * [十八，限价委托](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_17)
  * [十九，委托单的自定义参数](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_18)
  * [二十，其他类型的委托单](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_19)
  * [二十一，取消委托单](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_20)
  * [二十二，委托单与交易的关系](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_21)
  * [二十三，查询个人的历史交易](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_22)
  * [二十四，交易的数据结构](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_23)
  * [二十五，获取充值地址](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_24)
  * [二十六，地址的数据结构](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_25)
  * [二十七，提现](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_26)
  * [二十八，链上交易数据结构](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_27)
  * [二十九，查询充值记录](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_28)
  * [三十，查询提现记录](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_29)
  * [三十一，查询链上交易](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_30)
  * [三十二，查询手续费](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_31)
  * [三十三，查询交易所状态](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_32)
  * [三十四，预算交易费](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_33)
  * [三十五，资金操作费](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_34)
  * [三十六，查询账本](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_35)
  * [三十七，账本记录结构](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_36)
  * [三十八，修改Nonce值](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label9_37)
* [十一，CCXT错误处理](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label10)
  * [一，错误处理概述](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label10_0)
  * [二，异常类的体系](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label10_1)
  * [三，交易所异常](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label10_2)
  * [四，网络异常](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_label10_3)

## CCXT <a id="ccxt"></a>

[Top~~](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_labelTop)

## 一，简介

* JavaScript / Python / PHP加密货币交易API，支持超过120个比特币/山寨币交换
* 提供对市场数据的快速访问，以进行存储，分析，可视化，指标开发，算法交易，策略回测，自动程序编程和相关软件工程。
* 旨在供编码人员，开发人员，技术熟练的交易员，数据科学家和财务分析人员用来构建交易算法。

[Top~~](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_labelTop)

## 二，特点

* 支持许多加密货币交易所
* 完全实现的公共和私有API
* 用于交叉交换分析和套利的可选规范化数据
* 开箱即用的统一API，非常易于集成
* 可在Node 7.6 +，Python 3，PHP 5.4+和Web浏览器中使用

[Top~~](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_labelTop)

## 三，安装

```text
pip install ccxt
```

[Top~~](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_labelTop)

## 四，用法

### 一，介绍

CCXT库由公共部分和私有部分组成。安装后，任何人都可以立即使用公共部分。公共API无需注册用户帐户或拥有API密钥即可为所有交易所市场提供对公共信息的无限制访问。

公共API包括以下内容：

* 市场数据
* 交易对
* 价格饲料（汇率）
* 订购书
* 交易历史
* 股票行情
* OHLC（V）用于制图
* 其他公共端点

为了与私有API进行交易，您需要从交易所的网站获取API密钥。通常，这意味着注册交换并为您的帐户创建API密钥。一些交易所要求提供个人信息或身份证明。有时也可能需要验证。在这种情况下，您需要注册自己，该库不会为您创建帐户或API密钥。一些交易所公开用于注册帐户的API端点，但是大多数交易所没有。您将必须在他们的网站上注册并创建API密钥。

专用API允许以下内容：

* 管理个人帐户信息
* 查询账户余额
* 通过订立市场和限价单进行交易
* 存入和提取法定和加密货币资金
* 查询个人订单
* 获取分类账历史
* 在账户之间转移资金
* 使用商家服务

### 二，接口

```python
# 公有接口：
	loadMarkets            加载市场数据
	fetchMarkets           卖方市场
	fetchCurrencies        货币行情
	fetchTicker            取款行情
	fetchTickers           
	fetchOrderBook         订单簿
	fetchOHLCV             获取历史数据
	fetchStatus            获取状态
	fetchTrades            获取交易数据
# 私有接口：
	fetchBalance           查询余额
	createOrder            创建订单
	cancelOrder            取消订单
	fetchOrder             获取订单
	fetchOrders            获取所有订单
	fetchOpenOrders        获取打开的订单
	fetchClosedOrders      获取关闭的订单
	fetchMyTrades          获取我的交易记录
	deposit                存款
	withdraw               取款
# 也可以自己实现自定义API接口。
# ccxtpro实现了websocket的接口。
# 除了基本的市价委托单和限价委托单，有些交易所还支持杠杆交易和衍生品交易（例如期货合同和期权）， 以及暗池、场外交易（OTC）、商户API等更多服务。
```

### 三，实例化CCXT交易所类

要在代码中连接到交易所并开始交易数字货币，你首先需要利用ccxt库实例化一个交易所类。

**一，查询支持的交易所**

```python
# -*- coding: utf-8 -*-
import ccxt

print(ccxt.exchanges)
```

**二，交易所类的实例化**

```python
# -*- coding: utf-8 -*-
import ccxt

exchange = ccxt.okcoin()  # 默认id
okcoin1 = ccxt.okcoin({'id': 'okcoin1'})
okcoin2 = ccxt.okcoin({'id': 'okcoin2'})

id_ = 'okcoin'
okcoin3 = eval('ccxt.%s()' % id_)
okcoin4 = getattr(ccxt, 'okcoin')()

exchange_id = 'binance'
exchange_class = getattr(ccxt, exchange_id)
exchange2 = exchange_class()
exchange3 = exchange_class({
    'apiKey': 'YOUR_API_KEY',
    'secret': 'YOUR_SECRET',
    'timeout': 30000,
    'enableRateLimit': True,
})
print(exchange.id, okcoin1.id, okcoin2.id, okcoin3.id, okcoin4.id, exchange2.id)
```

#### **三，设置交易所的属性**

CCXT中交易所对象的大多数属性都可以在实例化时设置（也可以在实例化之后设置）

```python
# -*- coding: utf-8 -*-
import ccxt

exchange = ccxt.binance({
    'rateLimit': 10000,  # 统一的交易所属性
    'options': {
        'adjustForTimeDifference': True,  # 特定的交易所属性
     }
})
print(exchange.rateLimit)
print(exchange.options['adjustForTimeDifference'])
exchange.rateLimit = 12000
exchange.options['adjustForTimeDifference'] = False
print(exchange.rateLimit)
print(exchange.options['adjustForTimeDifference'])
```

### 四，交易所数据结构

每个交易所都有一组属性和方法，其中绝大部分都可以在创建交易所对象时， 使用一个关联数组类型的参数来覆盖默认的设置。也可以定义一个继承类 任意覆盖父类的逻辑。

下面是交易所基类的属性概览，其中的值用于演示：

↓ShowCode↓

* id: 每个交易所都有一个默认id，它是一个字符串常量，用于在ccxt中唯一的标识一个特定的交易所实例。 你可以有多个接入同一个交易所的ccxt交易所实例，可以使用id进行区分。默认的交易所id是全小写字符， 对应交易所的名称。
* name：方便人类查看的交易所名称，字符串常量。
* countries: 国别代码字符串数组，每个成员都是2个字符长的ISO国别代码，表示交易所的运营所在地。
* urls\['api'\]: 用于ccxt调用的交易所API url字符串，或者是包含了公开和私有API url的关联数组。
* urls\['www'\]: 交易所的官网URL
* urls\['doc'\]: 交易所API文档的官方URL，可以是单个url或url数组。
* version: 当前使用的交易所API的版本号，CCXT在调用交易所API时将在每个请求的URL中添加这个版本号。 除非你要实现一个新的交易所API，否则你不需要修改这个字段。
* api: 一个包含了交易所的所有API访问端结点的关联数组。ccxt使用这个API定义为每个可用访问端结点 自动构造交易所实例方法。
* has: 描述交易所特性支持能力的关联数组，例如 fetchTickers、fetchOHLCV 或CORS。
* timeframes: 交易所的fetchOHLCV方法支持的时间尺度，关联数组，键为时间尺度缩写。只有当 \['fetchOHLCV'\]属性为真时，ccxt才会填充这个字段的内容。
* timeout: ccxt访问交易所API时，请求-响应的超时设置，单位：毫秒，默认值：10000，即10秒。你 应当根据自己的网络情况进行适当的设置。
* rateLimit: 交易所API的请求限流，单位：毫秒，表示向同一交易所发出的两次请求之间需要的最小延迟间隔。 默认情况下ccxt禁用内置的限流功能，可以通过设置`enableRateLimit`来启用API访问限流。
* enableRateLimit: 是否启用内置的限流机制，布尔值，默认值：false。调用者需要开启内置的限流机制 或者自己实现限流，以避免被交易所禁止访问。
* userAgent: 用于设置HTTP请求头中的User-Agent。ccxt默认会设置自己的User-Aget，有些交易所可能 不允许ccxt访问，你可以将这个值设置为false、undefined或空字符串。
* verbose: 是否记录HTTP请求信息到标准输出设备，布尔值，默认：false。Python开发者可以使用提单的 日志调试方法，方法时在代码开头添加以下代码：

  ```text
  import logging
  logging.basicConfig(level=logging.DEBUG)
  ```

* markets: 市场描述关联数组，键为交易对或交易符号。在访问这个属性之前需要先调用`loadMarkets()`或 `load_markets()`载入市场数据。
* symbols: 交易所的有效符号的数组，以字母表顺序排列。这些符号是市场对象的键，可以用来方便地 访问指定的市场。
* currencies: 交易所的有效数字货币的关联数组，键为数字货币的代码（3~4字母）。数字货币从市场 载入。
* markets\_by\_id: 按交易所列举的市场关联数值。在访问此属性之前需要先载入市场。
* proxy: 用来访问交易所的http\(s\)代理的URL字符串，例如'[http://crossorigin.me/'，默认值：'](http://crossorigin.me/'%EF%BC%8C%E9%BB%98%E8%AE%A4%E5%80%BC%EF%BC%9A')'。
* apiKey: 用来访问交易所的API Key。大部分交易所需要API Key才能访问其API。
* secret: 用来访问交易所的密文。大部分交易所需要同时提供api key和密文。
* password: 交易所要求的交易密码。有些交易所在交易时要求提供这个密码，但是大多数交易所不需要。
* uid: 你的交易所账户的唯一ID。可以是字符串或数。有些交易所在交易时也需要提供这个信息，但是大多数交易所不需要。
* requiredCredentials: 统一的身份信息关联数组，定义需要哪些身份信息才能访问交易所的私有API。
* options: 一个针对特定交易所的关联数组，定义该交易所支持的特定的选项。
* precisionMode: 交易所的小数精度模式。
* has: 描述交易所支持特性的关联数组，例如：

  ↓ShowCode↓

  特性的值为`true`、`false`或`emulated`，其含义如下：

  * true表示该特性是交易所API原生支持的，并且在cctx库中通过统一API提供访问接口
  * false表示该特性不是交易所API原生支持的，并且在cctx库中没有访问该特性的统一API
  * emulated表示该特性不是交易所API原生支持的，但是cctx库通过统一API提供了该特性

### 五，交易所API限流

交易所通常都有限流机制。交易所会记录、跟踪你的身份和IP地址， 不允许你过于频繁的访问其API。通过限流措施，交易所可以对访问流量 进行负载均衡，以此保护其API服务被DDOS攻击或被滥用。

**警告**：为了避免你的账号或IP被封，不要超过交易所的流量限制！

大多数交易所允许每秒1到2个请求。如果你的访问过于有攻击性，交易所可能 会临时限制你访问其API或者封掉你的IP一段时间。

`exchange.rateLimit`属性被设置为一个安全的默认值，这是次优的选择。 有些交易所可能针对不同的访问端结点有不同的限流规则。ccxt的用户需要根据 应用的特定目的来修改rateLimit属性。

CCXT库有内置的实验性质的限流器，可以在后台实现访问节流，这一过程 对调用者是透明的。

**警告**：CCXT的用户应当至少启用一种限流机制：要么 实现自己的自定义限流算法，要么使用内置的限流器。

使用`.enableRateLimit`属性启用内置的限流器，例如： 下面的JavaScript代码在创建交易所实例时启用内置的限流器：

```text
# 在实例化交易所类时启用内置速率限制
exchange = ccxt.bitfinex({
    'enableRateLimit': True,
})

# 或者在实例化之后打开或关闭内置速率限制器
exchange.enableRateLimit = True  # 打开
exchange.enableRateLimit = False  # 关闭
```

如果你的调用达到了限流门槛或者返回nonce错误，ccxt库将抛出以下异常之一：

* DDoSProtectionError：DDOS保护错误
* ExchangeNotAvailable：交易所不可用
* ExchangeError：交易所错误
* InvalidNonce：无效的Nonce值

通常在稍晚时候再重试访问即可解决问题。

### 六，DDoS保护异常及处理办法

有些交易所使用Cloudflare或Incapsula的DDoS保护，在交易所处于高负载时 你的IP会被临时阻断，有时他们甚至限制你所在的整个国家和地区的访问。 在这种情况下他们的服务器通常会返回一个页面声明HTTP 40x错误或者 返回一个AJAX测试或验证码，然后推迟几秒钟才载入页面得到临时的访问 许可或者被添加到一个白名单中。

触发DDoS保护、限流或位置过滤的最常见表现有：

* 调用交易所对象的各种方法都返回RequestTimeout异常
* 捕捉到的`ExchangeError`或`ExchangeNotAvailable`异常，其HTTP错误码为400, 403, 404, 429, 500, 501, 503, 等等。
* 出现DNS解析问题、SSL证书问题和底层连接问题
* 从交易所API返回HTML页面而非JSON对象

如果你遇到DDoS保护错误，并且无法访问特定的交易所，那么可以尝试如下方法：

* 尝试使用cloudscraper:

  ↓ShowCode↓

* 使用一个代理服务器（不过会导致响应变慢）
* 要求交易所的技术支持人员将你加入白名单
* 在临近交易所的地方（同国、同城、同数据中心、同机架、同服务器）运行你的软件
* 尝试不同地理位置的其他IP
* 在一组分布网络服务器上运行你的软件

[Top~~](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_labelTop)

## 五，CCXT市场模型

### 一，市场数据结构

交易所是用来交易有价物品的场所。有时被冠以各种不同的术语，例如工具、符号、交易对、货币、股票、商品、合同等， 但是指的都是一个东西 - 交易对、符号或金融工具。

在ccxt库中，每个交易所都提供了多个市场。不同交易所提供的交易市场各有不同，因而也提供了跨交易所的套利机会。一个市场通常指的是一对可交易的数字货币或法币。

在CCXT中，市场模型的数据结构如下：

```text
{
    'id':     ' btcusd',  // 市场ID，用来在交易所内区分不同市场的字符串或数字ID
    'symbol':  'BTC/USD', // 市场符号，用来表示交易对的大写的字符串代码
    'base':    'BTC',     // 基础货币代码
    'quote':   'USD',     // 报价货币代码
    'baseId':  'btc',     // 基础货币ID
    'quoteId': 'usd',     // 报价货币ID
    'active': true,       // 是否激活，布尔值，表示这个市场是否可交易
    'precision': {        // 在委托单中金额相关字段（例如价格、数量、成本等）支持的最大小数位数
        'price': 8,       // integer or float for TICK_SIZE roundingMode, might be missing if not supplied by the exchange
        'amount': 8,      // integer, might be missing if not supplied by the exchange
        'cost': 8,        // integer, very few exchanges actually have it
    },
    'limits': {           // 限值，价格、数量和成本等的最高和最低限值，其中：成本 = 价格 * 数量
        'amount': {
            'min': 0.01,  // order amount should be > min
            'max': 1000,  // order amount should be < max
        },
        'price': { ... }, // same min/max limits for the price of the order
        'cost':  { ... }, // same limits for order cost = price * amount
    },
    'info':      { ... }, // 一个用于记录非共性市场属性的关联数组，包括手续费、费率、限制以及其他一般性市场信息
}
```

### 二，数据精度和极限值

不要混淆了精度和限值！精度和最低限值无关。8位精度并不一定意味着最低限值为 0.00000001。反过来也是正确的：最小限值0.0001也不一定意味着精度为4。

**示例1**

```text
(market['limits']['amount']['min'] == 0.05) && (market['precision']['amount'] == 4)
```

上面的代码要求任何委托单的数量必须同时满足以下条件：

* 数量值应当 &gt;= 0.05，例如：

  ```text
  + good: 0.05, 0.051, 0.0501, 0.0502, ..., 0.0599, 0.06, 0.0601, ...
  - bad: 0.04, 0.049, 0.0499
  ```

* 精度最高4位小数，例如：

  ```text
  + good: 0.05, 0.051, 0.052, ..., 0.0531, ..., 0.06, ... 0.0719, ...
  - bad: 0.05001, 0.05000, 0.06001
  ```

**示例2**

```text
(market['limits']['price']['min'] == 0.0019) && (market['precision']['price'] == 5)
```

这个例子中要求任何委托单的价格必须同时满足以下条件：

* 价格应当 &gt;= 0.019，例如：

  ```text
  + good: 0.019, ... 0.0191, ... 0.01911, 0.01912, ...
  - bad: 0.016, ..., 0.01699
  ```

* 价格精度最高5位小数，例如：

  ```text
  + good: 0.02, 0.021, 0.0212, 0.02123, 0.02124, 0.02125, ...
  - bad: 0.017000, 0.017001, ...
  ```

**示例3**

```text
(market['limits']['amount']['min'] == 50) && (market['precision']['amount'] == -1)
```

这个示例要求任何委托单的数量同时满足以下条件：

* 数量应当 &gt;= 50，例如：

  ```text
  + good: 50, 60, 70, 80, 90, 100, ... 2000, ...
  - bad: 1, 2, 3, ..., 9
  ```

* 精度为负数表示应当为10的倍数，例如：

  ```text
  + good: 50, ..., 110, ... 1230, ..., 1000000, ..., 1234560, ...
  - bad: 9.5, ... 10.1, ..., 11, ... 200.71, ...
  ```

### 三，委托单数值要求和格式化方法

ccxt的用户应当始终遵守精度和限值要求！委托单中的值应当满足以下条件：

* 委托单amount &gt; `limits['min']['amount']`
* 委托单amount &lt; `limits['max']['amount']`
* 委托单price &gt; `limits['min']['price']`
* 委托单price &lt; `limits['max']['price']`
* 委托单cost \(amount \* price\) &gt; `limits['min']['cost']`
* 委托单cost \(amount \* price\) &lt; `limits['max']['cost']`
* amount的精度 &lt;= `precision['amount']`
* price 的精度 &lt;= `precision['price']`

有些交易所的委托单可能不会包含上面提到的所有的值。

每个交易所都有它自己的取整、计数和填充模式。

CCXT支持的取整模式有：

* **ROUND** – 取整精度要求之后的小数位
* **TRUNCATE**– 截断精度要求之后的小数位

数值精度计数模式可以使用`exchange.precisionMode`属性访问。

CCXT支持的计数模式包括：

* DECIMAL\_PLACES – 统计所有的数字，99%的交易所使用这种计数模式
* SIGNIFICANT\_DIGITS – 仅统计非零数字，有些交易所（bitfinex等）采用这种模式的计数
* TICK\_SIZE – 有些交易所只允许某个特定值的整数倍（bitmex使用这种模式）

CCXT支持的填充模式包括：

* NO\_PADDING – 无填充，大多数情况下的默认模式
* PAD\_WITH\_ZERO – 使用0字符填充至精度要求

交易所基类包含了`decimalToPrecision`来帮助格式化数值为要求的精度， 它支持不同的取整、计数和填充模式。

↓ShowCode↓

### 四，载入市场清单

大多数情况下，在可以访问其他API方法之前，你都需要先载入特定交易所的市场清单和交易符号。如果你忘记载入市场清单，ccxt库会在你第一次调用统一API前自动载入。ccxt会先后发送两个HTTP请求，第一个请求市场清单， 第二个请求其他数据。

要手工预先载入市场清单，可以调用交易所实例的`loadMarkets ()` 或 `load_markets ()` 方法，该方法返回一个描述市场集合的关联数组，键为交易符号。如果你希望 对业务逻辑有更多控制，那么推荐用这种方法手工载入市场清单。

```text
okcoin = ccxt.okcoinusd()
markets = okcoin.load_markets()
print(okcoin.id, markets)
```

### 五，交易符号和市场ID

市场ID用于在REST请求-响应过程中引用交易所内的交易对。每个交易所 都有不同的市场ID集，因此不可以跨交易所使用市场ID。例如，BTC/USD 交易对在不同的交易所中可能有不同的ID：btcusd、 BTCUSD、XBTUSD、btc/usd、 42 \(数字ID\)、 BTC/USD、 Btc/Usd、 tBTCUSD、 XXBTZUSD等。你不需要 记住或使用市场ID，他们的作用是在交易所模型实现的内部用于HTTP的请求 -响应目的。

CCXT库将不通用的市场ID抽象为标准化的交易符号。交易符号不同于市场ID。 每个市场都采用一个对应的符号来引用，交易符号可以跨交易所使用，这使得 交易符号更适用于跨交易所套利等其他很多应用。

交易符号通常是描述一对交易货币的大写字符串常量，以斜杠间隔两个货币代码。 货币代码是3~4位大写字母，例如 BTC, ETH, USD, GBP, CNY, LTC, JPY, DOGE, RUB, ZEC, XRP, XMR, 等等。有些交易所也有长一些的富有异国风情的货币名称。 在斜杠之前的货币被称为基础货币，之后的被称为报价货币。下面是一些符号的 示例： BTC/USD, DOGE/LTC, ETH/EUR, DASH/XRP, BTC/CNY, ZEC/XMR, ETH/JPY。

有时用户可能会注意到像'XBTM18' 或'.XRPUSDM20180101' 或r "exotic/rare symbols" 之类的交易符号。交易符号并不是一定要有斜杠或者包含货币对的代码。符号字符串 完全取决于市场类型（它是一个现货市场、期货市场、暗池市场或过期市场等等）。 CCXT不鼓励你解析交易符号字符串，你不应该依赖于交易符号的格式，CCXT推荐你 使用市场属性来达成你的应用需求。

市场结构使用符号和ID为键。交易所基类也有内置的方法可以按符号访问市场对象。大多数 API方法需要传入交易符号作为第一个参数。当查询当前价格或委托下单时，也常常 需要你指定一个交易符号。

大多数时候，CCXT用户都是与市场交易符号打交道。如果你访问字典中不存在的 键，就会收获一个异常。

↓ShowCode↓

### 六，货币命名的一致性

不同的交易所在术语定义方面有一些模糊之处，对于新手交易者而言 可能会产生歧义。有些交易所将市场称为交易对，而另一些交易所则 将交易符号称为产品。对于CCXT开发库而言，每个交易所都包含一个 或多个交易市场，每个交易市场有一个ID和一个符号，大多数符号都是 由基础货币和报价货币对组成。

```text
Exchanges → Markets → Symbols → Currencies
```

历史上对同一个交易对曾经使用过各种各样的符号名称。有些数字货币 （例如Dash）甚至名字都改过不止一次。为了在多个交易所之间保持 一致性，ccxt库使用以下已知的符号和货币的替代名称：

* XBT → BTC：XBT比较新，但是BTC在交易所中更常见，而且听起来更像比特币
* BCC → BCH：比特币现金分叉通常使用两个不同的名称：BCC和BCH。BCC有点 不明确，容易和BitConnect搞混。ccxt库会正确地将BCC换成BCH（有些交易所 和聚合器会混淆这两个名字）。
* DRK → DASH：DASH原来叫Darkcoin，然后改名为Dash
* BCHABC → BCH：在2018年11月15日，比特币现金再次分叉，因此，现在有BCH \(BCH ABC\) 和BSV \(BCH SV\)。
* BCHSV → BSV：这对应比台币现金的SV分叉，有些交易所称之为BSV，另一些交易所称之为BCHSV，ccxt使用前者。
* DSH → DASH：The DSH \(Dashcoin\) 和DASH \(Dash\)不是一个东西。有些交易所不恰当地将DASH 标记为DSH，ccxt库对此进行了修正\(DSH → DASH\)，但是只有一个交易所混淆了这两种货币， 绝大多数交易所都正确地区分了这两种货币。记住DASH/BTC和DSH/BTC不一样。
* XRB → NANO：NANO是RaiBlocks的较新的代码，因此，CCXT统一API将在必要时 使用NANO替代较早的XRB。
* USD → USDT：有些交易所，例如Bitfinex、HitBTC等在其列表中将其命名为USD，但是 那些市场实际上交易的是USDT。混淆来自于3个字母的限制或者是其他原因。在实际交易 的货币是USDT而非USD时，CCXT库会将USD替换为USDT。注意，有些交易所同时有 USD和USDT。例如，Kraken有一个USDT/USD交易对。

每个交易所都使用一个关联数组用于数字货币代码的替换，可以通过`exchange.commonCurrencies` 属性访问这个关联数组。有时用户可能会注意到混合大小写或者包含空格的奇怪的货币符号， 之所以使用这些名称是为了解决不同交易所使用一样的符号表示不同的货币而引起的冲突：

首先，我们采集不同交易所关于有疑问的货币代码的所有可用信息。交易所通常有其上市 货币的描述清单，可能在API中，也可能在文档里、知识库里或网站的其他地方。

当我们识别出每个货币代码所表示的数字货币后，我们查看其在CoinMarketCap上的主页。

具有最大市值的货币可以保留自己的货币代码。例如，HOT通常表示Holo或Hydro Protocol。 这种情况下Holo得以继续持有其代码HOT，Hydro Protocol将以其名称作为代码，也就是Hydro Protocol。 因此，可能会有这样的交易对：HOT/USD \(表示Holo\) 和 Hydro Protocol/USD，这表示不同的市场。

如果一个货币的市值未知，或者不足以决定胜出者，我们也考虑交易量以及其他因素。

当决定了胜出的货币之后，所有其他竞争货币的代码都会重新进行映射，并使用`exchange.commonCurrencies` 来进行替换。

不幸的是这还是一个进展中的工作，因为每天都在上市新的货币，也是不是会出现 新的交易所。因此，总之这是一个在快速变化的环境中的没有尽头的自我纠错过程。

### 七，货币命名常见问题及解答

**Q：符号名称是否可能会改变？**

A：简而答之，是的，有时候会改变，但是极少。如果绝对需要修改符号映射并且不可避免的话，就会修改货币命名。然而，所有之前的符号修改都与冲突解析或分叉有关。迄今为止，在CCXT中还没有使用相同符号代码的一种货币的市值被另一种超越的先例。

**Q：我们可以始终用同样的符号表示同一个数字货币吗？**

A：或多或少：）首先，ccxt库本身也在不断前进中，它在尝试适应不断变化的现实，因此可能存在我们将来会通过修改符号映射来解决的冲突。 最后，我们的软件协议指出“不提供担保，自担风险使用”。然而，我们不会随意修改符号映射，因为我们理解随意修改的后果，不希望完全打破后向兼容性。

如果一个主要货币的符号不得不修改，那么控制权依然在用户手中。 `exchange.commonCurrencies`属性的值可以在初始化时或之后修改，就像 exchange对象的其他属性一样。如果涉及到一种重要的数字货币，我们通常会告诉大家如何添加一点代码来保持既有的代码行为。

**Q：基础货币和报价货币的一致性？**

A：这依赖于你使用的是哪个交易所，但是有些交易所的交易对是反的，它们会把报价货币放在前头而基础货币放在后头。这种情况下你会看到解析后的基础货币和报价货币和解析前是不一样的。

对于这些搞错交易对先后顺序的交易所，ccxt在解析交易所响应时会进行修正。 如果你希望少一些困扰，记住以下规则：基础货币总是在斜杠前，报价货币总是在斜杠后：

```text
base currency ↓
             BTC / USDT
             ETH / BTC
            DASH / ETH
                    ↑ quote currency
```

### 八，市场缓冲强制重载

`loadMarkets ()` / `load_markets ()`是一个有副作用的方法， 它会在exchange实例上保存市场数组。对每个交易所实例你只需要调用一次。所有后续对此方法的调用都会返回本地保存的市场数组。

当载入交易市场后，你可以随时使用`markets`属性访问市场信息，这个属性包含了一个以符号为键的市场关联数组。如果你需要强制重载市场 列表，只需要在调用时设置参数`reload`为`true`即可。[Top~~](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_labelTop)

## 六，CCXT API

### 一，API方法与访问端节点

每个交易所对象都提供了一组API方法。API的每个方法被称为一个访问端结点， 它指的是用于查询各种信息的HTTP URL。所有的访问端结点都返回JSON响应。

通常有一个访问端结点用于获取交易所的市场列表，一个访问端结点用于提取特定市场的交易委托账本，一个访问端结点用于提取交易历史，一组访问点用于 下单或取消委托单、充值或提现等等... 基本上你在交易所里可以进行的操作 都会有一个API提供出来供你调用。

因为不同交易所的方法集彼此不同，ccxt库实现了以下功能：

* 为所有可能的URL和方法提供公开和私有API
* 提供一个统一的API支持各交易所的共同的方法

端结点URL在每个交易所的`api`属性中预定义。你不需要重载这个属性，除非 你要实现一个新的交易所API（至少你需要了解你要做什么）。

### 二，隐式API方法

大多数交易所特定的API方法都是隐含的，意思是这些方法没有在代码中显式地定义。ccxt库采用声明式的方法来定义隐含的交易所API方法。

API的每个方法通常都有自己的访问端结点。ccxt库为每个交易所都定义了所有的访问端结点，你可以通过`.api`属性访问。在创建交易所对象时， 在`defineRestApi()` / `define_rest_api()`中将会为`.api`列表中的 每个url创建一个隐含的魔术方法（即偏函数或闭包）。这个环节在所有交易所上都是统一的。生成的每个方法都可以驼峰写法和下划线写法来访问。

访问点定义指的是一个交易所暴露出来的所有的API的URL的完整的列表。 这个列表将在交易所对象初始化时转化为可调用的方法。在API访问端结点 列表中的每个URL都有一个对应的可调用方法。对于所有的交易所而言，这 都是自动进行的，因此ccxt库支持数字货币交易所的所有可能的URL。

每个隐含的方法都有一个唯一的名字，这个名字是利用`.api`中的定义生成的。 例如，对于一个私有HTTPS PUT访问端结点`https://api.exchange.com/order/{id}/cancel`， 其对应的隐含方法名为`.privatePutOrderIdCancel()` / `.private_put_order_id_cancel()`。 对于一个公开的HTTPS GET访问端结点`https://api.exchange.com/market/ticker/{pair}`， 其对应的隐含方法名为`.publicGetTickerPair()` / `.public_get_ticker_pair()`，依次类推。

隐含方法接收传入的参数字典，将请求发送到交易所，然后返回交易所特定的未解析 的JSON结果。要传入一个参数，将其添加到字典中与参数同名的键下即可。例如对于 上面的例子，就是像`.privatePutOrderIdCancel ({ id: '41987a2b-...' })` 和`.publicGetTickerPair ({ pair: 'BTC/USD' })`。

ccxt推荐的与交易所交互的方式，并不是使用交易所特定的隐含方法，而是使用ccxt 提供的统一方法。只有当ccxt的统一api中没有提供相应的方法时，才应当使用隐含的方法作为后备方案。

要获得指定交易所实例的所有可用方法，包括隐含方法和统一方法，你可以 使用如下的简单代码。

```text
print(dir(ccxt.hitbtc()))
```

### 三，公开/私有API

API的URL通常分为两类：市场数据方面的公开API，以及交易和账户相关的私有API。 这两组API的方法通常分别使用前缀`public`和`private`。

**公开API**

公开API用来访问市场数据，不需要进行身份验证。大多数交易所为所有用户提供开放的市场数据（通常有一定的限流措施）。使用ccxt库，任何人都可以直接访问市场数据，而无需在交易所进行注册，也无需设置api key 和密码。

公开API包含如下内容：

* 交易对
* 价格流
* 委托账本（L1、L2、L3...）
* 交易历史（完成的订单、交易、执行）
* 行情数据（现价、24小时价格）
* 用于图表的OHLCV序列数据
* 其他公开访问点

**私有API**

要使用私有API进行交易，你需要从交易所获取API key。这通常意味着你需要在交易所注册并使用你的账户创建API key。大多数交易所需要个人信息或身份标识，一些身份验证也是必要的。

如果你希望交易，首先需要在交易所进行注册，ccxt库不会创建账户或者提供 API key。有些交易所的API提供了在代码中注册账户的接口，但是大多数交易所 都没有这样的接口。你必须在交易所的网站注册并创建API key。

私有API包含以下内容：

* 管理个人账户信息
* 查询账户余额
* 委托市价单和限价单
* 创建充值地址并进行账户充值
* 请求提取法币和加密货币
* 查询个人的关闭/完结委托单
* 查询杠杆交易的位置
* 获取账本历史
* 在不同账户之间转账
* 使用商户服务

有些交易所的相同服务采用了不同的名称。例如，公开API通常称为市场数据、 基础、市场、mapi、api、价格等等...所有这些指的都是一组用于访问公开 可用数据的方法。私有API通常称为trading、trade、tapi、exchange、account 等等。

有些交易所也暴露出商户API，可以让你创建发票并接收你的客户的数字货币和法币支付。 这一类API通常称为merchant、wallet、payment、ecapi（用于电子商务的API）。

### 四，同步调用与异步调用

Python版本的ccxt库使用async/await语法支持Python 3.5+的异步并发模式。 异步的Python版本使用aiohttp实现纯异步io。在异步模式下所有的属性和 方法名还是一样的，只是大多数方法都有async关键字装饰。如果你希望使用 异步模式，应当链接ccxt.async\_support子包，如下例所示：

```text
import asyncio
import ccxt.async_support as ccxt

async def print_poloniex_ethbtc_ticker():
    poloniex = ccxt.poloniex()
    print(await poloniex.fetch_ticker('ETH/BTC'))

asyncio.get_event_loop().run_until_complete(print_poloniex_ethbtc_ticker())
```

### 五，调用参数与返回值

所有的公开和私有API方法都返回交易所响应的原始的JSON对象，也就是 说没有解析的原始响应结果。统一API返回公共格式的JSON对象，在所有交易所上都保持统一的结构。

所有可能的API访问端结点集合对于每个交易所都不一样。大多数方法接收单一的关联数组（或Python字典）表示的键-值参数。传参方法如下所示：

```text
ccxt.zaif().public_get_ticker_pair ({ 'pair': 'btc_jpy' })  # Python
```

### 六，API方法命名规范

交易所方法名是由以下字符串拼接而成：

* 类型：public或private
* HTTP方法：GET、POST、PUT、DELETE
* 访问端结点URL

示例如下：

| 方法名 | API URL基地址 | 端结点URL |
| :--- | :--- | :--- |
| publicGetIdOrderbook | [https://bitbay.net/API/Public](https://bitbay.net/API/Public) | {id}/orderbook |
| publicGetPairs | [https://bitlish.com/api](https://bitlish.com/api) | pairs |
| publicGetJsonMarketTicker | [https://www.bitmarket.net](https://www.bitmarket.net/) | json/{market}/ticker |
| privateGetUserMargin | [https://bitmex.com](https://bitmex.com/) | user/margin |
| privatePostTrade | [https://btc-x.is/api](https://btc-x.is/api) | trade |
| tapiCancelOrder | [https://yobit.net](https://yobit.net/) | tapi/CancelOrder |
| ... | ... | ... |

ccxt库同时支持驼峰命名法（JavaScript常用）和下划线命名法（Python和PHP常用）， 因此所有的方法在任何开发语言中都可以上述两种风格之一调用：

```text
exchange.methodName ()  // 驼峰式伪代码
exchange.method_name () // 下划线式伪代码
```

### 七，统一API

ccxt统一API是所有交易所中的公共方法的集合。目前统一API包含以下方法：

* fetchMarkets\(\)： 从交易所提取所有有效市场的清单，返回市场对象数组。有些交易所没有办法通过其在线API获取市场清单，CCXT采用硬编码的方式返回这些交易所的市场清单。
* loadMarkets\(\[reload\]\)：返回对象形式的市场清单并在交易所实例上缓存，键为交易符号。如果之前已经载入过，则从缓存中返回结果，除非是强制使用了`reload`标志并设置为`true`。
* fetchOrderBook\(symbol\[, limit = undefined\[, params = {}\]\]\)：获取指定市场交易符号的L2/L3委托账本
* fetchStatus\(\[, params = {}\]\)：返回交易所状态信息，可能使用API或者硬编码实现
* fetchL2OrderBook\(symbol\[, limit = undefined\[, params\]\]\)：获取交易符号的2层（价格聚合）委托账本
* fetchTrades\(symbol\[, since\[, \[limit, \[params\]\]\]\]\)：获取指定交易符号的最近交易
* fetchTicker\(symbol\)：获取指定交易符号的最新行情数据
* fetchBalance\(\)：获取余额数据
* createOrder\(symbol, type, side, amount\[, price\[, params\]\]\)
* createLimitBuyOrder\(symbol, amount, price\[, params\]\)
* createLimitSellOrder\(symbol, amount, price\[, params\]\)
* createMarketBuyOrder\(symbol, amount\[, params\]\)
* createMarketSellOrder\(symbol, amount\[, params\]\)
* cancelOrder\(id\[, symbol\[, params\]\]\)
* fetchOrder\(id\[, symbol\[, params\]\]\)
* fetchOrders\(\[symbol\[, since\[, limit\[, params\]\]\]\]\)
* fetchOpenOrders\(\[symbol\[, since, limit, params\]\]\]\]\)
* fetchClosedOrders\(\[symbol\[, since\[, limit\[, params\]\]\]\]\)
* fetchMyTrades\(\[symbol\[, since\[, limit\[, params\]\]\]\]\)
* ...

### 八，改写统一API的参数

注意，统一API的大部分方法都可以接受一个可选的`params`参数，它是一个 关联数组（字典，默认为空），包含了你希望改写的参数。`params`的内容 是与特定交易所相关的，参考交易所的API文档了解其支持的字段和值。如果 你需要传入自定义设置或可选的参数，那么可以使用`params`字典。

```text
params = {
    'foo': 'bar',       # exchange-specific overrides in unified queries
    'Hello': 'World!',  # see their docs for more details on parameter names
}

# overrides go in the last argument to the unified call ↓ HERE
result = exchange.fetch_order_book(symbol, length, params)
```

### 九，统一API结果的分页

大多数统一API的方法会返回单一对象或对象数组（交易、委托单等）。 然而，极少数交易所会一次返回全部委托单、全部交易或全部ohlcv烛线图数据。 更常见的是交易所API会限制返回一定数量的最新对象，你不能一次调用就 获取从开始时间到当前时刻的全部对象。实际上，极少有交易所能容忍或允许 这样的调用。

要获取历史委托单或交易，用户需要分页遍历数据。分页通常表示要循环 提取部分数据。

在大多数情况下，用户需要使用某种类型的分页来获取期望的结果。如果 用户没有使用分页，大多数方法将返回交易所的默认结果，这可能是从历史 的开始时刻或者也可能是返回最近的一部分数据。默认行为是交易所相关的！ 分页通常会在以下方法中用到：

* fetchTrades
* fetchOHLCV
* fetchOrders
* fetchOpenOrders
* fetchClosedOrders
* fetchMyTrades
* fetchTransactions
* fetchDeposits
* fetchWithdrawals

对于返回对象列表的方法，交易所可能提供一种或多种分页类型。CCXT默认 统一了基于日期、基于毫秒时间戳的分页。

**用于UTC日期和时间戳的方法集：**

```text
exchange.parse8601 ('2018-01-01T00:00:00Z') == 1514764800000 # UTC时间转换为毫秒时间戳
exchange.iso8601 (1514764800000) == '2018-01-01T00:00:00Z'   # 毫秒时间戳转换为UTC时间
exchange.seconds ()      # 秒级时间戳
exchange.milliseconds () # 毫秒级时间戳
```

**一，基于日期的分页**

这是目前CCXT统一API使用的分页类型。调用者提供一个毫秒时间戳作为`since` 参数的值，同时传入一个数值来限定返回结果的数量。要逐页遍历感兴趣的对象， 调用者运行如下的伪代码。

```text
if  exchange.has['fetchOrders']:
    since = exchange.milliseconds() - 3600*24*1000  # 一天前
    # since = exchange.parse8601('2020-10-10T00:00:00Z')
    all_orders = []
    while since < exchange.milliseconds():
        symbol = None
        limit = 20
        orders =  exchange.fetch_orders(symbol, since, limit)
        print(len(orders))
        if len(orders):
            since = orders[len(orders) - 1]['timestamp']
            all_orders += orders
        else:
            break
    print(all_orders)
```

**二，基于ID的分页**

调用者提供对象的`from_id`，以及一个用于限定返回结果数量的值。这是一些交易所 的默认行为，然而，这一分页类型目前还不是统一的。要基于ID进行分页，调用者可以 运行如下伪代码：

```text
if exchange.has['fetchOrders']:
    from_id = 'abc123'  # all ids are strings
    all_orders = []
    while True:
        symbol = None  # change for your symbol
        since = None
        limit = 20  # change for your limit
        params = {
            'from_id': from_id,  # exchange-specific non-unified parameter name
        }
        orders = await exchange.fetch_orders(symbol, since, limit, params)
        if len(orders):
            from_id = orders[len(orders) - 1]['id']
            all_orders += orders
        else:
            break
```

**三，基于页号的分页**

调用者提供一个页号或者初始的游标值。交易所返回一页结果以及后续的游标值以便继续。 大多数实现这种类型分页的交易所，在响应内容或响应头中返回下一个游标。在每个迭代周期，调用者必须拿到下一个游标并将其传入下一次迭代的查询。

```text
if exchange.has['fetchOrders']:
    cursor = 0  # exchange-specific type and value
    all_orders = []
    while True:
        symbol = None  # change for your symbol
        since = None
        limit = 20  # change for your limit
        params = {
            'cursor': cursor,  # exchange-specific non-unified parameter name
        }
        orders = await exchange.fetch_orders(symbol, since, limit, params)
        if len(orders):
            # not thread-safu and exchange-specific !
            cursor = exchange.last_http_headers['CB-AFTER']
            all_orders += orders
        else:
            break
```

[Top~~](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_labelTop)

## 七，CCXT委托账本模型

### 一，交易委托账本

交易所会提供敞口委托单的买入/卖出价格、交易量以及其他数据。 通常对每一个特定的市场都会有一个单独的访问端接点来查询交易委托账本的状态。 交易委托账本经常被称为市场深度。委托账本信息可以用于交易决策过程。

获取指定符号的交易委托账本的方法是`fetchOrderBook`或`fetch_order_book`。 该方法的参数是交易符号以及一个可选的参数字典（如果该交易所支持的话）。 调用方法示例代码如下。

```text
import time
delay = 2 # seconds
for symbol in exchange.markets:
    print (exchange.fetch_order_book (symbol))
    time.sleep (delay) # rate limit
```

### 二，委托账本模型的结构

ccxt返回的委托账本结构如下：

```text
{
    'bids': [
        [ price, amount ], // [ float, float ]
        [ price, amount ],
        ...
    ],
    'asks': [
        [ price, amount ],
        [ price, amount ],
        ...
    ],
    'timestamp': 1499280391811, // Unix Timestamp in milliseconds (seconds * 1000)
    'datetime': '2017-07-05T18:47:14.692Z', // ISO8601 datetime string with milliseconds
}
```

如果查询的交易所在其API响应中没有提供时间戳和日期值，那么在返回的结果 中时间戳和日期的值可能也会缺失（undefined/None/null）。

Price和amount都是浮点数。`bids`数组按价格降序排列，最高的买入价格排在第一个，最低的 买入价格排在最后一个。`asks`数组按价格升序排列，最低的卖出价格排在第一个，最高的卖出 价格排在最后一个。bids/asks数组可以是空的，表示交易所的委托账本中没有相应 的委托单。

交易所可能返回用于分析的不同层级的委托单，结果中要么包含每个订单的详情，要么 已经按照价格和交易量进行了分组聚合因而其中的详情信息要少一些。越多的详情信息 就需要越多的带宽，因此总体上会更慢一些，但是好处在于有更高的精度。较少的详情 信息通常会快一些，但是可能在某些特定情况下不够用。

`orderbook['timestamp']`是交易所生成这个响应的时间，可能会缺失（undefined/None/null）。 如果交易所有定义的话，那么它是一个UTC时间戳，以毫秒为单位，记录子1970年1月1日零点 以来的毫秒数。

### 三，市场深度

有些交易所接受一个字典对象来将额外的参数传入`fetchOrderBook ()` / `fetch_order_book ()`函数。 所有额外的参数都是交易所特定的（不统一）。如果要设置特定的参数，例如交易账本的深度，那么 你需要查阅交易所的文档。你可以使用如下代码获取指定数量的委托单或指定层级的聚合（即市场深度）。

```text
import ccxt
# return up to ten bidasks on each side of the order book stack
limit = 10
ccxt.cex().fetch_order_book('BTC/USD', limit)
```

委托账本聚合的层级或详情通常是数字标注的，就像L1、L2、L3...

* L1：较少的详情，用于快速获取非常基本的信息，也就是仅市场价格。看起来就像在委托账本中仅包含一个委托单。
* L2：最常用的聚合层级，委托单交易量按价格分组。如果两个委托单有相同的价格，那么他们会合并为一项，其总量 为这两个委托单的交易量的和。这个聚合层级可能适合大部分的应用目的。
* L3：最详细的层级，包含所有的订单，没有聚合。这一层级自然包含了输出中的重复内容。因此，如果两个订单 有相同的价格，它们也不会合并在一起，这两个订单的优先级则取决于交易所的撮合引擎。你不一定真的需要 L3详情来进行交易。实际上，大多数情况下你根本不需要这么详细的信息。因此有些交易所不支持这个级别的数据， 总是返回聚合后的委托账本。

如果你想获取L2委托账本，可以使用统一API中的`fetchL2OrderBook(symbol, limit, params)` 或 `fetch_l2_order_book(symbol, limit, params)`方法。

### 四，获取市场价格

为了获取当前的最好价格（查询市场价格）并且计算买入卖出的价差， 可以使用如下代码。

```text
orderbook = exchange.fetch_order_book (exchange.symbols[0])
bid = orderbook['bids'][0][0] if len (orderbook['bids']) > 0 else None
ask = orderbook['asks'][0][0] if len (orderbook['asks']) > 0 else None
spread = (ask - bid) if (bid and ask) else None
print (exchange.id, 'market price', { 'bid': bid, 'ask': ask, 'spread': spread })
```

[Top~~](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_labelTop)

## 八，CCXT市场行情

### 一，价格行情

价格行情包含了最近一段时间内特定交易市场的统计信息，通常使用24小时进行统计。 查询价格行情的方法如下：

```text
fetchTicker (symbol, params = {})   // for one ticker
fetchTickers (symbol, params = {})  // for all tickers at once
```

检查交易所的`exchange.has['fetchTicker']`和 `exchange.has['fetchTickers']`属性 来决定所查询的交易所是否支持这些方法。

### 二，实时行情数据结构

行情的数据结构如下：

↓ShowCode↓

时间戳和日期都是以毫秒为单位的UTC时间值：

* ticker\['timestamp'\] 是交易所生成响应的时间，有的交易所可能没有这个值，因此在结果中会缺失
* exchange.last\_response\_headers\['Date'\] 是收到的最后一个HTTP响应的日期-时间字符串。`Date`解析器 应当考虑时区问题。日期-时间的精度是1秒、1000毫秒。

虽然有些交易所在其行情数据中混入了委托账本的最高买入/最低卖出价格，你不应当将 行情数据视为`fetchOrderBook`的替代方法。行情数据的主要目的是提供统计数据，可以 将其视为活跃的24小时OHLCV数据。已知的是，交易所不鼓励频繁地调用`fetchTicker`。 如果你需要一个统一的方法去访问bids和asks，你应当使用`fetchL[123]OrderBook`系列的方法。

要获取历史价格和数量，使用统一API中的`fetchOHLCV`方法。

获取行情数据的方法如下：

* fetchTicker \(symbol\[, params = {}\]\), symbol必须，params可选
* fetchTickers \(\[symbols = undefined\[, params = {}\]\]\), 两个参数都是可选的

### 三，查询指定交易对实时行情

要查询指定交易对/符号的实时行情数据，调用`fetchTicker(symbol)`方法。

```text
import random
if (exchange.has['fetchTicker']):
    print(exchange.fetch_ticker('LTC/ZEC')) # ticker for LTC/ZEC
    symbols = list(exchange.markets.keys())
    print(exchange.fetch_ticker(random.choice(symbols))) # ticker for a random symbol
```

有些交易所（不是所有）也支持同时查询所有交易对的实时行情。请查阅 交易所的文档获取详细信息。你可以在一次调用中获取所有的实时行情。

```text
if (exchange.has['fetchTickers']):
    print(exchange.fetch_tickers()) # all tickers indexed by their symbols
```

查询所有的实时行情需要更多的流量，另外，也要注意有些交易所对后续的查询会有更严格的限流。 还有一些交易所可能会对`fetchTickers()`的调用有更多的要求，有时你无法查询的原因是API的限制。 另外一些交易所可以在URL查询参数中接受一组交易对符号，但是由于URL的长度是有限的，在极端 情况下交易所可以有数千个市场 - url的长度无法容纳所有的交易对符号。

```text
if (exchange.has['fetchTickers']):
    print(exchange.fetch_tickers(['ETH/BTC', 'LTC/BTC'])) # listed tickers indexed by their symbols
```

注意在大多数情况下交易对符号列表不是必须的，但是如果你要处理所有可能的情况就需要额外的逻辑处理。

和CCXT统一API中的大多数方法一样，`fetchTickers`的最后一个参数是`params`，用来修改发送到 交易所的请求参数。

返回结果的结构如下：

```text
{
    'info':    { ... }, // the original JSON response from the exchange as is
    'BTC/USD': { ... }, // a single ticker for BTC/USD
    'ETH/BTC': { ... }, // a ticker for ETH/BTC
    ...
}
```

[Top~~](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_labelTop)

## 九，CCXT烛线图数据

### 一，OHLCV烛线图

大多数交易所都提供了获取OHLCV数据的访问端结点，但还是有一些交易所没有提供。 在ccxt中，交易所对象的`has['fetchOHLCV']`属性表示该交易所是否支持烛线数据序列， 如果这个布尔属性的值为true，则表明支持。

`fetchOHLCV`方法声明如下：

```text
fetchOHLCV (symbol, timeframe = '1m', since = None, limit = None, params = {})
```

你可以调用CCXT统一API的`fetchOHLCV` / `fetch_ohlcv`方法获取指定交易对符号的OHLCV烛线图数据。

```text
import time
if exchange.has['fetchOHLCV']:
    for symbol in exchange.markets:
        time.sleep (exchange.rateLimit / 1000) # time.sleep wants seconds
        print (symbol, exchange.fetch_ohlcv (symbol, '1d')) # one day
```

要获取所查询的交易所的可用时间窗，可以查看交易所对象的`timeframes`属性。 注意只有当交易所对象的`has['fetchOHLCV']`属性值为true时上述属性才有效。

你的请求能够回溯多久远的数据是有限制的。大多数交易所不会允许你查询太早时间 的详细烛线数据历史（就像1分钟和5分钟的时间窗口内的详情）。他们通常提供 一段合理时间内的烛线数据，例如任何时间窗的最近1000个烛线数据，这对于大多数 应用都是足够了。突破这一限制的办法，是你可以不停地查询（REST Polling）最新 的OHLCV数据，并存储到自己的CSV文件中或者数据库里。

注意最后的（当前）烛线数据可能是不完整的，直到开始记录下一个烛线。

和ccxt的统一api和隐含api中的其他许多方法一样，`fetchOHLCV`方法的最后一个参数 可以传入一个关联数组来设置额外的交易所特定的请求参数，你需要查询交易所的API 文档来了解其支持的字段和值。

`since`参数是一个以毫秒计量的UTC时间戳，如果未指定`since`参数，`fetchOHLCV` 方法将返回交易所默认的时间范围。有些交易所将返回从其开始以来的所有烛线，而另一些 则只会返回最近产生的烛线，这取决于交易所的默认行为。因此如果你不指定`since` 参数，那么返回的烛线的时间范围是交易所相关的，为了得到一致的响应结果，开发者 应当传入`since`参数。

### 二，OHLCV烛线数据结构

`fetchOHLCV`方法返回OHLCV烛线数组，其结构如下：

```text
[
    [
        1504541580000, // UTC 时间戳，单位：毫秒
        4235.4,        // (O)开盘价格, float
        4240.6,        // (H)最高价格, float
        4230.0,        // (L)最低价格, float
        4230.7,        // (C)收盘价格, float
        37.72941911    // (V)交易量，以基准货币计量， float
    ],
    ...
]
```

结果数组是以时间升序排列的，最早的烛线排在第一个，最新的烛线排在最后一个。

### 三，OHLCV数据的模拟

有些交易所没有提供任何OHLCV方法，为此ccxt库将利用公开交易模拟OHLCV烛线数据。 在这种情况下你会看到交易所对象的`has['fetchOHLCV']`属性的值为`emulated`。

但是，由于交易历史通常都非常有限，模拟的`fetchOHLCV`方法只能涵盖最近的信息， 因此只可以作为没有其他可选项是的备选方案使用。

**警告：`fetchOHLCV`方法的模拟目前还是实验性质的！**[Top~~](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_labelTop)

## 十，CCXT数字货币交易

### 一，查询交易

你可以调用ccxt的统一API方法`fetchTrades` / `fetch_trades`来获取指定交易对的最近交易记录。 `fetchTrade`方法声明如下：

```text
fetchTrades (symbol, since = None, limit = None, params = {})
```

例如，如果你希望逐个打印所有交易对的近期交易（别忘了交易所的限流！）， 可以使用以下代码。

```python
import time
if exchange.has['fetchTrades']:
    for symbol in exchange.markets:  # ensure you have called loadMarkets() or load_markets() method.
        time.sleep (exchange.rateLimit / 1000)  # time.sleep wants seconds
        print (symbol, exchange.fetch_trades (symbol))
```

上面展示的`fetchTrades`方法返回一个按时间戳升序排列的交易数组，最早的交易在 第一个，最新的交易在最后一个。交易数组结构如下：

```text
[
    {
        'info':       { ... },                  // the original decoded JSON as is
        'id':        '12345-67890:09876/54321', // string trade id
        'timestamp':  1502962946216,            // Unix timestamp in milliseconds
        'datetime':  '2017-08-17 12:42:48.000', // ISO8601 datetime with milliseconds
        'symbol':    'ETH/BTC',                 // symbol
        'order':     '12345-67890:09876/54321', // string order id or undefined/None/null
        'type':      'limit',                   // order type, 'market', 'limit' or undefined/None/null
        'side':      'buy',                     // direction of the trade, 'buy' or 'sell'
        'price':      0.06917684,               // float price in quote currency
        'amount':     1.5,                      // amount of base currency
    },
    ...
]
```

大多数交易所返回上述交易对象中的大部分字段，虽然也有些交易所不会返回type, side, 交易id或委托单id这些字段 。 大多数时候可以保证你能拿到一个交易的以下字段：timestamp, datetime,symbol, price 和amount 。

第二个可选参数`since`可以按时间戳削减结果数组，第三个参数`limit`可以削减返回的交易数量。

如果用户不指定`since`，那么`fetchTrade`方法将返回交易所默认的公开交易时间范围，这是交易所特定的， 有些交易所会返回自交易对上市开始的所有交易，另一些交易所则会返回缩减集合，例如 最近24小时、或者最近100个交易等等。如果用户希望更精确地控制时间窗口，那么应当指定 `since`参数。

ccxt的统一API中的大多数方法都会返回一个对象或对象数组。然而，也有极少数交易所会一次 返回所有的交易。通常来说交易所的API会限制仅返回最近的一定数量的交易。你不能只用 一个调用就返回自交易对上市依赖的所有交易对象，实际上，很少有交易所会容忍或允许 这种调用行为。

要查询历史交易，开发者需要按页遍历数据。分页通常暗示着使用循环分块提取数据。

大多数情况下，开发者需要使用至少某种类型的分页来获得一致的结果。

另一方面，有些交易所不支持公开交易的分页查询。总体来说交易所会提供最近的交易。

`fetchTrades ()` / `fetch_trades()` 方法也可以接收一个额外的关联数组作为其第四个参数。 你可以用这个关联数组传入特定交易所支持的额外的参数。请查询交易所的API文档获取详细信息。

### 二，交易身份验证

为了能够访问你的账户，通过市价单和限价单执行量化交易，查询余额、充值与提现等等，你需要 从每个你希望操作的交易所获取你的API key以进行身份验证。API key是交易所相关的，任何情况下 不同交易所的API key彼此都不能互换。

如果提供了正确的API key，交易所会自动进行身份验证。验证过程通常采用以下模式：

* 生成一个新的nonce。nonce是一个整数，通常是以秒或者毫秒计的unix时间戳。 nonce应当是单调递增的，因此没有两个请求会使用相同的nonce值。默认的nonce 是以秒计的unix时间戳。
* 将公开的api key和nonce追加到其他访问端结点参数之后，然后序列化以便进行签名
* 使用HMAC-SHA256/384/512 或 MD5 哈希序列化参数，然后用私钥签名
* 将16进制或base64编码的签名和nonce添加到HTTP头或请求内容中

不同的交易所上述过程可能有所区别。有些交易所可能要求其他编码格式的签名，有些则 使用不同的HTTP头参数名和格式，但是基本都是上述模式。

不要在多个线程、进程中同时运行的一个交易所的多个实例之间共享同一个API密钥对， 这可能会导致不可预料的行为。

ccxt已经为你处理了身份验证逻辑，因此你不需要手工进行任何操作，除非你在实现 一个新的交易所类，否则为了进行交易，你唯一需要做的就是提供正确的API密钥对。

### 三，API Key设置

API身份通常包含以下内容：

* apiKey：你的公开的API Key或Token。这部分不是保密的，它包含在你的请求头或请求内容中 用来标识你的请求。apiKey通常是一个16进制或base64编码的字符串，或者是一个UUID。
* secret：这是你的私钥，需要秘密保存，不要告诉任何人。私钥用来在本地签名你的请求， 然后发送请求给交易所。私钥不能通过互联网发出去，也不应该发布或通过电子邮件传递。 私钥和nonce一起来生成在密码学上足够强的签名，这个签名和你的API key一起用来识别 你的身份。每个请求都有唯一的nonce，因此其签名也是唯一的。
* uid：有些交易所也会生成一个较短的用户ID。它可以是字符串或者数字。如果交易所明确 地要求，那么你应该设置这个参数。请参考交易所的文档获取详细信息。
* password：有些交易所也要求你在交易时提供密码。如果交易所明确要求，那么你也应该 照办。请参考交易所的文档获取详细信息。

你可以在交易所的网站上创建API key，然后拷贝到你的配置文件中。记得正确设置配置文件 的权限，不要让其他任何人读取。

记住要保证apiKey和私钥的安全，避免未授权的使用，不要发送或告诉任何人。私钥泄漏 会导致你的财产损失。

要创建可以用于交易的exchange对象，只需将API身份信息赋给已有的交易所实例，或者 在创建交易所实例时指定。参考以下示例代码。

```python
import ccxt

# any time
bitfinex = ccxt.bitfinex ()
bitfinex.apiKey = 'YOUR_BFX_API_KEY'
bitfinex.secret = 'YOUR_BFX_SECRET'

# upon instantiation
hitbtc = ccxt.hitbtc ({
    'apiKey': 'YOUR_HITBTC_API_KEY',
    'secret': 'YOUR_HITBTC_SECRET_KEY',
})

# from variable id
exchange_id = 'binance'
exchange_class = getattr(ccxt, exchange_id)
exchange = exchange_class({
    'apiKey': 'YOUR_API_KEY',
    'secret': 'YOUR_SECRET',
    'timeout': 30000,
    'enableRateLimit': True,
})
```

注意，如果在交易之前你没有设置API身份信息，那么你的私有API请求可能会失败而抛出异常或错误。 为了避免字符的转移问题，请使用单引号描述你的身份信息，例如'VERY\_GOOD'而不是 "VERY\_BAD"。

### 四，查询账户余额

要查询账户余额，获取可用于交易的资金数量，或者锁定在委托单中的资金数量， 可以使用`fetchBalance`方法。

```python
fetchBalance (params = {})
```

方法返回的余额结构如下：

↓ShowCode↓

有些交易所可能不会返回完整的余额信息。许多交易所不会返回你的空账户或者未用的账户， 这种情况下在返回的余额结构中可能会缺少某些货币的信息。

Python示例代码：

```python
print (exchange.fetch_balance ())
```

**余额信息的推导**

有些交易所的API不会返回余额信息的完整集合，它们只会返回可用余额或者只是资金总量。 这种情况下ccxt会尝试从委托单缓存中获取缺失的数据，并根据已知的信息猜测完整的余额信息。 但是这在一些极端情况下可能不足以推导出正确的余额信息，开发者应当了解这种可能性。

### 五，查询委托单

大多数时候，你可以按id或符号查询委托单，虽然不是所有的交易所都提供了完整 和灵活的委托单查询访问端结点。有些交易所可能没有方法查询最近完成的委托单， 另一些可能缺少按id获取委托单的方法，等等。ccxt库考虑了这些情况并尽可能 加以解决。

查询委托单的方法如下：

* fetchOrder \(id, symbol = undefined, params = {}\)
* fetchOrders \(symbol = undefined, since = undefined, limit = undefined, params = {}\)
* fetchOpenOrders \(symbol = undefined, since = undefined, limit = undefined, params = {}\)
* fetchClosedOrders \(symbol = undefined, since = undefined, limit = undefined, params = {}\)

注意这些方法的名字可以看出该方法是返回一个委托单还是多个委托单。

如果用户调用了交易所不支持的方法，ccxt库会抛出`NotSupported`异常。

要检查上述方法是否有效，可以查看交易所对象的`.has`属性。

```python
import ccxt
id = 'binance'
exchange = getattr(ccxt, id) ()
print(exchange.has)
```

一个典型的`.has`属性通常包含如下对应上述用于查询委托单的API方法的标志：

```python
exchange.has = {

    // ... other flags ...

    'fetchOrder': true, // available from the exchange directly and implemented in ccxt
    'fetchOrders': false, // not available from the exchange or not implemented in ccxt
    'fetchOpenOrders': true,
    'fetchClosedOrders': 'emulated', // not available from the exchange, but emulated in ccxt

    // ... other flags ...

}
```

ture和false的含义很明确。`emulated`表示这个方法是ccxt模拟出来的，不是交易所原生API提供的。

### 六，查询交易

下面的这些方法可以返回一组交易和委托单，支持`since`参数和`limit`参数：

* fetchTrades \(public\)
* fetchMyTrades \(private\)
* fetchOrders
* fetchOpenOrders
* fetchClosedOrders

第二个参数`since`可以按时间戳缩减结果数组，第三个参数`limit`可以限制返回结果的数量。

如果用户没有指定`since`参数，那么`fetchTrades`/`fetchOrders`方法将返回交易所的默认集合， 这是交易所相关的，有些交易所会返回交易对上市依赖的所有数据，而另一些交易所则只会返回 少量的交易或委托单，例如最近24小时内的，最近的100个委托单或最近的100个交易等等。如果 用户期望对时间窗口有更精确地控制，那么应该使用`since`参数。

注意：不是所有的交易所都提供了按开始时间过滤交易或委托单的方法，因此，对`since` 和`limit`的支持是交易所相关的。但是，大多数交易所都提供了分页和滚动的替代方案。

### 七，委托单缓存

一些交易所没有查询完结委托单或者所有委托单的方法，它们只提供了 `fetchOpenOrders`访问端结点，有时也会大方地提供`fetchOrder`端结点。 这意味着它们没有提供查询委托单历史的方法。ccxt库将尝试模拟委托单历史， 方法是使用交易所对象的`.orders`属性来记录所有的委托单。

任何时候当用户创建一个新的委托单，或者取消一个已有的敞口委托单，或者 进行了其他可能修改委托单状态的操作，ccxt库就会在缓存中记录整个委托单 信息。在后续的对`fetchOrder`, `fetchOrders`或 `fetchClosedOrders`方法 调用时，交易所实例会发送一个对`fetchOpenOrders`的请求，然后对比当前获取 的敞口委托单和之前缓存的委托单。ccxt库检查每个缓存的委托单，然后尝试 匹配对应的获取到的敞口委托单。当缓存的委托单不在获取到的敞口委托单中 时，ccxt库会将这个缓存的委托单标记为已完结。对fetchOrder, fetchOrders, fetchClosedOrders 的调用将返回`.orders`缓存中更新过的委托单。

这个逻辑简单点说就是：如果一个缓存的委托单没有在获取到的敞口委托单中出现， 那么它就不再是敞口单了，因此，就是完结单。

大多数情况下，`.orders`缓存的工作对用户而言是透明的。更常见的是交易所 本身提供了足够的方法。然而，由于某些交易所没有提供完整的API，`.orders` 缓存有以下已知的局限性：

* 如果用户没有在程序运行之间保存`.orders`缓存，而且也没有在重新运行时 进行恢复，那么`.orders`缓存就会丢失。因此在下一次运行程序时对 `fetchClosedOrders`的调用，交易所实例将返回一个空的委托单列表。 没有正确的恢复缓存，交易所没有办法了解委托单是完结还是取消。
* 如果API密钥对在多个交易所实例间共享，一个实例没法了解其他实例 创建或取消的委托单。这意味着`.orders`缓存不是共享的。因此API密钥对 不要在多个实例间共享，否则会有不可预料的副作用。
* 如果从ccxt库的外部创建或取消委托单，那么新委托单的状态不会到达 缓存，ccxt库也没有办法在之后正确的返回。
* 如果一个委托单的取消请求跳过了ccxt，那么ccxt库将无法从`fetchOpenOrders` 返回的敞口订单中找到该委托单，因此ccxt会将其标注为完结。这是错误的。
* 如果`fetchOrder(id)`是模拟的，那么ccxt库没有办法返回特定的委托单。
* 如果一个未处理的错误导致应用的崩溃，那么`.orders`缓存就不会保存以及再次 重启时恢复，缓存就会丢失。

注意：委托单缓存功能目前还在调整当中。

### 八，清理缓存的委托单

对于长时间运行的交易所实例，及时清理不再需要的资源是非常重要的。 因为在活跃的交易当中，`.orders`缓存会增长到非常大，ccxt库提供了 `purgeCachedOrders`/`purge_cached_orders`方法来清理缓存中较早的 非敞口委托单以释放占用的内存或其他目的，清理选择条件如下：

```text
where (order['timestamp'] < before) && (order['status'] != 'open')
```

清理命令接受一个参数来声明具体的清理条件。示例代码如下：

```text
# keep last hour of history in cache
before = exchange.milliseconds () - 1 * 60 * 60 * 1000

# purge all closed and canceled orders "older" or issued "before" that time
exchange.purge_cached_orders (before)
```

### 九，查询指定ID的委托单

要获取具有指定ID的委托单，使用`fetchOrder` / `fetch_order`方法。即使是你要查询一个特定ID的委托单，有些交易所也要求你提供交易对符号。

`fetchOrder`/`fetch_order`方法的原型如下：

```text
if (exchange.has['fetchOrder']) {
    //  you can use the params argument for custom overrides
    order = await exchange.fetchOrder (id, symbol = None, params = {})
}
```

有些交易所没有提供按ID查询委托单的访问端结点，ccxt会尽可能的提供模拟实现。 不过现在这个工作还在进行中，可能你会碰到没有实现这个模拟的交易所。

你可以使用额外的键/值参数对象来指定委托单类型等需要的设置。

下面是使用`fetchOrder`方法从一个已经验证过身份的交易所实例获取委托单信息的 示例代码。

```text
if exchange.has['fetchOrder']:
    order = exchange.fetch_order(id)
    print(order)

# Python 3.5+ asyncio (asynchronous)
import asyncio
import ccxt.async_support as ccxt
if exchange.has['fetchOrder']:
    order = asyncio.get_event_loop().run_until_complete(exchange.fetch_order(id))
    print(order)
```

### 十，查询全部委托单 - fetchOrders

使用`fetchOrders`方法查询交易所的全部委托单，方法原型如下；

```text
if (exchange.has['fetchOrders'])
    exchange.fetchOrders (symbol = undefined, since = undefined, limit = undefined, params = {})
```

有些交易所没有查询全部委托单的访问端结点，ccxt库会尝试尽可能的模拟实现。 不过到目前为止这一工作还在进展当中，因此你可能会碰到不支持此功能的交易所。

### 十一，查询全部敞口委托单

使用`fetchOpenOrders`方法查询交易所的所有敞口委托单，方法原型如下：

```text
if (exchange.has['fetchOpenOrders'])
    exchange.fetchOpenOrders (symbol = undefined, since = undefined, limit = undefined, params = {})
```

### 十二，查询全部已完结委托单

使用交易所实例的`fetchClosedOrders`方法来查询所有已完结的委托单， 其方法原型如下：

```text
if (exchange.has['fetchClosedOrders'])
    exchange.fetchClosedOrders (symbol = undefined, since = undefined, limit = undefined, params = {})
```

不要把已完结委托单和交易搞混了！一个完结的委托单可能会对应多个交易！ 因此，已完结委托单和交易并不是一回事。总的来说，委托单根本不存在手续费 ，但是每个用户交易的确有手续费、成本及其他属性。然而，许多交易所 也会把交易的这些属性传递给委托单。

有些交易所没有提供查询全部的已完结委托单的访问端结点，ccxt库会尽可能 尝试模拟实现。不过目前这一工作还在进行中，因此你可能会碰到不支持此 功能的交易所类。

### 十三，委托单数据结构

ccxt统一API中绝大多数返回委托单的方法，通常会输出如下的委托单数据结构：

```text
{
    'id':                '12345-67890:09876/54321', // string
    'datetime':          '2017-08-17 12:42:48.000', // ISO8601 datetime of 'timestamp' with milliseconds
    'timestamp':          1502962946216, // order placing/opening Unix timestamp in milliseconds
    'lastTradeTimestamp': 1502962956216, // Unix timestamp of the most recent trade on this order
    'status':     'open',         // 'open', 'closed', 'canceled'
    'symbol':     'ETH/BTC',      // symbol
    'type':       'limit',        // 'market', 'limit'
    'side':       'buy',          // 'buy', 'sell'
    'price':       0.06917684,    // float price in quote currency
    'amount':      1.5,           // ordered amount of base currency
    'filled':      1.1,           // filled amount of base currency
    'remaining':   0.4,           // remaining amount to fill
    'cost':        0.076094524,   // 'filled' * 'price' (filling price used where available)
    'trades':    [ ... ],         // a list of order trades/executions
    'fee': {                      // fee info, if available
        'currency': 'BTC',        // which currency the fee is (usually quote)
        'cost': 0.0009,           // the fee amount in that currency
        'rate': 0.002,            // the fee rate (if available)
    },
    'info': { ... },              // the original unparsed order structure as is
}
```

补充说明如下：

* fee：手续费信息这部分的工作还在进行中，取决于交易所提供的接口，这部分信息可能不完整甚至完全没有。
* fee.currency：手续费货币可能与所交易的货币都不一样。例如，一个ETH/BTC的委托单可能使用USD支付手续费
* lastTradeTimestamp：最后交易时间戳表示该委托单最后一次交易的时间。在有些情况下， 这个字段可能没有值或者是undefined/None/null，例如交易所不支持，或者委托单还是敞口状态。
* status：委托单状态的优先级高于最后交易时间戳
* cost：委托单花费 = filled \* price ，表示委托单的总花费，cost字段是处于方便目的而提供， 值可以根据其他字段推导出来

### 十四，委托下单

使用ccxt库委托下单需要提供以下信息：

* symbol：希望交易的市场对应的交易对符号，例如 BTC/USD, ZEC/ETH, DOGE/DASH, 等等。 请确保所制定的交易对符号在目标交易所存在并且可以交易。
* side：委托单的交易方向，买入还是卖出。当你下买单时，给出报价货币并将收到基准货币。 例如，买入BTC/USD意味着你将支出美元并收到比特币。当你卖出BTC/USD时则是相反的， 你将支出比特币并收到美元。
* type：委托单类型，ccxt库目前仅仅统一了市价单和限价单的API
* amount：你希望交易的数量。这通常指的是交易对符号中的基准货币的数量，虽然也有些 交易所会要求提供报价货币的数量，还有一些会根据委托单的方向而要求分别提供基准货币 或报价货币的数量。
* price：你希望为交易支付的报价货币的数量，仅限于限价单

使用ccxt统一API下市价单或限价单的成功调用将返回如下的数据结构：

```text
{
    'id': 'string',  // order id
    'info': { ... }, // decoded original JSON response from the exchange as is
}
```

有些交易所只允许限价委托单，请参考交易所的文档获取详细信息。

### 十五，市价委托

市价委托单也称为现价委托单、即时委托单或市价单。市价委托单 会立即执行。交易所的撮合引擎使用委托账本栈顶部的一个或多个 委托单来完成市价委托单。

交易所会用当时有效的最优价格来完成你的市价单。但是这并不保证 会按照你下单时看到的价格来执行交易，执行价格可能会有微小的变化， 这也称为价格滑点（price slippage），引起滑点的原因可能网络延迟、 交易所访问量过大、价格波动等。下市价委托单时，你不需要指定 委托单的价格。

使用ccxt统一APi中的`createMarketSellOrder`方法下市价卖单，或者使用 `createMarketBuyOrder`方法下市价买单。示例代码如下：

```text
// camelCaseNotation
exchange.createMarketSellOrder (symbol, amount[, params])
exchange.createMarketBuyOrder (symbol, amount[, params])

// underscore_notation
exchange.create_market_sell_order (symbol, amount[, params])
exchange.create_market_buy_order (symbol, amount[, params])
```

也可以使用更通用的`createOrder`下买单或买单，例如：

```text
// using general createOrder, type = 'market' and side = 'buy' or 'sell'
exchange.createOrder (symbol, 'market', 'sell', amount, ...)
exchange.create_order (symbol, 'market', 'buy', amount, ...)
```

注意，有些交易所不接受市价委托单（只允许限价单）。为了用程序检测 一个交易所是否支持市价委托单，你可以使用交易所的`.has['createMarketOrder']` 属性。

### 十六，市价买入委托的特殊情况

总的说来，当市价委托买入或卖出时，用户只需要指定要买入或卖出的基准货币 的数量。但是然而，有些交易所的市价买入委托单处理采用了不同的方式来计算 委托单价值。

假设你在交易`BTC/USD`，目前的BTC市场价格是超过9000 USD。要按市价买入或 卖出，你可以指定数量为 2 BTC，取决于你的委托方向，成交结果将是你的账户 增加或减少18000 USD左右。

但是有些交易所要求按报价货币指定委托单的总价！这背后的逻辑其实很简单， 不是说我要买入或卖出多少基准货币，而是”我想消费多少报价货币“。

在这些交易所进行市价买入委托，你不能将委托单的数量指定为 2 BTC，而是 应当指定委托单的总价，在这个例子中，也就是 18000 USD。采用这种方式处理 市价委托单的交易所，有一个选项`createMarketBuyOrderRequiresPrice`，你 可以用它以两种方式指定市价买入委托单的总花费：

第一种是默认的，如果你同时设置了委托数量和价格，那么在ccxt内部将会 简单地按照这个公式`(cost = amount * price)`计算出委托单总价格，得到 的总花费就会设置为该市价委托单的报价货币总花费，也就是USD总额。

↓ShowCode↓

如果希望自己指定委托单的总花费，那么可以使用第二种方式。这需要先 关闭`createMarketBuyOrderRequiresPrice`选项，然后进行设置。示例代码 如下：

```text
const exchange = new ccxt.cex ({
    'apiKey': YOUR_API_KEY,
    'secret': 'YOUR_SECRET',
    'enableRateLimit': true,
    'options': {
        'createMarketBuyOrderRequiresPrice': false, // switch off
    },
})

// or, to switch it off later, after the exchange instantiation, you can do
exchange.options['createMarketBuyOrderRequiresPrice'] = false

;(async () => {

    // when `createMarketBuyOrderRequiresPrice` is true, we can pass the price
    // so that the total cost of the order would be calculated inside the library
    // by multiplying the amount over price (amount * price)

    const symbol = 'BTC/USD'
    const amount = 2 // BTC
    const price = 9000 // USD
    cost = amount * price // ← instead of the amount cost goes ↓ here
    const order = await exchange.createMarketBuyOrder (symbol, cost)
    console.log (order)
})
```

### 十七，用限价单模拟市价单

用限价单来模拟市价单也是可能的。

警告：由于高波动性，这个方法存在风险，在使用之前请务必了解 清楚！

大多数时候，市价买单可以使用一个设置极低价格的限价单来模拟- 当交易所 检测到你在以非常低的价格卖出时，会自动将其设置为taker order，它会 自动提供委托账本中的最优买方价格。这实际上和下市价卖单的效果一样。 因此市价委托单可以使用限价委托单来模拟。

反方向也是一样的 - 市价买入委托可以使用一个价格非常高的限价买入 委托来模拟。大多数交易所也会使用最优价格来完成你的委托单，也就是市价。

然而，你不能完全依赖这样的模拟，记得先用少量资金进行测试！你可以 在交易所的web页面验证逻辑。你可以在指定的限价卖出少量（可承担的损失）， 然后在交易历史中检查实际的执行价格。

### 十八，限价委托

限价委托单也称为限价单。有些交易所只接受限价委托单。 限价委托单需要在提交委托单时指定价格（单位费率）。 只有在市场价格达到期望的价位时，交易所才会完成限价 委托单。

使用`createLimitBuyOrder`委托限价买入，或者使用`createLimitSellOrder` 委托限价卖出。示例代码如下：

```text
// camelCaseStyle
exchange.createLimitBuyOrder (symbol, amount, price[, params])
exchange.createLimitSellOrder (symbol, amount, price[, params])

// underscore_style
exchange.create_limit_buy_order (symbol, amount, price[, params])
exchange.create_limit_sell_order (symbol, amount, price[, params])
```

### 十九，委托单的自定义参数

有些交易所允许你指定委托单的可选参数。在调用ccxt统一API时， 你可以使用一个关联数组传入额外的参数。所有的自定义参数都是 交易所相关的，当然彼此也是不可以互换的，不要期望一个交易所 的自定义参数可以用于另一个交易所。

```text
# add a custom order flag
kraken.create_market_buy_order('BTC/USD', 1, {'trading_agreement': 'agree'})
```

### 二十，其他类型的委托单

委托单的类型可以是限价或市价，如果你要限价止损委托类型，可以使用 改写默认参数值。下面的代码展示了如何改写委托单类型，然而，你必须阅读交易所的 文档以了解应该使用什么参数以及如何正确设定参数值。限价委托或 市价委托之外的其他类型目前在ccxt中还没有统一的API，只能参考如下 代码改写默认的参数。

↓ShowCode↓

### 二十一，取消委托单

要取消已有的委托单，可以使用`cancelOrder (id, symbol, params)` / `cancel_order (id, symbol, params)`方法。 注意，即使指定了要取消的委托单ID，有些交易所还是要求传入第二个参数指定交易对符号。

`cancelOrder`调用示例代码如下。

```text
exchange.cancel_order ('1234567890') # replace with your order id here (a string)
```

**委托单取消异常**

`cancelOrder()`通常仅用于敞口委托单。然而，交易所有可能在你的取消请求 之前刚好执行了委托单，因此取消请求可能击中一个已经完成的委托单。

取消请求也可能会抛出`NetworkError`异常，表示委托单可能没有成功取消。 后续的`cancelOrder()`调用也可能击中一个已经取消的委托单。

因此，`cancelOrder()`在这些情况下会抛出`OrderNotFound`异常：

* 取消一个已经完成的委托单
* 取消一个已经取消的委托单

### 二十二，委托单与交易的关系

交易也称为成交。每个交易都是委托单执行的结果。需要注意的是， 委托单和交易是一对多的关系：委托单的一次执行可能会产生多笔交易。 然而，当一个委托单匹配了另一个相反方向的委托单，就会生成一笔 交易。因此，当一个委托单匹配了另一个方向的多个委托单时，就会 生成多笔交易，每个配对对应一笔交易。

简而言之，一个委托单可以包含一笔或多笔交易。或者换句话说， 一个委托单可以通过一笔或多笔交易来成交。

例如，委托账本中可以包含如下的委托单（可以是任何交易符号或交易对）：

```text
    | price  | amount
----|----------------
  a |  1.200 | 200
  s |  1.100 | 300
  k |  0.900 | 100
----|----------------
  b |  0.800 | 100
  i |  0.700 | 200
  d |  0.500 | 100
```

上面的数字都不是真实的，这只是用于演示委托单和交易之间的关系。

一个卖家决定在卖出侧下一个限价卖出单，价格为0.700，数量为150：

```text
    | price  | amount
----|----------------  ↓
  a |  1.200 | 200     ↓
  s |  1.100 | 300     ↓
  k |  0.900 | 100     ↓
----|----------------  ↓
  b |  0.800 | 100     ↓ sell 150 for 0.700
  i |  0.700 | 200     --------------------
  d |  0.500 | 100
```

由于新的卖出单的价格和数量覆盖超过一个买入委托单（委托单b和i）， 在交易撮合引擎中很快（但不是立刻）会产生以下事件：

委托单b可以匹配新进来的卖单，因为两者价格有交集。它们的数量 可以彼此消化，因此，买入方在0.800价格成交了100单位。买方的 卖出委托单在0.800价位部分成交了100单位。注意对于委托单的成交 部分，买方得到了比初始要求更好的价格。他要求最低价格是0.7， 但是成交价是更好的0.8。大多数传统的交易所使用最优价格来执行 委托单。

交易撮合引擎会为委托单b生成一笔和进来的卖出单发生的交易。这个 交易成交了整个委托单b，以及卖出单的大部分数量。每一对匹配的 委托单都会生成一笔交易，无论是部分成交还是全部成交。在这个示例 中，买方数量100可以让委托单b完全成交（完成委托单b），同时也 部分成交了卖方的委托单（它在委托账本中还是敞口的）。

委托单b现在是完成状态，成交数量是100，它包含了一笔和卖出单 发生的交易。卖出单目前是敞口状态，成交数量是100，它包含了 一个和委托单b发生的交易。因此到目前位置，每个订单都只有 一个成交交易。

进入撮合引擎的卖出委托单目前的成交数量是100，还剩下50单位 继续等待成交。

委托账本的中间状态现在如下所示（委托单b已经完成，因此已经不再 出现在委托账本中）：

```text
    | price  | amount
----|----------------  ↓
  a |  1.200 | 200     ↓
  s |  1.100 | 300     ↓
  k |  0.900 | 100     ↓
----|----------------  ↓ sell remaining 50 for 0.700
  i |  0.700 | 200     -----------------------------
  d |  0.500 | 100
```

委托单i可以匹配卖出单的剩余部分，因为两者价格相交。买入单i的数量 是200，因此可以完全吃掉卖出单的剩余数量50。委托单i可以部分成交 50单位，但是其剩余数量150还将继续在委托账本中等待撮合。不过卖出 委托单在这第二次撮合过程中可以完全成交了。

交易撮合引擎为委托单i生成一笔和卖出单发生的交易。这笔交易让委托单i 部分成交，让卖出单完全成交。又一次，一对匹配的委托单生成了一笔交易。

经过上述步骤，更新后的委托账本看起来是这样：

```text
    | price  | amount
----|----------------
  a |  1.200 | 200
  s |  1.100 | 300
  k |  0.900 | 100
----|----------------
  i |  0.700 | 150
  d |  0.500 | 100
```

注意委托单b已经消失了，卖出单也不在了。所有完成的委托单都会从 委托账本中移除。部分成交的委托单i处于敞口状态，依然还呆在委托 账本中。

### 二十三，查询个人的历史交易

ccxt库的统一API中的大部分方法会返回单个交易对象或交易对象数组。 但是，极少数交易所会一次返回全部个人交易。大多数情况下，交易所 的API会限制返回结果的数量。你不应该在一个调用中读取所有交易对象。 实际上，极少有交易所会容忍或允许这种行为。

要查询历史交易，用户需要分页遍历数据。分页通常隐含着使用循环 分批获取数据的意思。

在大多数情况下，用户需要提供至少某种类型的分页以便可以一致地获取期望的结果。 使用`fetchMyTrade`/`fetch_my_trade`方法获取个人的历史交易，其方法原型与调用的示例代码如下。

```text
# fetch_my_trades (symbol = None, since = None, limit = None, params = {})

if exchange.has['fetchMyTrades']:
    exchange.fetch_my_trades (symbol = None, since = None, limit = None, params = {})
```

`fetchMyTrade`方法返回一个有序的交易对象数组，最近产生的交易排在最后。

### 二十四，交易的数据结构

在ccxt中，交易的数据结构如下：

```text
{
    'info':         { ... },                    // the original decoded JSON as is
    'id':           '12345-67890:09876/54321',  // string trade id
    'timestamp':    1502962946216,              // Unix timestamp in milliseconds
    'datetime':     '2017-08-17 12:42:48.000',  // ISO8601 datetime with milliseconds
    'symbol':       'ETH/BTC',                  // symbol
    'order':        '12345-67890:09876/54321',  // string order id or undefined/None/null
    'type':         'limit',                    // order type, 'market', 'limit' or undefined/None/null
    'side':         'buy',                      // direction of the trade, 'buy' or 'sell'
    'takerOrMaker': 'taker',                    // string, 'taker' or 'maker'
    'price':        0.06917684,                 // float price in quote currency
    'amount':       1.5,                        // amount of base currency
    'cost':         0.10376526,                 // total cost (including fees), `price * amount`
    'fee':          {                           // provided by exchange or calculated by ccxt
        'cost':  0.0015,                        // float
        'currency': 'ETH',                      // usually base currency for buys, quote currency for sells
        'rate': 0.002,                          // the fee rate (if available)
    },
}
```

补充说明如下：

* fee：手续费部分的处理目前还在进行中，可能缺失信息甚至没有
* fee currency：手续费货币可能不同于所交易的货币，例如，一个 ETH/BTC委托单的手续费采用USD支付
* cost：交易总花费 = amount \* price，这是一个方便字段，可以利用其他字段计算得出。

### 二十五，获取充值地址

要将资金存入交易所，你必须先从交易所获取一个你希望存入的数字货币的 地址。大多数交易所会为用户创建并管理这些地址。有些交易所也允许用户 创建用于充值的新地址。有些交易所则要求用户为每次充值都创建新的充值 地址。

用于充值的地址可以使用`fetchDepositAddress`方法获取在交易所中已有的地址， 也可以使用`createDepositAddress`创建新的地址。要查看交易所支持哪个方法， 可以使用`exchange.has['fetchDepositAddress']`和`exchange.has['createDepositAddress']` 属性，这两个方法都返回一个地址结构：

```text
fetchDepositAddress (code, params = {})
createDepositAddress (code, params = {})
```

* code：统一的货币代码，大写字符串
* params：额外的可选参数

有些交易所也提供API方法来一次获取多个或全部充值地址：

```text
fetchDepositAddresses (codes = undefined, params = {})
```

取决于交易所的要求，上述调用可能需要传入货币代码数组作为第一个参数。 `fetchDepositAddresses`方法返回一个地址对象数组。

### 二十六，地址的数据结构

`fetchDepositAddress`、`fetchDepositAddresses`和`createDepositAddress`方法返回的 地址，结构如下：

```text
{
    'currency': currency, // currency code
    'address': address,   // address in terms of requested currency
    'tag': tag,           // tag / memo / paymentId for particular currencies (XRP, XMR, ...)
    'info': response,     // raw unparsed data as returned from the exchange
}
```

有些货币，例如 AEON, BTS, GXS, NXT, SBD, STEEM, STR, XEM, XLM, XMR, XRP, 交易所通常会要求提供一个额外的标签（tag）参数。其他货币则将标签设置为 undefined / None / null。标签可以是备注、消息或支付ID，用来附加在提现交易 上。对于上述货币来说，标签是强制性的，因为交易所需要用它来区分不同的用户账户。

当设置标签和地址时需要谨慎。标签不是你随便选择的字符串！你不能在标签里发送 用户消息和评论。标签字段的目的是正确定位你的钱包，因此必须是正确的。你应该 只使用从交易所收到的标签，否则你的交易可能永远也不会到达目标地址。

### 二十七，提现

使用交易所实例的`withdraw`方法从交易所提现。示例代码如下。

```text
exchange.withdraw(code, amount, address, tag=None, params={})
```

`code`参数表示货币代码（通常是三位大写字幕，但是不同情况下可能有所差异）。

`withdraw`方法返回一个字典，其中的提现ID字段值通常是链上交易的ID，或者 是交易所内部的提现请求ID。`withdraw`的返回值看起来像这样：

```text
{
    'info' { ... },      // unparsed reply from the exchange, as is
    'id': '12345567890', // string withdrawal id, if any
}
```

有些交易所采用双因子认证的手段要求每一笔提现都进行人工确认。为了放行 你的提现请求，通常你不得不点击交易所发给你的邮件中的秘密链接，或者 在交易所网站上输入一个验证码，以便交易所确认提现交易是安全的。

在有些情况下，你也可以使用提现ID在稍后检查提现状态（是否成功）并 提交双因子确认码，这需要参考交易所的文档获取详细信息。

### 二十八，链上交易数据结构

ccxt库中，链上交易（Transaction）的数据结构如下：

```text
{
    'info':      { ... },    // the JSON response from the exchange as is
    'id':       '123456',    // exchange-specific transaction id, string
    'txid':     '0x68bfb29821c50ca35ef3762f887fd3211e4405aba1a94e448a4f218b850358f0',
    'timestamp': 1534081184515,             // timestamp in milliseconds
    'datetime': '2018-08-12T13:39:44.515Z', // ISO8601 string of the timestamp
    'addressFrom': '0x38b1F8644ED1Dbd5DcAedb3610301Bf5fa640D6f', // sender
    'address':  '0x02b0a9b7b4cDe774af0f8e47cb4f1c2ccdEa0806', // "from" or "to"
    'addressTo': '0x304C68D441EF7EB0E2c056E836E8293BD28F8129', // receiver
    'tagFrom', '0xabcdef', // "tag" or "memo" or "payment_id" associated with the sender
    'tag':      '0xabcdef' // "tag" or "memo" or "payment_id" associated with the address
    'tagTo': '0xhijgklmn', // "tag" or "memo" or "payment_id" associated with the receiver
    'type':     'deposit',   // or 'withdrawal', string
    'amount':    1.2345,     // float (does not include the fee)
    'currency': 'ETH',       // a common unified currency code, string
    'status':   'pending',   // 'ok', 'failed', 'canceled', string
    'updated':   undefined,  // UTC timestamp of most recent status change in ms
    'comment':  'a comment or message defined by the user if any',
    'fee': {                 // the entire fee structure may be undefined
        'currency': 'ETH',   // a unified fee currency code
        'cost': 0.1234,      // float
        'rate': undefined,   // approximately, fee['cost'] / amount, float
    },
}
```

补充说明：

* 如果交易所没有设置交易的方向（买入/卖出）， addressFrom 或 addressTo 的值可能为undefined/None/null
* address字段的含义是交易所相关的。有些情况下该字段的值表示发送方的地址，有时则可能表示接收方的地址。
* update字段表示最近的资金操作的状态变化，以毫秒计算的UTC时间戳。
* 取决于交易所的支持与否，fee字段的内容可能缺失
* comment字段的值可能是undefined/None/null，否则表示用户创建链上交易时传入的消息或备注
* 处理标签（tag）和地址（address）时需要谨慎，标签不是用户任意指定的字符串，不能在 标签中发送用户消息和评论。标签的目的是正确定位你的钱包。因此应当遵循交易所的要求。

### 二十九，查询充值记录

使用ccxt统一API的`fetchDeposits`方法查询充值记录。示例代码如下。

```text
# fetch_deposits(code = None, since = None, limit = None, params = {})

if exchange.has['fetchDeposits']:
    deposits = exchange.fetch_deposits(code, since, limit, params)
else:
    raise Exception (exchange.id + ' does not have the fetch_deposits method')
```

### 三十，查询提现记录

使用ccxt统一API的`fetchWithdrawals`方法查询提现记录。示例代码如下。

```text
# fetch_withdrawals(code = None, since = None, limit = None, params = {})

if exchange.has['fetchWithdrawals']:
    withdrawals = exchange.fetch_withdrawals(code, since, limit, params)
else:
    raise Exception (exchange.id + ' does not have the fetch_withdrawals method')
```

### 三十一，查询链上交易

使用ccxt统一API的`fetchTransactions`方法查询链上交易。示例代码如下。

```text
# fetch_transactions(code = None, since = None, limit = None, params = {})

if exchange.has['fetchTransactions']:
    transactions = exchange.fetch_transactions(code, since, limit, params)
else:
    raise Exception (exchange.id + ' does not have the fetch_transactions method')
```

### 三十二，查询手续费

手续费通常可以分为以下两类：

* 交易手续费：向交易所支付的交易手续费，通常按成交量的百分点计取
* 资金操作手续费：在充值和提现时向交易所支付的费用，包含链上交易费用

因为手续费结构会依赖于用户交易的货币的实际交易量，手续费是与账户相关的。 ccxt的统一API中，提供了以下方法用于账户相关的手续费处理：

* fetchFees \(params = {}\)
* fetchTradingFees \(params = {}\)
* fetchFundingFees \(params = {}\)

手续费方法将返回一个统一的手续费结构，该结构在整个ccxt库中保持统一， 通常采用交易市场或货币为索引键。手续费结构如下：

```text
{
    'type': takerOrMaker,
    'currency': 'BTC', // the unified fee currency code
    'rate': percentage, // the fee rate, 0.05% = 0.0005, 1% = 0.01, ...
    'cost': feePaid, // the fee cost (amount * fee rate)
}
```

手续费这一部分的代码目前还在进行中，因此其中有些方法和属性在某些交易所 可能还会缺失。

**不要使用已经废弃的`.fees`属性。**

### 三十三，查询交易所状态

交易所状态描述交易所API的最近可用情况。交易所状态信息可能是在交易所 实现类中硬编码的，也可能是从交易所API直接获取的。

可以使用ccxt的统一API中的`fetchStatus`方法来查询交易所状态。其返回结果为 以下三者之一：

* 交易所实现类硬编码的信息，例如，如果交易所宕机的话
* 使用交易所对象的ping或fetchTime方法检查交易所API是否存活
* 使用交易所提供的API获取状态信息

`fetchStatus`方法原型如下：

```text
fetchStatus(params = {})
```

方法返回的状态数据结构如下：

```python
{
    'status': 'ok', // 'ok', 'shutdown', 'error', 'maintenance'
    'updated': undefined, // integer, last updated timestamp in milliseconds if updated via the API
    'eta': undefined, // when the maintenance or outage is expected to end
    'url': undefined, // a link to a GitHub issue or to an exchange post on the subject
}
```

说明：

* 'ok'表示交易所API可用
* 'shutdown'表示交易所停机，这时`updated`字段的值就表示停机时间
* 'error'表示API不兼容
* 'maintenance'表示常规维护，`eta`字段的值表示预计恢复时间。

### 三十四，预算交易费

交易费是市场的属性。通常交易费使用`fetchMarkets`调用载入。但有时 交易所会使用不同的访问端结点提供交易费服务。

ccxt的统一API中的`calculateFee`方法可以预算交易费。**警告！**这个方法 是实验性的，不稳定而且可能在有些情况下的结果不正确。请谨慎使用。 实际的手续费可能和`calculateFee`返回的结果不一致，因此不要依赖于 预算值，因为市场条件变化很快，很难预料你的委托单是会成为maker还是taker。 方法原型如下：

```text
calculateFee (symbol, type, side, amount, price, takerOrMaker = 'taker', params = {})
```

`calculateFee`方法将返回统一的手续费结构。

应当使用交易所的`.markets`属性方位交易费率，例如：

```python
exchange.markets['ETH/BTC']['taker'] // taker fee rate for ETH/BTC
exchange.markets['BTC/USD']['maker'] // maker fee rate for BTC/USD
```

当你为交易所提供流动性时，支付的是maker手续费。maker手续费通常低于 taker手续费。当你从交易所拿走流动性时，则需要支付taker手续费。

### 三十五，资金操作费

资金操作费是货币的属性。

可以使用交易所的`.currencies`属性访问资金操作费率。这方面目前在ccxt 中还没有统一，未来可能会有变化。

```python
exchange.currencies['ETH']['fee'] // tx/withdrawal fee rate for ETH
exchange.currencies['BTC']['fee'] // tx/withdrawal fee rate for BTC
```

### 三十六，查询账本

有些交易所提供额外的访问点用于查询整合的账本历史。账本 就是变化的历史，记录改变用户余额的操作，包括充值和提现等。

使用ccxt统一API中的`fetchLedger`方法查询账本，原型如下：

```python
async fetchLedger (code = undefined, since = undefined, limit = undefined, params = {})
```

有些交易所不允许一次查询所有的账本条目，需要在调用`fetchLedger` 方法时指定code参数。

### 三十七，账本记录结构

账本记录结构如下：

```python
{
    'id': 'hqfl-f125f9l2c9',                // string id of the ledger entry, e.g. an order id
    'direction': 'out',                     // or 'in'
    'account': '06d4ab58-dfcd-468a',        // string id of the account if any
    'referenceId': 'bf7a-d4441fb3fd31',     // string id of the trade, transaction, etc...
    'referenceAccount': '3146-4286-bb71',   // string id of the opposite account (if any)
    'type': 'trade',                        // string, reference type, see below
    'currency': 'BTC',                      // string, unified currency code, 'ETH', 'USDT'...
    'amount': 123.45,                       // absolute number, float (does not include the fee)
    'timestamp': 1544582941735,             // milliseconds since epoch time in UTC
    'datetime': "2018-12-12T02:49:01.735Z", // string of timestamp, ISO8601
    'before': 0,                            // amount of currency on balance before
    'after': 0,                             // amount of currency on balance after
    'status': 'ok',                         // 'ok, 'pending', 'canceled'
    'fee': {                                // object or or undefined
        'cost': 54.321,                     // absolute number on top of the amount
        'currency': 'ETH',                  // string, unified currency code, 'ETH', 'USDT'...
    },
    'info': { ... },                        // raw ledger entry as is from the exchange
}
```

补充说明：

账本记录的类型就是与之关联的操作类型。如果amout来自委托单，那么关联的交易类型就是`trade`，同时`referenceId`字段的值记录交易ID。如果amount 来自提现操作，那么这条记录关联的就是链上交易。可能值如下：

* trade
* transaction
* fee
* rebate
* cashback
* referral
* transfer
* whatever
* ...

`referenceId`字段表示引用ID，记录对应事件的ID。

`status`字段描述账本变化是成功（ok）、待定（pending）还是取消（ok）等状态。 大多数情况下都应该是ok。

`type`字段可以关联常规交易、链上交易（充值或提现操作）或交易所内部转账。 如果账本记录关联的是内部转账，那么`account`字段将包含该记录要修改的账户ID， `referenceAccount`字段的值则是相对方向的账户ID。

### 三十八，修改Nonce值

默认的nonce是以秒计的32位unix时间戳。如果你希望进行更频繁的 私有请求，应该使用毫秒计的nonce来改写，否则最快才能每秒发一个请求。 当你达到交易所限流值时，大多数交易所都会进行节流，请参考具体 交易所的API文档。

要重设nonce值的话，更简单的方式是再创建一个用于访问私有api 的密钥对。

有些情况下你没办法创建新的密钥，比如没有权限或者其他原因。 这时也有办法改写nonce值，可以使用ccxt统一api中市场基类的以下方法：

* seconds \(\): 返回秒计的unix时间戳
* milliseconds \(\): 返回毫秒计的unix时间戳
* microseconds \(\): 返回微秒计的unix时间戳

有的交易所在API文档中搞混了毫秒和微秒，原谅他们吧。你可以使用上面的这些方法重设nocne值。示例代码如下。

```python
# A: the shortest
gdax = ccxt.gdax({'nonce': ccxt.Exchange.milliseconds})

# B: custom nonce
class MyKraken(ccxt.kraken):
    n = 1
    def nonce(self):
        return self.n += 1

# C: milliseconds nonce
class MyBitfinex(ccxt.bitfinex):
    def nonce(self):
        return self.milliseconds()

# D: milliseconds nonce inline
hitbtc = ccxt.hitbtc({
    'nonce': lambda: int(time.time() * 1000)
})

# E: milliseconds nonce
acx = ccxt.acx({'nonce': lambda: ccxt.Exchange.milliseconds()})
```

[Top~~](https://www.cnblogs.com/zyyhxbs/p/13803561.html#_labelTop)

## 十一，CCXT错误处理

### 一，错误处理概述

ccxt采用各种语言中原生的异常机制进行错误处理。

要处理错误，你需要使用try代码块来保护调用ccxt统一API的代码， 然后使用catch代码块捕捉异常。示例代码如下。

```python
try:
    response = await exchange.fetch_order_book('ETH/BTC')
    print(response)
except ccxt.NetworkError as e:
    print(exchange.id, 'fetch_order_book failed due to a network error:', str(e))
    # retry or whatever
    # ...
except ccxt.ExchangeError as e:
    print(exchange.id, 'fetch_order_book failed due to exchange error:', str(e))
    # retry or whatever
    # ...
except Exception as e:
    print(exchange.id, 'fetch_order_book failed with:', str(e))
    # retry or whatever
    # ...
```

### 二，异常类的体系

ccxt中所有的机场都派生自BaseError基类，其定义如下：

```python
class BaseError (Exception):
    pass
```

下面是ccxt异常类的继承体系：

↓ShowCode↓

`BaseError`类是各种错误的一般性描述，包括可用性错误、请求/响应错误等。 开发者至少应该捕捉这个异常，如果不需要区分具体是什么错误的话。

在错误体系中有两个子树，都派生自BaseError：

* NetworkError
* ExchangeError

`NetworkError`表示不严重的错误，某种意义上说并不是真正的错误，更可能是临时性的不可用情况，可能原因包括交易所维护、DDoS保护和临时性访问阻断。

相比之下，`ExchangeError`是严重的错误 – 如果捕捉到这个错误，那么你使用 相同的输入应该都会得到同样的错误。

这两族错误的区别在于`NetworkError`是可恢复的，而`ExchangeError`是不可恢复的。

### 三，交易所异常

当交易所服务器返回的JSON响应中包含了错误信息时，ccxt就会 抛出这个异常。可能的原因包括：

* 访问端结点被交易所关闭
* 交易所未找到指定的交易对符号
* 请求的参数缺失
* 参数格式不正确
* 交易所响应含义不明确

其他从ExchangeError派生的异常包括：

* NotSupported：如果交易所的API不支持所访问的端结点，就会抛出这个异常
* AuthenticationError：如果API需要身份验证而请求中没有提供或者提供的不正确，就会抛出这个异常
* PermissionDenied：如果请求中指定的api key没有足够的权限，就会抛出这个异常
* InsufficientFunds：如果账户余额不足以执行当前请求的操作，例如委托下单，就会抛出这个异常
* InvalidAddress：如果请求中的地址格式不正确，就会抛出这个异常
* InvalidOrder：这是统一API中order系列方法异常类的基类
* OrderNotFound：试图查询或取消不存在的委托单时，就会抛出这个异常

### 四，网络异常

所有网络相关的错误通常是可恢复的，网络故障、流量阻塞、服务器不可用这些 通常都是时间相关的，稍后重新请求通常就能解决问题。

**DDoS保护异常 - DDoSProtection**

当有以下情况之一发生时，就会抛出这个异常：

* 当Cloudflare或Incapsula限流时
* 当交易所限流时

除了默认的错误处理，ccxt库会使用以下关键字搜索交易所的响应内容：

* cloudflare
* incapsula
* overload
* ddos

**请求超时异常 - RequestTimeout**

当与交易所的连接失败或没有在指定时间内收到交易所响应的完整数据时， 就会抛出RequestTimeout异常。

因此建议采用以下方式处理这一类的异常：

* 对于查询请求，只需要重新尝试调用即可
* 对于

  ```text
  cancelOrder
  ```

  请求，要求用户进行二次尝试。如果没有进行二次尝试 而是立即调用了fetchOrder, fetchOrders, fetchOpenOrders 或 fetchClosedOrders， 那么可能导致

  ```text
  .orders
  ```

  缓存不同步。二次尝试调用

  ```text
  cancelOrder
  ```

  可能返回 以下结果之一：

  * 成功完成，表示委托单已经正确地取消了
  * 抛出OrderNotFound异常，表示委托单要么已经在上次请求时取消， 要么已经在两次请求的间隔执行（完成或成交）。这是需要调用`fetchOrder`来 正确地更新缓存

* 如果

  ```text
  createOrder
  ```

  请求抛出

  ```text
  RequestTimeout
  ```

  异常，开发者应当：

  * 使用fetchOrders, fetchOpenOrders, fetchClosedOrders检查上个请求是否成功下单 并更新orders缓存。
  * 如果委托单不是敞口状态，那么开发者需要调用`fetchBalance`检查账户余额 是否变化。注意fetchBlanace依靠orders缓存进行余额推理，因此只能在更新 缓存后进行调用！

**交易所不可用异常 - ExchangeNotAvailable**

如果在响应中检测到如下任何关键字，ccxt库会抛出ExchangeNotAvailable异常：

* offline
* unavailable
* busy
* retry
* wait
* maintain
* maintenance
* maintenancing

**无效Nonce异常 - InvalidNonce**

当你使用的Nonce比之前的请求中的nonce还要小的时候，ccxt就会抛出InvalidNoce异常。 在以下情况中会抛出这一类异常：

* 你没有进行请求限流，或者发送太多请求
* 你的API key没有刷新，可能在其他软件或脚本中使用了同样的api key
* 在多个交易所实例中使用相同的api密钥对
* 系统时钟没有同步。

