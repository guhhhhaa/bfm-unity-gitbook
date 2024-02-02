# 卓尔金升级5——动态图表

{% embed url="https://zhuanlan.zhihu.com/p/151045480" %}

### **E00.动态图表原理**

因为Excel没有时间轴，无法描述运动轨迹，只能表达图表的最终形态。简单来说动态图表就是作图数据源发生了变化。\
![](https://pic2.zhimg.com/80/v2-a5723086798244b536b4641945003255\_1440w.jpg)

在Excel中常见的动态图表元素组合有：**选择器+抽数引擎+图表=动态图表**

![](https://pic1.zhimg.com/80/v2-6b40ad234812f516f11d2935ba518480\_1440w.jpg)

①选择器常见有**Excel控件**，**下拉菜单**，**单选框**、**复选框**、**调节数值器**、**切片器**、**日程表**等；

②常见的抽数引擎有：**透视表**、**常见的链接**、引用函数如：**vlookup**，**offset**，**index与match**等

以下，我们根据选择器的不同，盘点各类动态图表：

### **E01.**RANDBETWEEN**函数**

我们可以看到构成RANDBETWEEN动态图表有三要素：**①数据源+②选择器→③动态图表**

### **02.下拉序列**

下拉序列动态图表有4要素：**①数据源+②选择器+③作图数据源→④动态图表**

还有隐藏的抽数引擎，栗子在作图数据源提取时，用了Vlookup。

### **03透视表+切片器**

切片器动态图表有4要素：**①数据源+②选择器+③作图数据源→④动态图表**

抽数引擎：**透视表**

选择器：**②切片器**

### **E04.透视表+日程表**

日程表动态图表有4要素：**①数据源+②选择器+③作图数据源→④动态图表**

抽数引擎：**透视表**

选择器：**②日程表**

### **E05.控件-组合框**

控件-组合框动态图表有5要素：**①数据源+②选择器+②链接单元格+③作图数据源→④动态图表**

> 与上面不同的是，控件的动态图表在②选择器上，多了一个链接单元格。\
> 个人理解，因为控件是漂浮在单元格之上的对象，不方便利用控件进行运算，于是就有了链接单元格。把控件的不懂选择翻译成链接单元格显示。

### **E06.复选框**

控件-复选框动态图表有5要素：**①数据源+②多个选择器+②多个链接单元格+③作图数据源→④动态图表**

复选框：多个选框控制多个单元格。

### **E07.单选框**

控件-单选框动态图表有5要素：**①数据源+②多个选择器+②1个链接单元格+③作图数据源→④动态图表**

### E08.动态三维地图

版本要求：2016及以上，2013版本可以安装power map插件还能拯救。

话不多说，马上看看动态三维效果图↓