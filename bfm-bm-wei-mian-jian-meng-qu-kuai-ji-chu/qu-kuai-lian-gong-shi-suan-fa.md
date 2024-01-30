# 区块链共识算法

[区块链算法](https://www.zhihu.com/search?q=%E5%8C%BA%E5%9D%97%E9%93%BE%E7%AE%97%E6%B3%95\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2984827039%7D)

\
共识（共识机制）\
加密（[加密算法](https://www.zhihu.com/search?q=%E5%8A%A0%E5%AF%86%E7%AE%97%E6%B3%95\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2984827039%7D)）\
传输（点对点传输）\
数据（分布式数据存储）

共识

[比特币区块链](https://www.zhihu.com/search?q=%E6%AF%94%E7%89%B9%E5%B8%81%E5%8C%BA%E5%9D%97%E9%93%BE\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2984827039%7D)采用了 Proof of Work（PoW）机制来实现共识，该机制最早于 1998 年在 [B-money](https://link.zhihu.com/?target=http%3A//www.weidai.com/bmoney.txt) 设计中提出。

[权益证明](https://www.zhihu.com/search?q=%E6%9D%83%E7%9B%8A%E8%AF%81%E6%98%8E\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2984827039%7D)（Proof of Stake，PoS）最早在 2013 年被提出，最早在 [Peercoin](https://zhuanlan.zhihu.com/p/622128049/edit) 系统中被实现，类似于现实生活中的[股东机制](https://www.zhihu.com/search?q=%E8%82%A1%E4%B8%9C%E6%9C%BA%E5%88%B6\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2984827039%7D)，拥有股份越多的人越容易获取[记账权](https://www.zhihu.com/search?q=%E8%AE%B0%E8%B4%A6%E6%9D%83\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2984827039%7D)（同时越倾向于维护网络的正常工作）。

目前，Proof of X 系列中比较出名的一致性协议包括 PoW、PoS 等，都是通过经济惩罚来限制恶意参与。

[公链](https://www.zhihu.com/search?q=%E5%85%AC%E9%93%BE\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2984827039%7D)常用算法

PoW：Proof of Work，用于比特币BTC，狗狗币DOGE

PoS：Proof of Stake，用于[以太坊](https://www.zhihu.com/search?q=%E4%BB%A5%E5%A4%AA%E5%9D%8A\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2984827039%7D)ETH

其他垃圾联盟链和[私有链](https://www.zhihu.com/search?q=%E7%A7%81%E6%9C%89%E9%93%BE\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2984827039%7D)算法

DPoS：Delegated Proof of Stake，委任权益证明，常用于联盟链，曾用于EOS柚子币，目前已被证伪。\
PoA：Proof of Activity，活跃证明，常用于私有链，一种基于声誉reputation 的[共识算法](https://www.zhihu.com/search?q=%E5%85%B1%E8%AF%86%E7%AE%97%E6%B3%95\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2984827039%7D)_，_一种 PoW 与PoS 混合的共识算法，目前已被证伪。\
PoSA：顾名思义，PoS+PoA，双链，更垃圾，常用于私有链，目前已被证伪。\
PoI：Proof of Importantce，重要性证明，一种评分系统，常用于私有链，曾用于 NEM [新经币](https://www.zhihu.com/search?q=%E6%96%B0%E7%BB%8F%E5%B8%81\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2984827039%7D)，目前已被证伪。\
PoP：Proof of Peers 或 Proof of Participation，号称将 PoI 和 DPoS 的思想结合，既能确保对设备的公平性，又拥有社区的共识，参考了 PBFT 和 RPCA，常用于私有链，目前已被证伪。

BFT : Byzantine Fault Tolerance，[拜占庭](https://www.zhihu.com/search?q=%E6%8B%9C%E5%8D%A0%E5%BA%AD\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2984827039%7D)容错，常用于[联盟链](https://www.zhihu.com/search?q=%E8%81%94%E7%9B%9F%E9%93%BE\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2984827039%7D)，目前已被证伪。\
PBFT：Practical Byzantine Fault Tolerance，实⽤拜占庭容错，常用于联盟链，目前已被证伪。\
RBFT：Redundant Byzantine fault tolerance，冗余拜占庭容错，常用于联盟链，目前已被证伪。\
DBFT：Delegated Byzantine Fault Tolerance，委托或授权拜占庭容错，常用于联盟链，曾用于NEO小蚁币，目前已被证伪。\
HBFT：Hierarchical Byzantine Fault Tolerance，分层拜占庭容错，常用于联盟链，性能优于POA，所以更垃圾，常用于私有链，目前已被证伪。\
RAFT：Replicated And Fault Tolerant，常用于联盟链，目前已被证伪。\
Zyzzyva：包括HBFT，EZBFT，FAB，常用于联盟链，目前已被证伪。\
PEABFT：综合了现有三种算法的优点：PnyxDB、EZBFT 和Abstract，常用于联盟链，能源互联网，目前已被证伪。

RPCA：[瑞波共识](https://www.zhihu.com/search?q=%E7%91%9E%E6%B3%A2%E5%85%B1%E8%AF%86\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2984827039%7D)，常用于联盟链，目前已被证伪。

Paxos：早期被淘汰算法，目前已被证伪

DAG：Direct Acyclic Graph，[有向无环图](https://www.zhihu.com/search?q=%E6%9C%89%E5%90%91%E6%97%A0%E7%8E%AF%E5%9B%BE\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2984827039%7D)，一种典型的谣言传播算法，其核心机制即在于[异步通讯](https://www.zhihu.com/search?q=%E5%BC%82%E6%AD%A5%E9%80%9A%E8%AE%AF\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2984827039%7D)。常用于联盟链和IOT链，曾用于IOTA，AVAX，CFX，目前已被证伪。

加密

加密算法安全性：DES\<DES3=AES\<RSA\<ECC,

至于MD5、SHA、HMAC不好说了（不好说了，是啥意思？是太垃圾吗？）

RSA是非对称[密码算法](https://www.zhihu.com/search?q=%E5%AF%86%E7%A0%81%E7%AE%97%E6%B3%95\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2984827039%7D)。非对称密码算法很少用于加密，一般用于对身份进行识别和认证，即使用于加密，也是用于对会话密钥进行加密而很少对文件或信息直接加密。

MD5和SHA1可以说是目前应用最广泛的Hash算法，而它们都是以MD4为基础设计的。 Md5和SHA系列是[哈希函数](https://www.zhihu.com/search?q=%E5%93%88%E5%B8%8C%E5%87%BD%E6%95%B0\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2984827039%7D)。哈希函数不用于对文件或信息加密的，而是用于对传输信息进行完整性校验。

[对称加密](https://www.zhihu.com/search?q=%E5%AF%B9%E7%A7%B0%E5%8A%A0%E5%AF%86\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2984827039%7D)（加密解密密钥相同）：DES、DES3、AES

[非对称加密](https://www.zhihu.com/search?q=%E9%9D%9E%E5%AF%B9%E7%A7%B0%E5%8A%A0%E5%AF%86\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2984827039%7D)（分公钥私钥）：RSA 信息摘要算法/[签名算法](https://www.zhihu.com/search?q=%E7%AD%BE%E5%90%8D%E7%AE%97%E6%B3%95\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2984827039%7D)：MD5、HMAC、SHA

前端实际使用中MD5、AES、RSA使用频率是最高的

几种加密方式配合次序：采用[非对称加密算法](https://www.zhihu.com/search?q=%E9%9D%9E%E5%AF%B9%E7%A7%B0%E5%8A%A0%E5%AF%86%E7%AE%97%E6%B3%95\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2984827039%7D)管理对称算法的密钥，然后用对称加密算法加密数据，用签名算法生成非对称加密的摘要

DES、DES3、AES、RSA、MD5、SHA、HMAC传入的消息或者密钥都是bytes数据类型，不是bytes数据类型的需要先转换；密钥一般是8的倍数

Python实现RSA，在rsa库中，带有生成签名和校对签名的方法。
