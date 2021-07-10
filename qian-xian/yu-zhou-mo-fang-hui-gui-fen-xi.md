---
description: Te-s-r-act，是 TensorAct，还是 Tesseract ?
---

# 战略资产配置——宇宙魔方（分类网络）

## Te-s-r-act，是 TensorAct，还是Tesseract ?

{% page-ref page="management-cockpit-operation/zi-chan-pei-zhi/ling-hang-duo-lei-da/zhuo-er-jin-sheng-ji-5-shen-jing-wang-luo.md" %}

{% hint style="info" %}
## 问题描述

![](../.gitbook/assets/a4%20%281%29.png)

## [卓尔金历法](https://www.bfm-unity.com/qian-xian/management-cockpit-operation/zi-chan-pei-zhi/ling-hang-duo-lei-da)

我们之前所说的[卓尔金历法](https://www.bfm-unity.com/qian-xian/management-cockpit-operation/zi-chan-pei-zhi/ling-hang-duo-lei-da)，解决的是二维空间中的分类问题，

使用的方法是逻辑回归LR，使用的激活函数是sigmoid函数

二维空间，指的是 MVRV，S2F月预测价格/价格， 这两个变量，经过规整化，90%概率分布于（-1，1）后，构成的空间，

喂进去的训练数据是，经过数学处理，90%概率分布于（-1，2）的，基于（50天后的涨跌幅分布）的训练数据。

模型的预计输出结果是，（-1，2）的仓位控制策略模型，

这个模型被称为：[卓尔金历法](https://www.bfm-unity.com/qian-xian/management-cockpit-operation/zi-chan-pei-zhi/ling-hang-duo-lei-da)，或，二向箔。 

问题已经被Excel解决，但是不具有扩展性。

## [宇宙魔方](https://www.bfm-unity.com/qian-xian/yu-zhou-mo-fang-hui-gui-fen-xi)

我们现在这个问题属于三维空间中的，分类问题， 

使用的方法是逻辑回归LR，使用的激活函数是sigmoid函数

三维空间，指的是 MVRV，S2F月预测价格/价格，NVT的90日均线， 这三个变量，经过规整化，90%概率分布于（-1，1）后，构成的空间，

喂进去的训练数据是，经过数学处理，90%概率分布于（-1，2）的，基于（50天后的涨跌幅分布）的训练数据。

模型的预计输出结果是，（-1，2）的仓位控制策略模型，

这个模型被称为：[宇宙魔方](https://www.bfm-unity.com/qian-xian/yu-zhou-mo-fang-hui-gui-fen-xi)（Tesseract）

问题的模型已经建立了，解决起来就只是时间问题了。

## 使用工具

[Anaconda](https://www.anaconda.com/) \(Jupyter Notebook，Jupyter Lab，Numpy，Pandas，SciPy，TensorFlow，Keras\)还有matplotlib，差点忘了

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

## 开发环境

![](../.gitbook/assets/ping-mu-kuai-zhao-20210709-shang-wu-7.54.06.png)

[https://www.anaconda.com/](https://www.anaconda.com/)

[https://www.anaconda.com/pycharm](https://www.anaconda.com/pycharm)

![](../.gitbook/assets/qq20210625-2.jpg)

**pandas**是一个数据处理的包，本身提供了许多读取文件的函数，像read\_csv（读取csv文件），read\_excel（读取excel文件）等，只需一行代码就能实现文件的读取。

## 规整化算法

第一步：去指数转线性，y = LN\(x/x的几何平均数\)，   
第二步：Logistic 模式 ，y = 1/\(1+e^\(-x\)\)   
第三步：z-score 标准化，y=\(x-μ\)/σ

只要经过这三步处理，不管之前是怎样分布的数据，都会转化为标准正态分布。

## 研发进度

#### 2021.7.9 

安装了Anaconda，借助Anaconda 安装了  
Jupyter Notebook，Jupyter Lab，Numpy，Pandas，SciPy，TensorFlow，Keras  
还有matplotlib，差点忘了

课程？[在看了在看了](https://www.bilibili.com/video/BV1rz4y117p1)。

```python
from tensorflow import keras
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
```

找到了 [TensorFlow学习笔记](https://www.zhihu.com/column/c_1377756991213998081) ，发现逻辑回归分类问题应该用**交叉熵损失函数，**而不是**均方误差MSE损失函数**

\*\*\*\*[交叉熵](https://baike.baidu.com/item/%E4%BA%A4%E5%8F%89%E7%86%B5/8983241) \|  ****[损失函数](https://baike.baidu.com/item/%E6%8D%9F%E5%A4%B1%E5%87%BD%E6%95%B0/1783236)  \|  [归一化指数函数](https://baike.baidu.com/item/%E5%BD%92%E4%B8%80%E5%8C%96%E6%8C%87%E6%95%B0%E5%87%BD%E6%95%B0)\(Softmax函数\)

[matplotlib-tutorial](https://www.runoob.com/w3cnote/matplotlib-tutorial.html) 学会复制粘贴了，这是一种进步

[python-tutorial](https://www.runoob.com/python/python-tutorial.html) 找到了python基础教程，重新回去学python

不学了，要吐了

再想想

找到了一本书：利用Python进行数据分析：[![](https://gblobscdn.gitbook.com/spaces%2F-LF_s_ql-GHXb31QEE8_%2Favatar.png?alt=media)README](https://seancheney.gitbook.io/python-for-data-analysis-2nd/)

找到了英文版

[https://github.com/wesm/pydata-book](https://github.com/wesm/pydata-book)

找到了中文版

[https://github.com/BrambleXu/pydata-notebook](https://github.com/BrambleXu/pydata-notebook)

* [Chapter 4: NumPy Basics: Arrays and Vectorized Computation（NumPy基础：数组和向量化计算）](http://nbviewer.jupyter.org/github/LearnXu/pydata-notebook/tree/master/Chapter-04/)
  * [4.1 The NumPy ndarray: A Multidimensional Array Object（ndarray: 多维数组对象\)](http://nbviewer.jupyter.org/github/LearnXu/pydata-notebook/blob/master/Chapter-04/4.1%20The%20NumPy%20ndarray%EF%BC%88%E5%A4%9A%E7%BB%B4%E6%95%B0%E7%BB%84%E5%AF%B9%E8%B1%A1%EF%BC%89.ipynb)
  * [4.2 Universal Functions: Fast Element-Wise Array Functions（通用函数：快速点对点数组函数）](http://nbviewer.jupyter.org/github/LearnXu/pydata-notebook/blob/master/Chapter-04/4.2%20Universal%20Functions%20%28%E9%80%9A%E7%94%A8%E5%87%BD%E6%95%B0%29.ipynb)
  * [4.3 Array-Oriented Programming with Arrays（数组导向编程）](http://nbviewer.jupyter.org/github/LearnXu/pydata-notebook/blob/master/Chapter-04/4.3%20Array-Oriented%20Programming%20with%20Arrays%EF%BC%88%E6%95%B0%E7%BB%84%E5%AF%BC%E5%90%91%E7%BC%96%E7%A8%8B%EF%BC%89.ipynb)
* [Chapter 5: Getting Started with pandas（开始使用pandas）](http://nbviewer.jupyter.org/github/LearnXu/pydata-notebook/tree/master/Chapter-05/)
  * [5.1 Introduction to pandas Data Structures（pandas的数据结构）](http://nbviewer.jupyter.org/github/LearnXu/pydata-notebook/blob/master/Chapter-05/5.1%20Introduction%20to%20pandas%20Data%20Structures%EF%BC%88pandas%E7%9A%84%E6%95%B0%E6%8D%AE%E7%BB%93%E6%9E%84%EF%BC%89.ipynb)
  * [5.2 Essential Functionality（主要功能）](http://nbviewer.jupyter.org/github/LearnXu/pydata-notebook/blob/master/Chapter-05/5.2%20Essential%20Functionality%EF%BC%88%E4%B8%BB%E8%A6%81%E5%8A%9F%E8%83%BD%EF%BC%89.ipynb)
  * [5.3 Summarizing and Computing Descriptive Statistics（汇总和描述性统计）](http://nbviewer.jupyter.org/github/LearnXu/pydata-notebook/blob/master/Chapter-05/5.3%20Summarizing%20and%20Computing%20Descriptive%20Statistics%EF%BC%88%E6%80%BB%E7%BB%93%E5%92%8C%E6%8F%8F%E8%BF%B0%E6%80%A7%E7%BB%9F%E8%AE%A1%EF%BC%89.ipynb)
* [Chapter 7: Data Cleaning and Preparation（数据清洗和准备）](http://nbviewer.jupyter.org/github/LearnXu/pydata-notebook/tree/master/Chapter-07/)
  * [7.1 Handling Missing Data（处理缺失数据）](http://nbviewer.jupyter.org/github/LearnXu/pydata-notebook/blob/master/Chapter-07/7.1%20Handling%20Missing%20Data%EF%BC%88%E5%A4%84%E7%90%86%E7%BC%BA%E5%A4%B1%E6%95%B0%E6%8D%AE%EF%BC%89.ipynb)
  * [7.2 Data Transformation（数据变换）](http://nbviewer.jupyter.org/github/LearnXu/pydata-notebook/blob/master/Chapter-07/7.2%20Data%20Transformation%EF%BC%88%E6%95%B0%E6%8D%AE%E5%8F%98%E6%8D%A2%EF%BC%89.ipynb)
  * [7.3 String Manipulation（字符串处理）](http://nbviewer.jupyter.org/github/LearnXu/pydata-notebook/blob/master/Chapter-07/7.3%20String%20Manipulation%EF%BC%88%E5%AD%97%E7%AC%A6%E4%B8%B2%E5%A4%84%E7%90%86%EF%BC%89.ipynb)
* [Chapter 11: Time Series（时间序列）](http://nbviewer.jupyter.org/github/LearnXu/pydata-notebook/tree/master/Chapter-11/)
  * [11.1 Date and Time Data Types and Tools（日期和时间数据类型及其工具）](http://nbviewer.jupyter.org/github/LearnXu/pydata-notebook/blob/master/Chapter-11/11.1%20Date%20and%20Time%20Data%20Types%20and%20Tools%EF%BC%88%E6%97%A5%E6%9C%9F%E5%92%8C%E6%97%B6%E9%97%B4%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8B%E5%8F%8A%E5%85%B6%E5%B7%A5%E5%85%B7%EF%BC%89.ipynb)
  * [11.2 Time Series Basics（时间序列基础）](http://nbviewer.jupyter.org/github/LearnXu/pydata-notebook/blob/master/Chapter-11/11.2%20Time%20Series%20Basics%EF%BC%88%E6%97%B6%E9%97%B4%E5%BA%8F%E5%88%97%E5%9F%BA%E7%A1%80%EF%BC%89.ipynb)
  * [11.3 Date Ranges, Frequencies, and Shifting（日期范围，频度，和位移）](http://nbviewer.jupyter.org/github/LearnXu/pydata-notebook/blob/master/Chapter-11/11.3%20Date%20Ranges%2C%20Frequencies%2C%20and%20Shifting%EF%BC%88%E6%97%A5%E6%9C%9F%E8%8C%83%E5%9B%B4%EF%BC%8C%E9%A2%91%E5%BA%A6%EF%BC%8C%E5%92%8C%E4%BD%8D%E7%A7%BB%EF%BC%89.ipynb)
* [Chapter 12: Advanced pandas（高级pandas用法）](http://nbviewer.jupyter.org/github/LearnXu/pydata-notebook/tree/master/Chapter-12/)
  * [12.1 Categorical Data（类别数据）](http://nbviewer.jupyter.org/github/LearnXu/pydata-notebook/blob/master/Chapter-12/12.1%20Categorical%20Data%EF%BC%88%E7%B1%BB%E5%88%AB%E6%95%B0%E6%8D%AE%EF%BC%89.ipynb)
* [Chapter 14: Data Analysis Examples（数据分析实例）](http://nbviewer.jupyter.org/github/LearnXu/pydata-notebook/tree/master/Chapter-14/)
  * [14.1 USA.gov Data from Bitly（USA.gov数据集）](http://nbviewer.jupyter.org/github/LearnXu/pydata-notebook/blob/master/Chapter-14/14.1%20USA.gov%20Data%20from%20Bitly%EF%BC%88USA.gov%E6%95%B0%E6%8D%AE%E9%9B%86%EF%BC%89.ipynb)
  * [14.2 MovieLens 1M Dataset（MovieLens 1M数据集）](http://nbviewer.jupyter.org/github/LearnXu/pydata-notebook/blob/master/Chapter-14/14.2%20MovieLens%201M%20Dataset%EF%BC%88MovieLens%201M%E6%95%B0%E6%8D%AE%E9%9B%86%EF%BC%89.ipynb)
  * [14.3 US Baby Names 1880–2010（1880年至2010年美国婴儿姓名](http://nbviewer.jupyter.org/github/BrambleXu/pydata-notebook/blob/master/Chapter-14/14.3%20US%20Baby%20Names%201880%E2%80%932010%EF%BC%881880%E5%B9%B4%E8%87%B32010%E5%B9%B4%E7%BE%8E%E5%9B%BD%E5%A9%B4%E5%84%BF%E5%A7%93%E5%90%8D%EF%BC%89.ipynb)\*\*\*\*

**pandas**是一个数据处理的包，本身提供了许多读取文件的函数，像read\_csv（读取csv文件），read\_excel（读取excel文件）等，只需一行代码就能实现文件的读取。

[python pandas read\_html快读读取中国商情网的A股，港股以及新三板股票](https://www.bilibili.com/video/BV1aQ4y1A7fh)

[pandas.read\_csv 详细介绍](https://www.gairuo.com/p/pandas-read-csv)

[pandas.read\_excel 详细介绍](https://www.gairuo.com/p/pandas-read-excel)

[30分钟带你入门数据分析工具 Pandas](https://oicebot.github.io/2018/09/05/30-mins-into-pandas-for-data-science.html)

[十分钟入门 Pandas](https://www.pypandas.cn/docs/getting_started/10min.html)

* CSV
  * [写入 CSV 文件 \(opens new window\)](https://pandas.pydata.org/pandas-docs/stable/user_guide/io.html#io-store-in-csv)。

```text
In [143]: df.to_csv('foo.csv')
```

* * 读取 CSV 文件数据：

```text
In [144]: pd.read_csv('foo.csv')
```

* Excel
  * 详见 [Excel \(opens new window\)](https://pandas.pydata.org/pandas-docs/stable/user_guide/io.html#io-excel)文档。
  * 写入 Excel 文件：

```text
In [147]: df.to_excel('foo.xlsx', sheet_name='Sheet1')
```

* * 读取 Excel 文件：

```text
In [148]: pd.read_excel('foo.xlsx', 'Sheet1', index_col=None, na_values=['NA'])
```

