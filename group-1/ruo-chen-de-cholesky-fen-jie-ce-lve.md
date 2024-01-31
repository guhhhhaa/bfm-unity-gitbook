# 若尘的cholesky分解策略

## 若尘的cholesky分解策略

对了，晚上的时候我解出了最佳资产配比的方法对于可用的n种资产，平均收益率向量为b，对数协方差矩阵为A，

那么对A作cholesky分解得到A=R'R，最优资产配置就是(R^{-1})'b（的归一化）

注意要添加一种资产叫做银行存款，它和任何资产包括它自己的协方差都是零这样就把所有仓位都统一了

而且既用到了凯利公式的核心就是对数效用函数，又用到了夏普率，我会的工具能做到的就这么多了

这比你那个什么同架策略简洁可靠得多越看越觉得巧妙

一个cholesky分解就解决了问题

顺便因为非正定矩阵是没法分解的，所以用模拟的广发钱袋子代替银行存款，引入一个微小的正态扰动，规避掉奇异矩阵的问题​[https://github.com/sffred/fundFuser/blob/main/README.md](https://github.com/sffred/fundFuser/blob/main/README.md)
