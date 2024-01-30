---
description: BFM Trading Strategy
---

# BFM Trading Strategy♟

> ## 比坊梦交易策略
>
> ### BFM Trading Strategy

{% hint style="info" %}
## 游戏已经开始，请选择你的英雄。

### 注：不同的英雄分属不同的派系，你只能选择一种。

### 开场后，请不要换英雄，否则[后果自负](https://www.bilibili.com/video/BV1hJ411G7jN)。
{% endhint %}

## 写在前面

<details>

<summary>策略选择</summary>

1，没能力用，用不上的策略别研究。 统计学的前提是不是分布不变或稳定，但是机器学习也没法推断未来的分布。并不能证明它的效果比统计学好。

2，研究成本高的策略，能等就等等。 机器学习成本太高了，小资金带不动这个研究成本。 而且收益率提高这个，暂时证明不了。

3，能看书就别研究，让别人研究去，等他研究明白了，他也亏完了，而且市面上也烂大街了，一个策略，别人嫌弃的时候，这个时候用最好。&#x20;

4，盈亏同源，策略没有优劣，但是，非要选一个的话，动态平衡最牛逼，毕竟是信息论祖师爷香农钦定的。

</details>

<details>

<summary>标的选择</summary>

投资原则1，树杈易折，主干长青&#x20;

投资原则2，你相信的，你确定的&#x20;

投资原则3，基本面好，投资方稳

</details>

<details>

<summary>投资难度</summary>

对于单一标的的概率统计分析是简单的，但是足够你在赌场赚的盆满钵满。&#x20;

对于多个标的的概率统计分析，是诺贝尔经济学奖级别的困难。&#x20;

对于单一标的的跨周期性时间校准是较为困难的，而价格点位校准是不可能的。&#x20;

对于多个标的的跨周期性时间校准是神灵的工作。

</details>

<details>

<summary>量化行业 发展规划</summary>

量化行业的发展，是五个阶段：数字化，自动化，标准化，数据化，智能化。

1，数字化：机器人可以执行简单的人工操作。（比如冰山委托，时间加权委托，定投等）&#x20;

2，自动化：机器人可以自动读取市场参数进行简单操作。（如马丁，网格，动态平衡智能持仓，均线系统，通道系统等。）&#x20;

3，标准化：机器人从位于交易所外，转为被内置于交易所之内。（目前处于这个阶段）&#x20;

4，数据化：机器人可以读取链上数据和市场数据，进行简单微观短期分析和简单宏观长期判断，如分析比特币减半时间，分析恐惧贪婪指数，分析合约数据，分析流入流出数据，借助MVRV，S2F，NVT等指标分析比特币的宏观经济，借助山寨季节指标，分析是否处于山寨季节等。&#x20;

5，智能化：机器人可以借助统计学习，机器学习，深度学习，对链上数据和市场数据，进行自动分析和研究，做出复杂的多策略组合交易，调仓，调节杠杆率等的操作。

但是一切都不如，狗吃屎，狗拉屎的狗DOGE屎SHIB网格，狗屎网格是衔尾蛇，是永动机，是大解脱，能救一切苦，真实不虚。

</details>

<details>

<summary>量化行业 合规整改</summary>

### 终止合作不合规业务：

1，第三方授权（将API授权第三方，并托管在第三方服务器）&#x20;

2，嵌套交易所（将用户资产托管于另一家交易所，并与其共享流动性）

### 转为推进合规业务：

3，自托管授权（用户将API授权给自己，将API托管于用户自己控制的服务器中，用户负责对API自行保密，一般是基于一系列开源软件）&#x20;

4，内置机器人（交易所内置的交易机器人）

</details>

## 战士：价值投资策略（俗称：街头捡烟蒂，低估成长，集中投资）

