# 比坊梦全球互联网基金

## 比坊梦全球互联网 - 被动 基金

{% embed url="https://qieman.com/portfolios/ZH116702" %}

## 比坊梦全球互联网 - 主动 基金

{% embed url="https://qieman.com/portfolios/ZH116751" %}

## [同架策略](https://guhhhhaa.gitbook.io/joinquant/jin-rong-li-lun-zong-jie/zi-chan-pei-zhi/tong-gen-ce-lve-yu-tong-jia-ce-lve)

{% embed url="https://guhhhhaa.gitbook.io/joinquant/jin-rong-li-lun-zong-jie/zi-chan-pei-zhi/tong-gen-ce-lve-yu-tong-jia-ce-lve" %}

```c
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

