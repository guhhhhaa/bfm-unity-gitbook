# 选股

{% hint style="info" %}
NOTE: 策略推荐市盈率，市净率策略，

**该策略的特点是 —— 抗跌不跟涨，跟涨选指数**
{% endhint %}

## 大盘

### 沪深300

沪深300-市净率

[https://robo.datayes.com/v2/landing/monitor\_detail?slotId=238422](https://robo.datayes.com/v2/landing/monitor_detail?slotId=238422)

沪深300-市盈率

[https://robo.datayes.com/v2/landing/monitor\_detail?slotId=238421](https://robo.datayes.com/v2/landing/monitor_detail?slotId=238421)

### 上证综指

上证综指-市净率

[https://robo.datayes.com/v2/landing/monitor\_detail?slotId=238420](https://robo.datayes.com/v2/landing/monitor_detail?slotId=238420)

上证综指-市盈率

[https://robo.datayes.com/v2/landing/monitor\_detail?slotId=238419](https://robo.datayes.com/v2/landing/monitor_detail?slotId=238419)

## 选股

### 因子看板——风险因子，风格因子

[https://www.joinquant.com/view/factorlib/list](https://www.joinquant.com/view/factorlib/list)

### 市净率因子 book\_to\_price\_ratio

（教科书上是价格/净值，这个是净值/价格，所以教科书上选小的，这个选大的）  
**（回测区间选10年）  
（策略：按照市值比例购买。预计未来下跌时选择最大分位数的股票，预计上涨时选指数）**  
[https://www.joinquant.com/view/factorlib/detail/f297b9704818db80ad7fde91fe42b493?buildtype=0&universetype=aHMzMDA%3D&period=M3k%3D&commisionFee=MA%3D%3D&skipPaused=MQ%3D%3D](https://www.joinquant.com/view/factorlib/detail/bb3b7b42b7425d4ada99603b008724d4?buildtype=0&universetype=aHMzMDA%3D&period=M3k%3D&commisionFee=MA%3D%3D&skipPaused=MQ%3D%3D)

### 预期市盈率 predicted\_earnings\_to\_price\_ratio

（教科书上是价格/收益，这个是收益/价格，所以教科书上选小的，这个选大的）  
**（回测区间选10年）  
（策略：按照市值比例购买。预计未来下跌时选择最大分位数的股票，预计上涨时选指数）**  
[https://www.joinquant.com/view/factorlib/detail/bb3b7b42b7425d4ada99603b008724d4?buildtype=0&universetype=aHMzMDA%3D&period=M3k%3D&commisionFee=MA%3D%3D&skipPaused=MQ%3D%3D](https://www.joinquant.com/view/factorlib/detail/bb3b7b42b7425d4ada99603b008724d4?buildtype=0&universetype=aHMzMDA%3D&period=M3k%3D&commisionFee=MA%3D%3D&skipPaused=MQ%3D%3D)

## 投资建议

选股是没有必要的，技术分析一概不靠谱。最好的选股就是指数。至于个股，和个基金，我是从来不推荐的。推荐买入指数基金和债券基金。

真正需要做的是，指数和债券的配比关系。而指数和债券的配比关系是按照市净率和市盈率来决定的。

一切通过技术分析，想要跑赢沪深300和纳指100的尝试都是徒劳的。选股和操作没有用，噪声操作会加大你的亏损，不信你做个10年回测就明白了——[https://www.joinquant.com/view/factorlib/list](https://www.joinquant.com/view/factorlib/list) 这个是因子分析，可以选择你的选股策略进行回测，如果你把周期拉到10年，你会发现，指数才是真正牛逼的选择。 

如果说什么有用，也就是，市净率，市盈率，才有用。 而且市净率，市盈率只有下跌行情有用，能抗跌，

上涨行情都偏离价值了，所以市净率，市盈率无法用来追涨。

{% embed url="https://guhhhhaa.gitbook.io/joinquant/jin-rong-li-lun-zong-jie/ji-ben-mian-xuan-gu" %}

{% hint style="success" %}
## 低估：

市盈率P/E＜10，12-17 ，甚至15-25

市净率P/B＜2，1.2-1.7，甚至1.5-2.5

股息率＞5%，

市盈率相对盈利增长比率[PEG](https://xueqiu.com/8287840120/74917276)＜0.5。（&lt;1也可） 

## 成长：

净资产收益率ROE＞15%，且用杜邦分析剔除杠杆（权益乘数&lt;3）。

\*\*\*\*[**https://www.ricequant.com/quant/wizard/**](https://www.ricequant.com/quant/wizard/)\*\*\*\*

\*\*\*\*[**https://www.joinquant.com/wizardstock/index/generateStock**](https://www.joinquant.com/wizardstock/index/generateStock)\*\*\*\*
{% endhint %}

如果说最简单粗暴的选股是什么，就是这个策略。 

不信，你去[聚宽](https://www.joinquant.com/)，[米筐](https://www.ricequant.com/)，[UQER](https://uqer.datayes.com/)，用向导式回测一下就行了。 

量化平台的向导式回测，无需编程，输入几个数，点几下按钮，就行。

![&#xA0;&#xA0;&#xA0;&#x6A2A;&#x8F74;&#x662F;&#x4F30;&#x503C;&#xFF0C;&#x7EB5;&#x8F74;&#x662F;&#x4ED3;&#x4F4D;&#x548C;&#x64CD;&#x4F5C;](../.gitbook/assets/0e2abfcc2987f6aaeb09ece758f3e8ac.jpg)

