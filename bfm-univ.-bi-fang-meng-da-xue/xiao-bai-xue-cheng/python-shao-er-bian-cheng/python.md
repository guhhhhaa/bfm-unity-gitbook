# Python Project

## 调试

```python
exit() # 执行到此处中止
```

## [Numpy](https://pypi.org/project/numpy/) - 矩阵计算

### 安装

{% embed url="https://numpy.org/install/" %}

### 使用

```python
import numpy as np

array = np.array([[1,2,3],
                  [2,3,4]])

print(array)
print('number of dim:', array.ndim) # 输出矩阵的维数
print('shape:', array.shape) # 输出矩阵的行列数
print('size:', array.size) # 输出矩阵的元素数
```

```python
import numpy as np

a = np.array([10,20,30,40])
b = np.arange(4)

print(a,b)

# 输出结果:
# [10 20 30 40] [0 1 2 3]
```

```python
import numpy as np

a = np.array([10,20,30,40])
b = np.arange(4)

print(a,b)

c = a+b
print(c)

# 输出结果:
# [10 20 30 40] [0 1 2 3]
# [10 21 32 43]
```

```python
import numpy as np

a = np.array([10,20,30,40])
b = np.arange(4)

print(a,b)

c = a-b
print(c)

# 输出结果:
# [10 20 30 40] [0 1 2 3]
# [10 19 28 37]
```

```python
import numpy as np

a = np.array([10,20,30,40])
b = np.arange(4)

c = b**2
print(c)

# 输出结果:
# [0 1 4 9]
```

```python
import numpy as np

a = np.array([10,20,30,40])
b = np.arange(4)

c = 10*np.sin(a)
print(c)

# 输出结果:
# [-5.44021111 9.12945251 -9.88031624 7.4511316]
```

```python
import numpy as np

a = np.array([10,20,30,40])
b = np.arange(4)

print(b)
print(b<3)

# 输出结果:
# [0 1 2 3]
# [True True True False]
```

```python
import numpy as np

a = np.array([10,20,30,40])
b = np.arange(4)

print(b)
print(b==3)

# 输出结果:
# [0 1 2 3]
# [False False False True]
```

```python
import numpy as np

a = np.array([10,20,30,40])
b = np.arange(4)

print(b)
print(b==3)

# 输出结果:
# [0 1 2 3]
# [False False False True]
```

```python
import numpy as np

a = np.array([[1,1],
              [0,1]])
b = np.arange(4).reshape((2,2))

print(a)
print(b)

c = a*b
c_dot = np.dot(a,b)

print(c)
print(c_dot)

# 输出结果:
# [[1 1]
#  [0 1]]
# [[0 1]
#  [2 3]]

# [[0 1]
#  [0 3]]
# [[2 4]
#  [2 3]]
```

{% embed url="https://blog.csdn.net/like4501/article/details/79753346" %}

## [Pandas](https://pypi.org/project/pandas/) - 数据分析

### 安装

{% embed url="https://pandas.pydata.org/pandas-docs/stable/getting\_started/install.html" %}

### 使用 - 读取数据

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

### 使用 - 排序数据

```python
import pandas as pd

DataName_data = pd.read_csv('/path', encoding='gbk') # 导入为DataName_data

DataName_data.sort_values(by = ['列名1', '列名2'], inplace = True) 
# 先按列名1排序，再按列名2排序
print DataName_data # 打印DataName_data
```

### 使用 - 截取数据

```python
import pandas as pd

DataName_data = pd.read_csv('/path', encoding='gbk') # 导入为DataName_data

DataName_data = DataName_data['交易日期'] > pd.to_datetime(20201231)

print DataName_data # 打印DataName_data
```

## [Openpyxl](https://pypi.org/project/openpyxl/) - 处理EXCEL

