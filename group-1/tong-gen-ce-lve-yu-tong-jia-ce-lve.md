# 同根策略与同架策略

## 同根策略与同架策略

[若尘的cholesky分解策略](https://www.bfm-unity.com/v/joinquant/jin-rong-li-lun-zong-jie/zi-chan-pei-zhi/ruo-chen-de-ce-lve)

### 表格 <a href="#biao-ge" id="biao-ge"></a>

​[https://share.weiyun.com/xUw40P4l](https://share.weiyun.com/xUw40P4l)​

### 公式 <a href="#gong-shi" id="gong-shi"></a>

![](https://1765781468-files.gitbook.io/\~/files/v0/b/gitbook-legacy-files/o/assets%2F-M6CRaXFMq2pMngzlUK3%2F-MTDLl\_ZWCMKbruD-Zfg%2F-MTDKx8GUGm-lbdIbs5\_%2F%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202021-02-11%20%E4%B8%8A%E5%8D%887.55.50.png?alt=media\&token=acd81e04-8c33-4733-a6d4-522faa91f73c)

### 考虑杠杆和做空的公式推广 <a href="#kao-lv-gang-gan-he-zuo-kong-de-gong-shi-tui-guang" id="kao-lv-gang-gan-he-zuo-kong-de-gong-shi-tui-guang"></a>

![](https://1765781468-files.gitbook.io/\~/files/v0/b/gitbook-legacy-files/o/assets%2F-M6CRaXFMq2pMngzlUK3%2F-MW3a0h6sHufqpPKq33M%2F-MW3aA3wC6VAxV-CavK9%2F%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202021-03-18%20%E4%B8%8B%E5%8D%885.07.54.png?alt=media\&token=70eed2ca-9a09-457a-a87b-8031ba2f7eb9)

### 同根策略 <a href="#tong-gen-ce-lve" id="tong-gen-ce-lve"></a>

![](https://1765781468-files.gitbook.io/\~/files/v0/b/gitbook-legacy-files/o/assets%2F-M6CRaXFMq2pMngzlUK3%2F-MSzWSKuBFAngnhkYTvS%2F-MSzUphJZuS25Cs-Y2NL%2F%E5%90%8C%E6%A0%B9%E7%AD%96%E7%95%A5.png?alt=media\&token=c4ce7815-9f59-4ccf-af29-4d20ec2491f3)同根策略a + b + c = 1a\*(1-x) = b\*(1-y) = c\*(1-z)a\*(1-x)/(1-y) = ba\*(1-x)/(1-z) = ca\*(1-x)/(1-x)+a\*(1-x)/(1-y)+a\*(1-x)/(1-z) = 1b\*(1-y)/(1-x)+b\*(1-y)/(1-y)+b\*(1-y)/(1-z) = 1c\*(1-z)/(1-x)+c\*(1-z)/(1-y)+c\*(1-z)/(1-z) = 1a = 1/(1-x)/(1/(1-x)+1/(1-y)+1/(1-z))b = 1/(1-y)/(1/(1-x)+1/(1-y)+1/(1-z))c = 1/(1-z)/(1/(1-x)+1/(1-y)+1/(1-z))ax = x/(1-x)/(1/(1-x)+1/(1-y)+1/(1-z))by = y/(1-y)/(1/(1-x)+1/(1-y)+1/(1-z))cz = z/(1-z)/(1/(1-x)+1/(1-y)+1/(1-z))ax+by+cz=(x/(1-x)+y/(1-y)+z/(1-z))/(1/(1-x)+1/(1-y)+1/(1-z))​我把这个叫做同根策略灰色的是现金，颜色的是资产。每种资产携带的现金相同。所以叫同根策略x,y,z是单独考虑的资产占比a,b,c是分配权重，ax,by,cz是分配后的资产仓位占比

### 同架策略 <a href="#tong-jia-ce-lve" id="tong-jia-ce-lve"></a>

![](https://1765781468-files.gitbook.io/\~/files/v0/b/gitbook-legacy-files/o/assets%2F-M6CRaXFMq2pMngzlUK3%2F-MSzWSKuBFAngnhkYTvS%2F-MSzUTKWHpIW5o3auAAe%2F%E5%90%8C%E6%9E%B6%E7%AD%96%E7%95%A5.png?alt=media\&token=e255193d-ddab-4946-9966-e77475648a04)同架策略a + b + c = 1a/x\*(1-x) = b/y\*(1-y) = c/z\*(1-z)a\*((1-x)/x)/((1-y)/y) = ba\*((1-x)/x)/((1-z)/z) = ca\*((1-x)/x)/((1-x)/x)+a\*((1-x)/x)/((1-y)/y)+a\*((1-x)/x)/((1-z)/z) = 1b\*((1-y)/y)/((1-x)/x)+b\*((1-y)/y)/((1-y)/y)+b\*((1-y)/y)/((1-z)/z) = 1c\*((1-z)/z)/((1-x)/x)+c\*((1-z)/z)/((1-y)/y)+c\*((1-z)/z)/((1-z)/z) = 1a = 1/((1-x)/x)/(1/((1-x)/x)+1/((1-y)/y)+1/((1-z)/z)) = x/(1-x)/(x/(1-x)+y/(1-y)+z/(1-z))b = 1/((1-y)/y)/(1/((1-x)/x)+1/((1-y)/y)+1/((1-z)/z)) = y/(1-y)/(x/(1-x)+y/(1-y)+z/(1-z))c = 1/((1-z)/z)/(1/((1-x)/x)+1/((1-y)/y)+1/((1-z)/z)) = z/(1-z)/(x/(1-x)+y/(1-y)+z/(1-z))ax = x^2/(1-x)/(x/(1-x)+y/(1-y)+z/(1-z))by = y^2/(1-y)/(x/(1-x)+y/(1-y)+z/(1-z))cz = z^2/(1-z)/(x/(1-x)+y/(1-y)+z/(1-z))ax+by+cz = (x^2/(1-x)+y^2/(1-y)+z^2/(1-z))/(x/(1-x)+y/(1-y)+z/(1-z))我把这个叫做同架策略灰色的是现金，颜色的是资产。每种资产携带现金间比例，与资产间比例，相等。所以叫同架策略。x,y,z是单独考虑的资产占比，a,b,c是分配权重，ax,by,cz是分配后的资产仓位占比。

### 策略比较 <a href="#ce-lve-bi-jiao" id="ce-lve-bi-jiao"></a>

![](https://1765781468-files.gitbook.io/\~/files/v0/b/gitbook-legacy-files/o/assets%2F-M6CRaXFMq2pMngzlUK3%2F-MSzWSKuBFAngnhkYTvS%2F-MSzUvgvaRKMjIqWW1m1%2F%E5%90%8C%E6%A0%B9%E5%90%8C%E6%9E%B6%E7%AD%96%E7%95%A5%E6%AF%94%E8%BE%83.png?alt=media\&token=bd9ce50a-b43a-4956-9d23-04ef9c62a5d5)同根同架策略比较

### 实际应用（同架策略） <a href="#shi-ji-ying-yong-tong-jia-ce-lve" id="shi-ji-ying-yong-tong-jia-ce-lve"></a>

![](https://1765781468-files.gitbook.io/\~/files/v0/b/gitbook-legacy-files/o/assets%2F-M6CRaXFMq2pMngzlUK3%2F-MSzv29SFQxgTIyUSvgf%2F-MSzvHJxhiJS5reItvYk%2F%E5%AE%9E%E9%99%85%E5%BA%94%E7%94%A8.png?alt=media\&token=3cfcdce5-c6b0-4323-ad42-20a82f39873f)实际应用
