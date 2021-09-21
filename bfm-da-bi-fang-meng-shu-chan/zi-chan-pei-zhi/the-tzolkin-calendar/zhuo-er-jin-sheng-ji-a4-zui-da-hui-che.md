# 卓尔金升级A4——最大回撤

参考：[https://jingyan.baidu.com/article/636f38bb3d678797b8461093.html](https://jingyan.baidu.com/article/636f38bb3d678797b8461093.html)

```python
#正数最大回撤
=IF(MAX($A$1:A2)-A2<B1,B1,MAX($A$1:A2)-A2)

#负数最大回撤
=IF(A2-MAX($A$1:A2)>B1,B1,A2-MAX($A$1:A2))

#正数最大回撤比例
=IF((MAX($A$1:A2)-A2)/MAX($A$1:A2)<B1,B1,(MAX($A$1:A2)-A2)/MAX($A$1:A2))

#负数最大回撤比例
=IF(A2-(MAX($A$1:A2))/MAX($A$1:A2)>B1,B1,(A2-MAX($A$1:A2))/MAX($A$1:A2))
```