* 巴菲特的，PE和ROE（[链接](https://xueqiu.com/8287840120/102600210)）
* 彼得·林奇的，PEG（[链接1](https://xueqiu.com/8287840120/83909262)，[链接2](https://xueqiu.com/8287840120/74917276)）
* [林园怎么投资](../bfm-trad.-bi-fang-meng-jin-dian/gu-piao-xin-xi-gong-ju/xuan-gu.md)

{% hint style="info" %}
[我怎么投资](../bfm-trad.-bi-fang-meng-jin-dian/gu-piao-xin-xi-gong-ju/xuan-gu.md)（✨🌟✨🌟回测结果在这里🌟✨🌟✨）
{% endhint %}

## 辅助：结构性收益策略（俗称：保护无知，构建组合，分散投资）

* （🔥）固定比例动态平衡（[香农的恶魔，凯利系统](https://www.sohu.com/a/279180185\_99931606)）【算数平均收益与几何平均收益之差】

> **香农阐述了一个通过随机游走赚钱的方法**。他让观众试想一只价格随机上下波动的股票，上下波动并不存在整体趋势。然后把一半资金投入股票，另一半放在“现金”账户中。**每天，股票的价格都会发生变化。每天中午你都要“调整”投资组合。**
>
> 也就是说，你要计算出整个投资组合（股票+现金账户）现在的价值，然后从股票投资中抽出一部分加到现金账户或者从现金账户抽出一部分加到股票投资当中，这样做的目的是与最初股票和现金投资各一半的组合方式保持一致。

> 香农系统假定的是一只股票的几何平均收益为0
>
> 真正想要赚钱的人应该遵循（普通）凯利赌徒的做法，总是追求最大几何平均数。当凯利赌徒被允许按任何比例拆分资金总额投入现金账户和随机游走的股票时，他会选择一半对一半的拆分方式，因为这样做的几何平均数最大。香农的计划是凯利赌博的一个特例。
>
> 由于算数平均收益总是高于几何平均收益，因此，一只几何平均收益为0（假设）的不稳定股票的算数平均收益一定为正值。

### 再平衡有这样几种模式

| 理论                                                                                                                                                                                        |                                                                                                                                                                                                                                  |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **公允理论**                                                                                                                                                                                  | **公允公式**                                                                                                                                                                                                                         |
| 凯利公式：单标的版本                                                                                                                                                                                | 仓位权重=收益率/方差                                                                                                                                                                                                                      |
| 凯利公式：多元化版本                                                                                                                                                                                | 仓位权重向量=收益率向量/协方差矩阵                                                                                                                                                                                                               |
| 马科维兹：CAPM理论                                                                                                                                                                               | 仓位权重=收益率/标准差                                                                                                                                                                                                                     |
| 桥水基金：全天候，波动率倒数理论                                                                                                                                                                          | 仓位权重=1/标准差                                                                                                                                                                                                                       |
| 指数基金：按市值，被动投资                                                                                                                                                                             | 仓位权重=市值比例                                                                                                                                                                                                                        |
| **自创理论**                                                                                                                                                                                  | **自创公式**                                                                                                                                                                                                                         |
| <p>主动基金：按市值，主动投资，季节性</p><p>又名：<a href="../bfm-ds-bi-fang-meng-shu-ju-zhi-chi/zi-chan-pei-zhi/the-tzolkin-calendar/zhuo-er-jin-sheng-ji-10-shi-zhan-mi-xiu.md">帕累托分布与市值修正幂率投资法</a><br></p> | <p>仓位权重=市值比例^修正幂率</p><p></p><p>确定修正幂率：<br>山寨季指标=100山寨币中多少比BTC收益高<br>修正因子=山寨季节指标/50－1 <br>修正幂率=EXP(修正因子)</p>                                                                                                                      |
| [同根策略](https://guhhhhaa.gitbook.io/joinquant/jin-rong-li-lun-zong-jie/zi-chan-pei-zhi/tong-gen-ce-lve-yu-tong-jia-ce-lve)                                                                 | <p>ax = x/(1-x)/(1/(1-x)+1/(1-y)+1/(1-z))</p><p>by = y/(1-y)/(1/(1-x)+1/(1-y)+1/(1-z))</p><p>cz = z/(1-z)/(1/(1-x)+1/(1-y)+1/(1-z))<br></p><p>ax+by+cz=(x/(1-x)+y/(1-y)+z/(1-z))/(1/(1-x)+1/(1-y)+1/(1-z))</p>                   |
| [同架策略](https://guhhhhaa.gitbook.io/joinquant/jin-rong-li-lun-zong-jie/zi-chan-pei-zhi/tong-gen-ce-lve-yu-tong-jia-ce-lve)                                                                 | <p>ax = x^2/(1-x)/(x/(1-x)+y/(1-y)+z/(1-z))</p><p>by = y^2/(1-y)/(x/(1-x)+y/(1-y)+z/(1-z))</p><p>cz = z^2/(1-z)/(x/(1-x)+y/(1-y)+z/(1-z))<br></p><p>ax+by+cz = (x^2/(1-x)+y^2/(1-y)+z^2/(1-z))/(x/(1-x)+y/(1-y)+z/(1-z))</p>     |
| [cholesky分解策略](https://guhhhhaa.gitbook.io/joinquant/jin-rong-li-lun-zong-jie/zi-chan-pei-zhi/ruo-chen-de-ce-lve)                                                                         | <p>对于可用的n种资产，平均收益率向量为b，对数协方差矩阵为A，</p><p>那么对A作cholesky分解得到A=R'R，最优资产配置就是(R^{-1})'b（的归一化） </p><p><a href="https://github.com/sffred/fundFuser/blob/main/README.md">https://github.com/sffred/fundFuser/blob/main/README.md</a></p> |

* [固定比例动态平衡多标的优化（4332221111准则，或322111准则）](../bfm-ds-bi-fang-meng-shu-ju-zhi-chi/zi-chan-pei-zhi/the-haab-calendar/zhuo-er-jin-sheng-ji-6-cang-wei-dan-yuan.md)
* 🔥 [帕累托分布与市值修正幂率投资法](../bfm-ds-bi-fang-meng-shu-ju-zhi-chi/zi-chan-pei-zhi/the-tzolkin-calendar/zhuo-er-jin-sheng-ji-10-shi-zhan-mi-xiu.md)（按照市值的N次幂（N取0～3）分配投资组合，再定期再平衡）（虽然这个链接是比特币，但是道理相同，也可以用于股票）
* [凯利公式](https://guhhhhaa.gitbook.io/joinquant/jin-rong-li-lun-zong-jie/zi-chan-pei-zhi)
* [**马科维兹均值方差模型**  与 **凯利准则（几何平均数准则）**结合](https://guhhhhaa.gitbook.io/joinquant/jin-rong-li-lun-zong-jie/zi-chan-pei-zhi)
* [同根策略 与 同架策略](https://guhhhhaa.gitbook.io/joinquant/jin-rong-li-lun-zong-jie/zi-chan-pei-zhi/tong-gen-ce-lve-yu-tong-jia-ce-lve)
* [cholesky分解策略](https://guhhhhaa.gitbook.io/joinquant/jin-rong-li-lun-zong-jie/zi-chan-pei-zhi/ruo-chen-de-ce-lve)

## 刺客：套利与流动性收益策略（俗称：低买高卖）

* （🔥）固定比例动态平衡（[香农的恶魔，凯利系统](https://www.sohu.com/a/279180185\_99931606)）【算数平均收益与几何平均收益之差】
* [网格交易策略](https://guhhhhaa.gitbook.io/joinquant/joinquant/pan-dian-ge-zhong-wang-ge)【[调和平均数均价买入，算数平均数均价卖出](https://guhhhhaa.gitbook.io/joinquant/joinquant/wang-ge-fu-ying-ying-an-die-dan-mai-de-tiao-he-ping-jun-zhang-dan-mai-de-suan-shu-ping-jun-ji-suan)】

> 网格交易是赚调和平均买入价和算数平均卖出价的差，
>
> 动态平衡交易是赚几何平均收益和算数平均收益的差。
>
> 网格交易假设调和平均买入价为0，那么算数平均卖出价大于调和平均买入价，差价为正值。
>
> 动态平衡交易假设几何平均收益为0，那么算数平均收益大于几何平均收益为正值。

* [定投【调和平均数均价买入】](https://m.sohu.com/a/372948519\_120052323)
  * [优化定投+定卖](https://mp.weixin.qq.com/s?\_\_biz=MzI5ODY5MTQwMA==\&mid=2247488396\&idx=1\&sn=418d4ffe5504c9d67356fa145dcadeb9\&scene=21#wechat\_redirect)
* [金字塔仓位管理法](https://guhhhhaa.gitbook.io/joinquant/jin-rong-li-lun-zong-jie/zi-chan-pei-zhi/jin-zi-ta-cang-wei-guan-li-fa) （金字塔加仓与金字塔减仓，“底仓与浮仓分配”仓位管理的极致）

## 射手：趋势性收益策略（俗称：追涨杀跌）

* 海龟策略（[唐奇安通道](https://www.zhihu.com/zvideo/1386620312193126400)，[ATR开平仓止盈止损](https://www.zhihu.com/zvideo/1408466616892313601)）
* 美林时钟
* [大小市值轮动策略，二八轮动](http://www.360doc.cn/mip/554655681.html)
  * [抱团股会一直涨？无脑执行大小盘轮动策略，轻松跑赢指数5倍](https://mp.weixin.qq.com/s?\_\_biz=MzI5ODY5MTQwMA==\&mid=2247488496\&idx=1\&sn=05754fa8f993b802eaf5d0592496a0c7\&scene=21#wechat\_redirect)
  * [币圈轮动](https://mp.weixin.qq.com/s?\_\_biz=MzI5ODY5MTQwMA==\&mid=2247488576\&idx=1\&sn=015e9165bd427048214359cb4403889c\&chksm=eca0aa67dbd72371f4915c9e1e100825c7744d81e59292e464b0e1e067dfdd2d346cd0a07d87\&scene=178\&cur\_album\_id=1823729338689585161#rd)
* 布林带通道策略（这个不给链接，你自己去搜，出来一堆）
* 双均线策略（这个不给链接，你自己去搜，出来一堆）

{% content-ref url="../bfm-trad.-bi-fang-meng-jin-dian/gu-piao-xin-xi-gong-ju/xuan-gu.md" %}
[xuan-gu.md](../bfm-trad.-bi-fang-meng-jin-dian/gu-piao-xin-xi-gong-ju/xuan-gu.md)
{% endcontent-ref %}

## 法师：赌博策略（就是赌博）

* 马丁格尔(Martingale)策略（等价鞅，亏损加倍投注）
* 反马丁格尔(Anti-Martingale)策略（反等价鞅，盈利加倍投注）

（这个不给链接，你自己去搜，出来一堆）

{% embed url="https://m.hexun.com/futures/2014-08-27/167930226.html" %}

## 不想玩游戏了？可以去抢游戏之神特图的星杯

* [卓尔金历法](../bfm-ds-bi-fang-meng-shu-ju-zhi-chi/zi-chan-pei-zhi/the-tzolkin-calendar/)
  * 智能投顾表格，帮您轻松确定杠杆率，抄底+逃顶
  * **MVRV+S2F+币圈美林时钟+凯利准则收益率和收益率方差控制最大杠杆率+激活函数神经元最终确定仓位+帕累托分布+香农的恶魔+山寨币指数+市值占比幂率修正—共同构筑的基于Excel表格的策略！**
*   [BFM算法](../bfm-rins.-bi-fang-meng-ke-xue-yan-jiu-yuan/suan-fa-yan-jiu-yuan/)

    三角套利的升级与扩展+O(N^3)算法优化的极致+FPGA硬件级别优化+量子退火未来发展
