# Python Project

## 调试

```python
exit() # 执行到此处中止
```

## [Numpy](https://pypi.org/project/numpy/) - 矩阵计算

### 安装

{% embed url="https://numpy.org/install/" %}

```python
import numpy as np

array = np.array([[1,2,3],
                  [2,3,4]])

print(array)
print('number of dim:', array.ndim) # 输出矩阵的维数
print('shape:', array.shape) # 输出矩阵的行列数
print('size:', array.size) # 输出矩阵的元素数
```

## [Pandas](https://pypi.org/project/pandas/) - 数据分析

### 安装

{% embed url="https://pandas.pydata.org/pandas-docs/stable/getting\_started/install.html" %}

### 读取数据

```python
import pandas as pd

pd.read_csv('/path') #读取csv文件
pd.read_excel('/path') #读取excel表格
pd.read_table('/path') #读取txt文本
```

```python
import pandas as pd

pd.read_csv('/path', encoding='gbk')
# encoding='gbk' : 防止出现中文乱码
```

```python
import pandas as pd

DataName_data = pd.read_csv('/path', encoding='gbk') # 导入为DataName_data

print DataName_data # 打印DataName_data
```

```python
import pandas as pd

DataName_data = pd.read_csv('/path', encoding='gbk') # 导入为DataName_data

print DataName_data[['列名1']] # 打印DataName_data的某一列
print DataName_data[['列名1', '列名2']] # 打印DataName_data的某两列
```

```python
import pandas as pd

DataName_data = pd.read_csv('/path', encoding='gbk') # 导入为DataName_data

DataName_data[['新增列名1']] = '新增列值1' # 新增一列
print DataName_data # 打印DataName_data
```

### 排序数据

```python
import pandas as pd

DataName_data = pd.read_csv('/path', encoding='gbk') # 导入为DataName_data

DataName_data.sort_values(by = ['列名1', '列名2'], inplace = True) 
# 先按列名1排序，再按列名2排序
print DataName_data # 打印DataName_data
```

### 截取数据

```python
import pandas as pd

DataName_data = pd.read_csv('/path', encoding='gbk') # 导入为DataName_data

DataName_data = DataName_data['交易日期'] > pd.to_datetime(20201231)

print DataName_data # 打印DataName_data
```

## [Openpyxl](https://pypi.org/project/openpyxl/) - 处理EXCEL

