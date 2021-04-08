# Python Project

## [Pandas](https://pypi.org/project/pandas/) - 数据分析

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

data = pd.read_csv('/path', encoding='gbk') # 导入为data
print data # 打印data
```

## [Openpyxl](https://pypi.org/project/openpyxl/) - 处理EXCEL

