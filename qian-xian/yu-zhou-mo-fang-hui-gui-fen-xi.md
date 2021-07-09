---
description: TesrAct，是TensorAct，还是Tesseract
---

# 战略资产配置——宇宙魔方（分类网络）

{% page-ref page="management-cockpit-operation/zi-chan-pei-zhi/ling-hang-duo-lei-da/zhuo-er-jin-sheng-ji-5-shen-jing-wang-luo.md" %}

{% hint style="info" %}
### 使用工具

[**TensorFlow**](https://www.tensorflow.org/)  **\|**  [**TensorBoard**](https://www.tensorflow.org/tensorboard?hl=zh-cn)  **\|**  [**TensorBoard.dev**](https://tensorboard.dev/)  **\|**  [**Google Colab**](https://colab.research.google.com/notebooks/intro.ipynb)\*\*\*\*

[**https://playground.tensorflow.org/**](https://playground.tensorflow.org/)\*\*\*\*

### 数据来源

[MVRV](https://www.qkl123.com/data/mvrv/btc)  \|  [S2F](https://www.qkl123.com/data/s2f/btc)  \|  [NVT](https://www.qkl123.com/data/nvt/btc)
{% endhint %}

[22 款神经网络的设计和可视化工具](https://www.huaweicloud.com/articles/d90130bfd852a55e505155e381ebfab1.html)

[Mac版Excel如何添加数据分析功能？](https://answers.microsoft.com/zh-hans/msoffice/forum/all/mac%E7%89%88excel%E5%A6%82%E4%BD%95%E6%B7%BB/4f9c7fcf-ba8a-4f1a-8f00-bc35a43cb480)

[机器学习-回归问题\(Regression\)](https://zhuanlan.zhihu.com/p/127972563)

[标准化、归一化、正规化](https://zhuanlan.zhihu.com/p/73080065)

[一文读懂机器学习分类算法（附图文详解）](https://zhuanlan.zhihu.com/p/82114104)

[Q&A: 机器学习与金融行业](http://www.fintechgl.com/articles/59)

## 问题描述

![](../.gitbook/assets/a4%20%281%29.png)

## 开发环境

![](../.gitbook/assets/ping-mu-kuai-zhao-20210709-shang-wu-7.54.06.png)

[https://www.anaconda.com/](https://www.anaconda.com/)

[https://www.anaconda.com/pycharm](https://www.anaconda.com/pycharm)

![](../.gitbook/assets/qq20210625-2.jpg)

**pandas**是一个数据处理的包，本身提供了许多读取文件的函数，像read\_csv（读取csv文件），read\_excel（读取excel文件）等，只需一行代码就能实现文件的读取。

## 卓尔金历法

我们之前所说的卓尔金历法，解决的是二维空间中的分类问题，

使用的方法是逻辑回归LR，使用的激活函数是sigmoid函数

二维空间，指的是 MVRV，S2F月预测价格/价格， 这两个变量，经过规整化，90%概率分布于（-1，1）后，构成的空间，

喂进去的训练数据是，经过数学处理，90%概率分布于（-1，2）的，基于（50天后的涨跌幅分布）的训练数据。

模型的预计输出结果是，（-1，2）的仓位控制策略模型，

这个模型被称为：卓尔金历法，或，二向箔。 

问题已经被Excel解决，但是不具有扩展性。

## 宇宙魔方

我们现在这个问题属于三维空间中的，分类问题， 

使用的方法是逻辑回归LR，使用的激活函数是sigmoid函数

三维空间，指的是 MVRV，S2F月预测价格/价格，NVT的90日均线， 这三个变量，经过规整化，90%概率分布于（-1，1）后，构成的空间，

喂进去的训练数据是，经过数学处理，90%概率分布于（-1，2）的，基于（50天后的涨跌幅分布）的训练数据。

模型的预计输出结果是，（-1，2）的仓位控制策略模型，

这个模型被称为：宇宙魔方（Tesseract）

问题的模型已经建立了，解决起来就只是时间问题了。

## 规整化算法

第一步：去指数转线性，y = LN\(x/x的几何平均数\)，   
第二步：Logistic 模式 ，y = 1/\(1+e^\(-x\)\)   
第三步：z-score 标准化，y=\(x-μ\)/σ

只要经过这三步处理，不管之前是怎样分布的数据，都会转化为标准正态分布。

## 研发进度

#### 2021.7.9 

安装了Anaconda，借助Anaconda 安装了  
Jupyter Notebook，Jupyter Lab，Numpy，Pandas，TensorFlow，Keras

