# 👩‍🔬 👨‍🔬 三角套利实验室 🧪 🔬

## 👩‍🔬 👨‍🔬 ➡️ 三角套利实验室 ⚠️ ☢️ ☠️ 🔥 💥 🧪 🔬 💻

![](../../.gitbook/assets/bfm-unity-hei-dong-tan-suo-.png)

{% hint style="info" %}
我们在尝试部署BellmanFord算法在币安上或者Uniswap上，进行单交易所内部多币种的多角套利。

如果在币安上运行，需要对接交易所API。使用python，ccxt，asyncio，通过异步并发协程的方式运行Bellman-Ford算法，以寻找套利路径。

我们发现了一个可以参考的项目：Peregrine，它可以**打印**出一个套利路径，但是没有**执行**下单的程序。

我们需要参考Peregrine的代码，自己编写并添加这个**执行**下单的程序。
{% endhint %}

![](../../.gitbook/assets/bfm-unity-zhan-lve-mu-biao-kai-fa-xing-bei-.png)

{% hint style="info" %}
[**BellmanFord算法**](https://www.bfm-unity.com/what-is-bfm-al) **+** [**参考文献**](https://www.bfm-unity.com/what-is-bfm-al/bfm-al-ckwx) **+** [**三角套利核心代码**](https://www.bfm-unity.com/ruan-jian-bfm-on-python) **+** [**陵墓**](https://www.bfm-unity.com/what-is-bfm-al/lo-st) **+** [**量子退火和FPGA**](https://guhhhhaa.gitbook.io/bfm-unity-doc-v1/bfm-suan-fa-de-wei-lai-fa-zhan-wei-wan-cheng)\*\*\*\*

千千的搬砖之王策略  \|  [**视频**](https://mp.weixin.qq.com/s/MsXdWAGJR0Kl9BPIUPxQgA)  **\|**  [**代码**](https://guhhhhaa.gitbook.io/bfm-unity-doc-v1/ruan-jian-bfm-on-python/qian-qian-de-liang-hua-shi-jie-hou-ban-dai-ma)  
****BellmanFord三角套利策略，是千千搬砖之王策略的算法升级版

千千的其它视频：[**上篇**](https://mp.weixin.qq.com/s/lVqcoBvtmyLaohz7DLtIoA)  **\|**  [**下篇**](https://mp.weixin.qq.com/s/6qL4redQ3lFiNvZOowpBaA)  **\|**  [**部署**](https://mp.weixin.qq.com/s/6bKVOqcYppqta3zRdMtvWA)  **\|**  [**回测**](https://mp.weixin.qq.com/s/Ju4XFDHTq7wk2wokArmKGw)  **\|**  [**三角套利策略介绍**](https://mp.weixin.qq.com/s/G5t7TyIyrH40Kl55feTDIw)\*\*\*\*

[**宝塔面板**](https://www.bt.cn/)**（**[**安装教程**](https://www.bt.cn/bbs/thread-19376-1-1.html)**） \|**  [**阿里云**](https://www.aliyun.com/)  **\|**  [**腾讯云**](https://cloud.tencent.com/)

**相关知乎问题：**

* [Bellman-Ford算法是如何用于三角套利的？](https://www.zhihu.com/question/360354203)
* [如何利用云计算（如AWS，阿里云，腾讯云）部署FPGA实例，用于BellmanFord三角套利？](https://www.zhihu.com/question/448419550)

我已经[**联系币安**](https://www.binance.com/zh-CN/my/user-support/feedback/entry)让他们自己研发三角套利策略了，不知道以[**币安**](https://www.binance.com/cn)的研发实力，会不会搞出一个功能，让散户人人都可以参与三角套利，这样散户只需要投资就行了，不需要研究技术。
{% endhint %}

![](../../.gitbook/assets/b49d19a6fef2385395ae687a10007929.png)

## 〇，策略学习

[**三角套利策略介绍**](https://mp.weixin.qq.com/s/G5t7TyIyrH40Kl55feTDIw) **+** [**考虑交易成本的三角套利**](https://www.jianshu.com/p/e50a52312a47)\*\*\*\*

[**BellmanFord算法**](https://www.bfm-unity.com/what-is-bfm-al) **+** [**参考文献**](https://www.bfm-unity.com/what-is-bfm-al/bfm-al-ckwx)\*\*\*\*

## 一，环境搭建

[**宝塔面板**](https://www.bt.cn/)**（**[**安装教程**](https://www.bt.cn/bbs/thread-19376-1-1.html)**） \|**  [**阿里云**](https://www.aliyun.com/)  **\|**  [**腾讯云**](https://cloud.tencent.com/)\*\*\*\*

千千的其它视频：[**上篇**](https://mp.weixin.qq.com/s/lVqcoBvtmyLaohz7DLtIoA)  **\|**  [**下篇**](https://mp.weixin.qq.com/s/6qL4redQ3lFiNvZOowpBaA)  **\|**  [**部署**](https://mp.weixin.qq.com/s/6bKVOqcYppqta3zRdMtvWA)  **\|**  [**回测**](https://mp.weixin.qq.com/s/Ju4XFDHTq7wk2wokArmKGw) ****

### **量化框架**

[**CCXT**](https://github.com/ccxt/ccxt)\*\*\*\*

\*\*\*\*[**Peregrine**](https://github.com/wardbradt/peregrine)**（**[**文档**](https://guhhhhaa.gitbook.io/peregrine/)**）**

[**AIOQuant**](https://github.com/CongZhengithub/aioquant)**（**[**视频**](https://space.bilibili.com/479971824)**）**

\*\*\*\*[**TheNextQuant**](https://thenextquant.com/intro)**（已下架）**

{% page-ref page="liang-hua-kuang-jia-tui-jian-ke-cheng.md" %}

## 二，对接准备

[**币安多币种自动化策略API操作指南**](https://zhuanlan.zhihu.com/p/55109087) **（**[**本地链接**](https://www.bfm-unity.com/command-room-discovery/san-jiao-tao-li-shi-yan-shi/bi-an-duo-bi-zhong-zi-dong-hua-ce-lve-api-cao-zuo-zhi-nan)**）**

## 三，代码**参考**

### **eregrine**

{% embed url="https://github.com/wardbradt/peregrine" %}

{% embed url="https://guhhhhaa.gitbook.io/peregrine/peregrine-cn" %}

### bmino-BTA & btrader

{% embed url="https://github.com/bmino/binance-triangle-arbitrage" %}

{% embed url="https://github.com/gabriel-milan/btrader" %}

[币圈搬砖、数字货币量化套利，从入门到实战（六）三角搬砖](https://www.jianshu.com/p/14dbaa02777a)

[**数字货币量化系统 CCXT 框架实战三角套利**](http://www.digtime.cn/articles/282/shu-zi-huo-bi-liang-hua-xi-tong-ccxt-kuang-jia-shi-zhan-san-jiao-tao-li)**（**[**本地链接**](https://www.bfm-unity.com/command-room-discovery/san-jiao-tao-li-shi-yan-shi/shu-zi-huo-bi-liang-hua-xi-tong-ccxt-kuang-jia-shi-zhan-san-jiao-tao-li)**）**[**课程地址**](https://study.163.com/course/courseMain.htm?courseId=1006162003)\*\*\*\*

[**https://guhhhhaa.gitbook.io/arbitrage-github/**](https://guhhhhaa.gitbook.io/arbitrage-github/)\*\*\*\*

[**三角套利核心代码**](https://www.bfm-unity.com/ruan-jian-bfm-on-python) **+** [**陵墓**](https://www.bfm-unity.com/what-is-bfm-al/lo-st)

### **技术难点**

{% page-ref page="yi-bu-bing-fa-xie-cheng-1/" %}

{% page-ref page="yi-bu-bing-fa-xie-cheng-1/yi-bu-bing-fa-xie-cheng.md" %}

## **四，FPGA**

[用这个库居然可以使用Python进行FPGA逻辑开发](https://zhuanlan.zhihu.com/p/56095014)

[**量子退火和FPGA**](https://guhhhhaa.gitbook.io/bfm-unity-doc-v1/bfm-suan-fa-de-wei-lai-fa-zhan-wei-wan-cheng)\*\*\*\*

## **五，量子退火**

[**量子退火和FPGA**](https://guhhhhaa.gitbook.io/bfm-unity-doc-v1/bfm-suan-fa-de-wei-lai-fa-zhan-wei-wan-cheng)\*\*\*\*

