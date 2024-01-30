# 区块链算法

## 区块链算法

* 共识（共识机制）
* 加密（加密算法）
* 传输（点对点传输）
* 数据（分布式数据存储）

## 共识

比特币区块链采用了 （Proof of Work，PoW）机制来实现共识，该机制最早于 1998 年在 [B-money](http://www.weidai.com/bmoney.txt) 设计中提出。

权益证明（Proof of Stake，PoS）最早在 2013 年被提出，最早在 [Peercoin](broken-reference) 系统中被实现，类似于现实生活中的股东机制，拥有股份越多的人越容易获取记账权（同时越倾向于维护网络的正常工作）。

目前，Proof of X 系列中比较出名的一致性协议包括 PoW、PoS 等，都是通过经济惩罚来限制恶意参与。

### **公链常用算法**

**PoW**：Proof of Work，用于比特币BTC，狗狗币DOGE

**PoS**：Proof of Stake，用于以太坊ETH

### 其他垃圾联盟链和私有链算法

**Proof of X** 系列：

* **DPoS**：Delegated Proof of Stake，委任权益证明，常用于**联盟链**，曾用于EOS柚子币，目前已被证伪。
* **PoA**：Proof of Activity，活跃证明，常用于**私有链**，一种基于声誉reputation 的共识算法_，_一种 PoW 与PoS 混合的共识算法，目前已被证伪。
* **PoSA：顾名思义，PoS+PoA，双链，更垃圾，**常用于**私有链**，目前已被证伪。
* **PoI**：Proof of Importantce，重要性证明，一种评分系统，常用于**私有链**，曾用于 NEM 新经币，目前已被证伪。
* **PoP**：Proof of Peers 或 Proof of Participation，号称将 PoI 和 DPoS 的思想结合，既能确保对设备的公平性，又拥有社区的共识，参考了 **PBFT 和 RPCA，**常用于**私有链**，目前已被证伪。

**BFT** : Byzantine Fault Tolerance，拜占庭容错，常用于**联盟链**，目前已被证伪。

* **PBFT**：Practical Byzantine Fault Tolerance，实⽤拜占庭容错，常用于**联盟链**，目前已被证伪。
  * **RBFT**：Redundant Byzantine fault tolerance，冗余拜占庭容错，常用于**联盟链**，目前已被证伪。
* **DBFT**：Delegated Byzantine Fault Tolerance，委托或授权拜占庭容错，常用于**联盟链**，曾用于NEO小蚁币，目前已被证伪。
* **HBFT**：Hierarchical Byzantine Fault Tolerance，分层拜占庭容错，常用于**联盟链**，性能优于POA，所以更垃圾，常用于**私有链**，目前已被证伪。
* **RAFT**：Replicated And Fault Tolerant，常用于**联盟链**，目前已被证伪。
* **Zyzzyva**：包括HBFT，EZBFT，FAB，常用于**联盟链**，目前已被证伪。
* **PEABFT**：综合了现有三种算法的优点：PnyxDB、EZBFT 和Abstract，常用于**联盟链，能源互联网**，目前已被证伪。

**其他**

* **RPCA**：瑞波共识，常用于**联盟链**，目前已被证伪。
* **Paxos**：早期被淘汰算法，目前已被证伪
* **DAG**：Direct Acyclic Graph，有向无环图，谣言传播算法，其核心机制在于异步通讯。常用于联盟链和IOT链，曾用于IOTA，AVAX，CFX，目前已被证伪。

## 加密

* 对称加密算法&#x20;
  * 分组加密算法
    * AES（最常用）
      * DES（已破解）
        * DESede（三重DES，计算密钥时间太长、加密效率不高，所以也基本上不用。）
      * Blowfish
      * CAST
      * IDEA（常用，电子邮件加密）
      * RC2
      * RC5
  * 流加密
    * RC4
  * 口令加密（融合）
    * PBE
* 非对称加密，AC，Asymmetric cryptography，或，公开密钥加密，PKC，public key cryptography
  * 整数分解
    * [Benaloh](https://zh.wikipedia.org/w/index.php?title=Benaloh\_cryptosystem\&action=edit\&redlink=1)
      * [Blum–Goldwasser](https://zh.wikipedia.org/w/index.php?title=Blum%E2%80%93Goldwasser\_cryptosystem\&action=edit\&redlink=1)
      * [Cayley–Purser](https://zh.wikipedia.org/w/index.php?title=Cayley%E2%80%93Purser\_algorithm\&action=edit\&redlink=1)
      * [Damgård–Jurik](https://zh.wikipedia.org/w/index.php?title=Damg%C3%A5rd%E2%80%93Jurik\_cryptosystem\&action=edit\&redlink=1)
      * [GMR](https://zh.wikipedia.org/w/index.php?title=GMR\_\(cryptography\)\&action=edit\&redlink=1)
      * [Goldwasser–Micali](https://zh.wikipedia.org/w/index.php?title=Goldwasser%E2%80%93Micali\_cryptosystem\&action=edit\&redlink=1)
      * [Paillier](https://zh.wikipedia.org/w/index.php?title=Paillier\_cryptosystem\&action=edit\&redlink=1)
      * [Rabin](https://zh.wikipedia.org/w/index.php?title=Rabin\_cryptosystem\&action=edit\&redlink=1)
      * [RSA](https://zh.wikipedia.org/wiki/RSA%E5%8A%A0%E5%AF%86%E6%BC%94%E7%AE%97%E6%B3%95)，Rivest–Shamir–Adleman_，_用于：密钥交换，数字签名，数据加密（缓慢）。
      * [Okamoto–Uchiyama](https://zh.wikipedia.org/w/index.php?title=Okamoto%E2%80%93Uchiyama\_cryptosystem\&action=edit\&redlink=1)
      * [Schmidt–Samoa](https://zh.wikipedia.org/w/index.php?title=Schmidt%E2%80%93Samoa\_cryptosystem\&action=edit\&redlink=1)
  * [离散对数](https://zh.wikipedia.org/wiki/%E7%A6%BB%E6%95%A3%E5%AF%B9%E6%95%B0)
    * [Cramer–Shoup](https://zh.wikipedia.org/w/index.php?title=Cramer%E2%80%93Shoup\_cryptosystem\&action=edit\&redlink=1)
      * [DH](https://zh.wikipedia.org/wiki/%E8%BF%AA%E8%8F%B2-%E8%B5%AB%E7%88%BE%E6%9B%BC%E5%AF%86%E9%91%B0%E4%BA%A4%E6%8F%9B)，Diffie-Hellman，用于：密钥交换
      * [DSA](https://zh.wikipedia.org/wiki/%E6%95%B0%E5%AD%97%E7%AD%BE%E5%90%8D%E7%AE%97%E6%B3%95)，Digital Signature Algorithm，只用于：数字签名
      * 🔥ECC，Elliptic Curve Cryptography
        * 🔥[ECDH](https://zh.wikipedia.org/wiki/%E6%A9%A2%E5%9C%93%E6%9B%B2%E7%B7%9A%E8%BF%AA%E8%8F%B2-%E8%B5%AB%E7%88%BE%E6%9B%BC%E9%87%91%E9%91%B0%E4%BA%A4%E6%8F%9B)，Elliptic-curve Diffie–Hellman
        * 🔥[ECDSA](https://zh.wikipedia.org/wiki/%E6%A4%AD%E5%9C%86%E6%9B%B2%E7%BA%BF%E6%95%B0%E5%AD%97%E7%AD%BE%E5%90%8D%E7%AE%97%E6%B3%95)，Elliptic Curve Digital Signature Algorithm
      * [EdDSA](https://zh.wikipedia.org/w/index.php?title=EdDSA\&action=edit\&redlink=1)
      * [EKE](https://zh.wikipedia.org/w/index.php?title=%E5%8A%A0%E5%AF%86%E5%AF%86%E9%91%B0%E4%BA%A4%E6%8F%9B\&action=edit\&redlink=1)
      * [ElGamal](https://zh.wikipedia.org/wiki/ElGamal%E5%8A%A0%E5%AF%86%E7%AE%97%E6%B3%95)&#x20;
        * [signature scheme](https://zh.wikipedia.org/wiki/ElGamal%E6%95%B0%E5%AD%97%E7%AD%BE%E5%90%8D%E6%96%B9%E6%A1%88)
      * [MQV](https://zh.wikipedia.org/w/index.php?title=MQV\&action=edit\&redlink=1)
      * [Schnorr](https://zh.wikipedia.org/w/index.php?title=Schnorr%E7%B0%BD%E5%90%8D\&action=edit\&redlink=1)
      * [SPEKE](https://zh.wikipedia.org/w/index.php?title=SPEKE\_\(cryptography\)\&action=edit\&redlink=1)
      * [SRP](https://zh.wikipedia.org/w/index.php?title=Secure\_Remote\_Password\_protocol\&action=edit\&redlink=1)
      * [STS](https://zh.wikipedia.org/w/index.php?title=Station-to-Station\_protocol\&action=edit\&redlink=1)
      * [SM2](https://zh.wikipedia.org/wiki/SM2)
  * 其他
    * [AE](https://zh.wikipedia.org/w/index.php?title=Algebraic\_Eraser\&action=edit\&redlink=1)
      * [CEILIDH](https://zh.wikipedia.org/w/index.php?title=CEILIDH\&action=edit\&redlink=1)
      * [EPOC](https://zh.wikipedia.org/w/index.php?title=Efficient\_Probabilistic\_Public-Key\_Encryption\_Scheme\&action=edit\&redlink=1)
      * [HFE](https://zh.wikipedia.org/w/index.php?title=Hidden\_Field\_Equations\&action=edit\&redlink=1)
      * [IES](https://zh.wikipedia.org/w/index.php?title=Integrated\_Encryption\_Scheme\&action=edit\&redlink=1)
      * [Lamport](https://zh.wikipedia.org/w/index.php?title=Lamport\_signature\&action=edit\&redlink=1)
      * [McEliece](https://zh.wikipedia.org/w/index.php?title=McEliece\_cryptosystem\&action=edit\&redlink=1)
      * [Merkle–Hellman](https://zh.wikipedia.org/w/index.php?title=Merkle%E2%80%93Hellman\_knapsack\_cryptosystem\&action=edit\&redlink=1)
      * [Naccache–Stern](https://zh.wikipedia.org/w/index.php?title=Naccache%E2%80%93Stern\_cryptosystem\&action=edit\&redlink=1)
      * [Naccache–Stern knapsack cryptosystem](https://zh.wikipedia.org/w/index.php?title=Naccache%E2%80%93Stern\_knapsack\_cryptosystem\&action=edit\&redlink=1)
      * [NTRU](https://zh.wikipedia.org/wiki/NTRU)
      * [NTRUEncrypt](https://zh.wikipedia.org/w/index.php?title=NTRUEncrypt\&action=edit\&redlink=1)
      * [NTRUSign](https://zh.wikipedia.org/w/index.php?title=NTRUSign\&action=edit\&redlink=1)
      * [Three-pass protocol](https://zh.wikipedia.org/w/index.php?title=Three-pass\_protocol\&action=edit\&redlink=1)
      * [XTR](https://zh.wikipedia.org/w/index.php?title=XTR\&action=edit\&redlink=1)
* 摘要
  * #### MD5 <a href="#41md5-suan-fa" id="41md5-suan-fa"></a>
  * #### SHA1 <a href="#42sha1-suan-fa" id="42sha1-suan-fa"></a>
  *

加密算法安全性：DES\<DES3=AES\<RSA\<ECC,

至于MD5、SHA、HMAC不好说了（不好说了，是啥意思？是太垃圾吗？）

RSA是非对称密码算法。非对称密码算法很少用于加密，一般用于对身份进行识别和认证，即使用于加密，也是用于对会话密钥进行加密而很少对文件或信息直接加密。

MD5和SHA1可以说是目前应用最广泛的Hash算法，而它们都是以MD4为基础设计的。 Md5和SHA系列是哈希函数。哈希函数不用于对文件或信息加密的，而是用于对传输信息进行完整性校验。

对称加密（加密解密密钥相同）：DES、DES3、AES

非对称加密（分公钥私钥）：RSA 信息摘要算法/签名算法：MD5、HMAC、SHA

前端实际使用中MD5、AES、RSA使用频率是最高的

几种加密方式配合次序：采用非对称加密算法管理对称算法的密钥，然后用对称加密算法加密数据，用签名算法生成非对称加密的摘要

DES、DES3、AES、RSA、MD5、SHA、HMAC传入的消息或者密钥都是bytes数据类型，不是bytes数据类型的需要先转换；密钥一般是8的倍数

Python实现RSA中，在rsa库中带有生成签名和校对签名的方法

\
