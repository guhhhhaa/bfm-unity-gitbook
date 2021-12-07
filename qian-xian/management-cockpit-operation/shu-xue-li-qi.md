# 数学利器

## 1，无监督学习的归一化操作伪代码——

适用于任何**无顺序状态数据**（**不管数据分布如何**），应用sigmod函数之前的**归一化操作**：

```python
定义 a_1, b_1
定义 f_1(), f_2()

f_2() = LN(f_1()/a_1)
        /b_1 
        * 4 
# 因为sigmod函数x取(-4,4)时，y在约(0,1), 所以这里最后*4
# 你也可以*5，大概覆盖增长区间就行

a_1 = 几何平均数(f_1()) 
# 几何平均数：GEOMEAN

b_1 = 算数平均数(极大值(LN(f_1()/a_1),N)
               -极小值(LN(f_1()/a_1),N)
              ) 
# 算数平均数：AVERAGE
```

### 找极值点

**二阶导数**大于0，图象为凹；

**二阶导数**小于0，图象为凸；

**二阶导数**等于0，不凹不凸。

当一阶导数等于0，而二阶导数大于0时，为极小值点。

当一阶导数等于0，而二阶导数小于0时，为极大值点；

当一阶导数和二阶导数都等于0时，为驻点。

在导数为0的点的两侧若函数单调性一致，则此点不是极值点

极值点因子 = 此处的二阶导数/ABS(此处的一阶导数)

```c
极值点因子 = 此处的二阶导数/ABS(此处的一阶导数)

// 找极值点因子偏离0最大的离群点(即一阶导数绝对值最小，二阶导数绝对值最大)
// 跟随二阶导数的符号
// 大于0时，为极小值点；小于0时，为极大值点。
```

### 统计振幅

取极值点因子最大的10个点和最小的10个点

```python
定义 a_1, b_1
定义 f_1(), f_2()

f_2() = LN(f_1()/a_1)
        /b_1 
        * 4 
# 因为sigmod函数x取(-4,4)时，y在约(0,1), 所以这里最后*4
# 你也可以*5，大概覆盖增长区间就行

a_1 = 几何平均数(f_1()) 
# 几何平均数：GEOMEAN

b_1 = 算数平均数(极大值(LN(f_1()/a_1),N)
               -极小值(LN(f_1()/a_1),N)
              ) 
# 算数平均数：AVERAGE
```

## 2，判断牛熊，用于决策的，施密特触发器伪代码：

IF函数 [**其他函数**](https://zhuanlan.zhihu.com/p/51366759) IFS函数 Choose函数\
[**多条件逻辑函数**](https://zhuanlan.zhihu.com/p/38326242)：AND、OR、IF

```python
定义 x_0, y_0 # 基期输入，基期状态 
定义 x_1, y_1 # 现期输入，现期状态 
定义并赋值 x_L = ?
定义并赋值 x_H = ?
定义函数 y_1 = 施密特触发器(x_1,y_0) # 现期状态=施密特触发器(现期输入，基期状态)
------------------------
上升的施密特触发器(x_1,y_0, x_L,x_H) { 
if x_1>x_H, return 1 # 如果，现期输入>高输入阈值，状态置1 
else if x_1<x_L, return 0 # 如果，现期输入<低输入阈值，状态置0 
else return y_0 # 否则，维持原状态 
}

下降的施密特触发器(x_1,y_0, x_L,x_H) { 
if x_1>x_H, return 0 # 如果，现期输入>高输入阈值，状态置1 
else if x_1<x_L, return 1 # 如果，现期输入<低输入阈值，状态置0 
else return y_0 # 否则，维持原状态 
}
------------------------
定义并赋值 w = ?

sigmod_上升的施密特触发器(x_1,y_0, x_L,x_H,w) {
if x_1>x_H-w && x_1>x_L+w, return y_0/(sigmod((x_0-x_H)/w*4))*(sigmod((x_1-x_H)/w*4)) #如果输入进入下降通道且不在上升通道内，状态更新 
else if x_1<x_H-w && x_1<x_L+w, return 1-(1-y_0)/(1-sigmod((x_0-x_L)/w*4))*(1-sigmod((x_1-x_L)/w*4))  #如果输入进入上升通道且不在下降通道内，状态更新
else return y_0 # 否则，维持原状态
}

sigmod_下降的施密特触发器(x_1,y_0, x_L,x_H,w) {
if x_1>x_H-w && x_1>x_L+w, return y_0/(sigmod(-(x_0-x_H)/w*4))*(sigmod(-(x_1-x_H)/w*4)) #如果输入进入下降通道且不在上升通道内，状态更新 
else if x_1<x_H-w && x_1<x_L+w, return 1-(1-y_0)/(1-sigmod(-(x_0-x_L)/w*4))*(1-sigmod(-(x_1-x_L)/w*4))  #如果输入进入上升通道且不在下降通道内，状态更新
else return y_0 # 否则，维持原状态
}
```

![](<../../.gitbook/assets/975d5638f160e54637ce82334bc30b2b (1).jpg>)

![](<../../.gitbook/assets/a4 (2).png>)

## 3，无监督学习的状态综合——[同架策略](https://guhhhhaa.gitbook.io/joinquant/jin-rong-li-lun-zong-jie/zi-chan-pei-zhi/tong-gen-ce-lve-yu-tong-jia-ce-lve)：

{% embed url="https://guhhhhaa.gitbook.io/joinquant/jin-rong-li-lun-zong-jie/zi-chan-pei-zhi/tong-gen-ce-lve-yu-tong-jia-ce-lve" %}

**注：ABS()** 函数 是 **绝对值()** 函数，\
**MAX()** 函数 是 **比较大小并取其中的大者()** 函数，

IF函数 [**其他函数**](https://zhuanlan.zhihu.com/p/51366759) IFS函数 Choose函数\
[**多条件逻辑函数**](https://zhuanlan.zhihu.com/p/38326242)：AND、OR、IF

```python
定义 x_i
定义 w_i

定义函数 w_i = 同架策略(x_i)
定义函数 w_i = 同根策略(x_i)
------------------------
同架策略(x_i){ 
return x_i*(x_i/(1-x_i))/SUM(x_i/(1-x_i))
}

同根策略(x_i){ 
return x_i*(1/(1-x_i))/SUM(1/(1-x_i))
}
------------------------
同架策略_带做空&杠杆(x_i){ 
return x_i*(ABS(x_i)/MAX(0.0…01,1-ABS(x_i)))/SUM((ABS(x_i)/MAX(0.0…01,1-ABS(x_i))))
}

同根策略_带做空&杠杆(x_i){ 
return x_i*(1/MAX(0.0…01,1-ABS(x_i)))/SUM((1/MAX(0.0…01,1-ABS(x_i))))
}
```

![](<../../.gitbook/assets/image (11).png>)

## 4，总结应用（已失效，用[卓尔金历法](https://www.bfm-unity.com/qian-xian/management-cockpit-operation/zi-chan-pei-zhi/ling-hang-duo-lei-da)代替）

```python
MVRV            ➡️ 归一化操作 ➡️ 施密特触发器 ↘️
                                        同架策略 ➡️ 仓位结果
S2F预测价格/价格0 ➡️ 归一化操作 ➡️ 施密特触发器 ↗️
```
