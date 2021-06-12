# 卓尔金历法的升级1——拟合函数

## 智能神经网络查找表

```python
=$E$4 + ($AI$4-$E$4) * 1/(1+EXP(-($D$4*(F3-$C$2))))
 
=$D$5 - ($D$5-$D$35) * 1/(1+EXP(-($D$4*(-C6+$B$3))))

=(E$4+$D5)/2

=MAX((F$4+$D5)/2,E4)

=MIN((E$4+$D6)/2,D5)

=IFS(
    ($C6-$B$3)<-(F$3-$C$2), MIN((F$4+$D6)/2,E5),
    ($C6-$B$3)>-(F$3-$C$2), MAX((F$4+$D6)/2,E5),
    TRUE, (F$4+$D6)/2
)
```

```c
激活函数

sigmoid(x) = 1/(1 + exp(−x))

tanh(x) = (exp(x) - exp(−x))/(exp(x) + exp(−x))
tanh(x) = (1 - exp(−2 * x))/(1 + exp(−2 * x))

tanh(x) = 2 * sigmoid(2 * x) - 1
tanh(x / 2) = 2 * sigmoid(x) - 1 

ReLU(x) = MAX(x,0)

Swish(x) = x * sigmoid(x)
```

