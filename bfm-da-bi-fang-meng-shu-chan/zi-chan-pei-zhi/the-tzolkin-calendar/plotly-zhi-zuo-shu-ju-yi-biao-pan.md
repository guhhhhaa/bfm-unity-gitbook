# Plotly-制作数据仪表盘

{% embed url="https://zhuanlan.zhihu.com/p/395793035" %}

{% embed url="https://zhuanlan.zhihu.com/p/60416273" %}

### **Plotly简要概述**

plotly Python 包是一个构建在 [plotly.js](https://www.zhihu.com/search?q=plotly.js\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22article%22%2C%22sourceId%22%3A60416273%7D) 上的开源库，而后者又是构建在 d3.js 上的。我们将使用一个 plotly 的“包装器”——cufflinks，它可以 plotly 的使用变得更加简单。整个堆叠顺序是cufflinks>plotly>plotly.js>d3.js，意味着我们同时获得了 Python 的编程高效性和d3强大的图形交互能力。（毕竟d3.js是全世界公认的第一可视化框架！）

本文中所有工作都是使用 plotly+cufflinks 在 Jupyter Notebook 中完成的。在开始前，我们需要使用 `pip install cufflinks plotly` 在 Python 环境中安装这两个包，然后在 [jupyter notebook](https://www.zhihu.com/search?q=jupyter+notebook\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22article%22%2C%22sourceId%22%3A60416273%7D) 中导入这两个包：

```
# 导入plotly包
import plotly.plotly as py
import plotly.graph_objs as go
from plotly.offline import iplot,init_notebook_mode

# 使用离线模式的 plotly + cufflinks
import cufflinks
cufflinks.go_offline(connected=True)
```

\\

### **单变量分布：直方图和箱线图**

单变量-单变量制图是开始一个数据分析的标准方法。直方图是绘制单变量分布的首选方式。在这里，我使用的数据来源是我个人在 medium 网站上所写过文章的统计信息，让我们先来制作一个关于文章点赞次数的交互式直方图（df 是一个标准的 Pandas 数据结构）。

```
df['claps'].iplot(kind='hist', xTitle='claps', yTitle='count', title='Claps Distribution')
```

![](https://pic2.zhimg.com/v2-8fb1b843a9351211c7cbb8a846256cf1\_b.jpg)

\\

如果你已经习惯使用\*\*`matplotlib`\*\*，你所需要做的只是在你原有代码的基础上添加一个字母，即把 plot 改为 iplot，就可以得到一个更加好看的交互式图标！我们可以通过鼠标的滑动获得更多的数据几节，还可以放大图的各个部分。

如果我们想要绘制重叠的直方图，这很简单：

```
df[['time_started', 'time_published']].iplot(    kind='hist',    histnorm='percent',    barmode='overlay',    xTitle='Time of Day',    yTitle='(%) of Articles',    title='Time Started and Time Published')
```

![](https://pic3.zhimg.com/80/v2-6e388bcbc71c2de6d30e4b11beb65a5a\_1440w.jpg)

\\

通过一点 `pandas` 处理，我们还可以制作一个条形图：

```
#重采样获得每月的均值 e Views and Reads')

df2 = df[['view','reads','published_date']].set_index('published_date').resample('M').mean()
df2.iplot(kind='bar', xTitle='Date', yTitle='Average',    title='Monthly Average Views and Reads')
```

![](https://pic2.zhimg.com/80/v2-7d03a1636e1884a9d12fedab18455191\_1440w.jpg)

\\

就像我们前面看到的那样，pandas+plotly+cufflinks 这一组合的功能非常强大。如果我们要绘制一个关于每篇文章粉丝数量在不同发表渠道的分布情况的箱线图，我们可以先使用 pandas 中DataFrame 的 pivot(透视表) 功能，然后再绘制图表，如下：\\

```
df.pivot(columns='publication', values='fans').iplot(  kind='box', yTitle='fans',title='Fans Distribution by Publication')
```

![](https://pic3.zhimg.com/v2-fc79c1658cb05c5634529e6b2f28e402\_b.jpg)

\\

交互式图表的好处就在于，我们可以尽情地探索图表中的数据。特别是在箱线图中，包含的信息很多，如果不能局部放大查看，我们可能会错过这些信息。\\

### [**散点图**](https://www.zhihu.com/search?q=%E6%95%A3%E7%82%B9%E5%9B%BE\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22article%22%2C%22sourceId%22%3A60416273%7D)

散点图是大多数分析的核心，它可以使我们看到变量随着时间的演变情况，也可以看到两种变量之间的关系。\\

### **时间序列**

现实世界中的大部分数据都与时间相关。幸运的是，plotly + cufflinks 在设计之初就考虑到了时间序列的可视化。让我们来创建一个关于我写过文章情况的 dataframe，看看它的各项指标是怎么随着时间变化的。

```
#创建一个数据集，只包括发布在Towards Data Science渠道的文章
tds = df[df['publication'] == 'Towards Data Science']. set_index('published_date')

#将阅读时间作为时间序列
tds[['claps', 'fans', 'title']].iplot(    y='claps', mode='lines+markers', secondary_y = 'fans',    secondary_y_title='Fans', xTitle='Date', yTitle='Claps',    text='title', title='Fans and Claps over Time')
```

![](https://pic2.zhimg.com/80/v2-6029f85ef2dc3c6858d8c18c580b9859\_1440w.jpg)

\\

\\

我们在一行代码里完成了很多不同的事情:

\- 自动获得了格式友好的时间序列作为x轴

\- 添加一个次坐标轴（第二y轴），因为上图中的两个变量的值范围不同。

\- 添加文章的标题到每个数据点中（鼠标放上去可以显示文章名和[变量值](https://www.zhihu.com/search?q=%E5%8F%98%E9%87%8F%E5%80%BC\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22article%22%2C%22sourceId%22%3A60416273%7D)）

\\

如果要从图表上了解更多的信息，我们还可以很容易地添加文本注释：

```
tds_monthly_totals.iplot(mode='lines+markers+text', text=text, y='word_count', opacity=0.8,   xTitle='Date', yTitle='Word Count',title='Total Word Count by Month')
```

![](https://pic4.zhimg.com/80/v2-363572d1db14713826794a74892995f3\_1440w.jpg)

\\

\\

对于由第三个分类变量着色的双变量散点图，我们使用：

```
#read_time代表文章所需阅读时长，read_ratio代表阅读比例，即阅读文章的人数/点击查看的人数
df.iplot( x='read_time', y='read_ratio',

# 定义类别变量  
categories='publication',xTitle='Read 
Time',yTitle='Reading Percent', title='Reading Percent vs Read Ratio by Publication')
```

![](https://pic4.zhimg.com/80/v2-61af7c8be57460f220c27eb9992c3877\_1440w.jpg)

\\

如果要在图表中体现三个[数值变量](https://www.zhihu.com/search?q=%E6%95%B0%E5%80%BC%E5%8F%98%E9%87%8F\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22article%22%2C%22sourceId%22%3A60416273%7D)，我们还可以使用气泡图，如下图:横坐标、纵坐标、气泡的大小分别代表三个不同的变量——文章字数的对数、阅读数量、阅读比例。

\\

```
tds.iplot(x='word_count',y='reads', size='read_ratio',text=text, mode='markers',    

# Log xaxis    
layout=dict(xaxis=dict(type='log', title='Word Count'), yaxis=dict(title='Reads'),        title='Reads vs Log Word Count Sized by Read Ratio'))
```

![](https://pic2.zhimg.com/80/v2-bec6bb4afb4ae87dd70a66402bc23121\_1440w.jpg)

\\

\\

再做一点工作，我们甚至可以在一个图表中体现四个变量！

![](https://pic3.zhimg.com/80/v2-02bc182d62e862af87cfafb963e3fc96\_1440w.jpg)

\\

\\

结合 pandas 对数据进行统计处理，我们可以得到很多非常有价值的图，比如下面这张关于不同文章发表渠道的读者点击查看数量的变化趋势图，显然名为`Toward Data Science`的发表渠道能给文章带来更多的点击量。

![](https://pic1.zhimg.com/80/v2-2786a6a5c8041af5c9e232cf0c778ff4\_1440w.jpg)

\\

### **更高级的图表**

接下来所讲述的图表大家可能不会经常用到，但是非常酷炫，值得了解一下。同样，我们仍然只使用一行代码就可以完成这些超级图表。\\

#### **散点图矩阵**

当我们想要探索许多变量之间的关系时，[散点图矩阵](https://www.zhihu.com/search?q=%E6%95%A3%E7%82%B9%E5%9B%BE%E7%9F%A9%E9%98%B5\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22article%22%2C%22sourceId%22%3A60416273%7D)是非常好的选择。

```
import plotly.figure_factory as ff
figure = ff.create_scatterplotmatrix(df[['claps', 'publication','views','read_ratio','word_count']],diag='histogram', index='publication')
```

![](https://pic1.zhimg.com/80/v2-5344f1a69aaee8b1605399f202d9ada8\_1440w.jpg)

以上的散点矩阵图仍然是可以交互的，可以自由放大缩小，查看各个数据点的详细信息。

\\

#### **相关系数热力图**

为了将数值型变量的相关性可视化，我们可以先计算相关系数，接着就可以创建一个带注释的热力图:

```
corrs = df.corr()
figure = ff.create_annotated_heatmap(z=corrs.values,x=list(corrs.columns),y=list(corrs.index), annotation_text=corrs.round(2).values, showscale=True)
```

![](https://pic4.zhimg.com/80/v2-2cbc4e9511891505b800b3926c37d2d7\_1440w.jpg) ![](https://pic4.zhimg.com/80/v2-fd38cea2d909455f3e5ae6193719fe07\_1440w.jpg)

\\

我们还可以绘制非常酷炫的3D[表面图](https://www.zhihu.com/search?q=%E8%A1%A8%E9%9D%A2%E5%9B%BE\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22article%22%2C%22sourceId%22%3A60416273%7D)和3D气泡图：

![](https://pic4.zhimg.com/80/v2-01656a21d94782c9d26ad0211b129fe7\_1440w.jpg) ![](https://pic1.zhimg.com/80/v2-507a0078708548d80ab6e5d9637016c0\_1440w.jpg)

\\

#### **云制图——Plotly Chart Studio**

当你使用 plotly 在 notebook 中绘制图表时，你可能注意到了每幅图的右下角都有一个链接 “Export to plot.ly” 。如果你点击该链接，就会跳转到名为[`chart studio`](https://www.zhihu.com/search?q=chart+studio\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22article%22%2C%22sourceId%22%3A60416273%7D)的云制图平台，然后你就可以对自己的图标进行润色，添加注释、改改颜色、清理一些不必要的内容等等。

\\

![](https://pic2.zhimg.com/80/v2-98bce04d36e115b9faa8324dedf295d5\_1440w.jpg)

\\

你还可以在线发布该图表，任何人可以直接通过链接访问到你的图表。\
（比如我的这个3D图，在浏览器中输入后方链接可直接抵达:[https://plot.ly/\~Allencxl/3/](https://link.zhihu.com/?target=https%3A//plot.ly/\~Allencxl/3/)）

前面所述的内容还不算是这个库的所有功能，非常鼓励各位小伙伴们去查看 plotly 和 cufflinks 的文档，肯定会有更多不可思议的神级可视化在等着你！

![](https://pic2.zhimg.com/80/v2-b0fa0cf59ed17d41ee8ffcd1cac87499\_1440w.jpg)

\
美国风力发电厂的分布情况

\\

### **总结**

我已经因为固执地使用`matploblib`而浪费了太多时间，所以希望大家能通过这篇文章学习到一种新的方式提升自己的绘图效率。\
另外，当我们在选择绘图库的时候，有几点是永远需要考虑的：

\- 用少量的代码进行数据探索

\- 可以实时与数据交互，查看[数据子集](https://www.zhihu.com/search?q=%E6%95%B0%E6%8D%AE%E5%AD%90%E9%9B%86\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22article%22%2C%22sourceId%22%3A60416273%7D)情况

\- 根据自己的需要，选择性挖掘数据中的细节

\- 非常便利地润色最终演示的图表

而到目前为止，能够在 Python 中实现上述需求的不二选择便是 plotly。plotly 使我们能够快速地进行可视化，让我们通过与图表的交互更好地了解我们的数据。日常工作中，在使用其他绘图库的时候，我感觉绘图是一项单调乏味的任务，但是使用 plotly 时，我觉得绘图是数据科学中相当有趣的工作之一！

\\

> 作者：Will Koehrsen 编译&图片汉化：Allen\
> 原文链接：[https://towardsdatascience.com/](https://link.zhihu.com/?target=https%3A//towardsdatascience.com/the-next-level-of-data-visualization-in-python-dd6e99039d5e)
