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
PoA：Proof of Activity，活跃证明，常用于私有链，一种基于声誉reputation 的[共识算法](https://www.zhihu.com/search?q=%E5%85%B1%E8%AF%86%E7%AE%97%E6%B3%95\&search\_source=Entity\&hybrid\_search\_source=Entity\&hybrid\_search\_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A2984827039%7D)\_，\_一种 PoW 与PoS 混合的共识算法，目前已被证伪。\
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

### 1，摘要 <a href="#d02iu" id="d02iu"></a>

本文尽可能列出所有主要的共识算法，评估各自的优劣之处。共识算法是区块链的核心技术，本文会跟随作者的理解，持续更新。如果读者发现有所遗漏，或是存在错误，希望能通过评论指出。

### 2，区块链共识算法 <a href="#id-90a1q" id="id-90a1q"></a>

#### 2.1 工作量证明（PoW，Proof of Work） <a href="#id-6bgj" id="id-6bgj"></a>

**优点：** 自2009年以来得到了广泛测试，目前依然得到广泛的使用。 \*\*不足：\*\*速度慢。耗能巨大，对环境不好。易受“规模经济”（economies of scale）的影响。 **使用者：** Bitcoin、Ethereum、LiteCoin、Dogecoin等。 \*\*类型：\*\*有竞争共识(Competive consensus）。 \*\*解释：\*\*PoW是是首个共识算法。它是由中本聪在他的论文中提出的，用于建立分布式无信任共识并识别“双重支付”（double spend）问题。PoW并非一个新理念，但是中本聪将Pow与加密签名、Merkle链和P2P网络等已有理念结合，形成一种可用的分布式共识系统。加密货币是这样系统的首个基础和应用，因而独具创新性。 在PoW的工作方式中，区块链参与者（称为“矿工”）要在区块链中添加一块交易，必须解决某种“复杂但是无用”的计算问题。 只要由矿工提交的工作有超过一半是值得信任的，那么Bitcoin就是安全的。 从某种角度来看，PoW有点像买彩票，只是概率高一点而已。 **技术原理：** 工作量证明最核心的技术原理是散列函数（哈希）。在比特币中，PoW工作其实就是如何去计算一个区块的目标哈希值问题，让用户进行大量的穷举运算，同时得出这个哈希值还必须满足一些必要条件，这个条件在区块链中其实就是一个难度系数值，通过计算出的哈希值是否符合前面N位全是0，最终达成工作量证明。 举个例子： 比如现在给出一个固定的字符串“Hello, blockchain”，现在要求计算的难题是将这个字符串与一个随机数（Nonce）拼接起来，并通过SHA256哈希计算一个固定256位长度的哈希值，如果计算结果得到的前5位全是0，即认为满足计算条件，同时得到的随机数（Nonce）值证明为达成工作量证明的有效随机数。

#### 2.2 权益证明（PoS，Proof of Stake） <a href="#vrkv" id="vrkv"></a>

\*\*优点：\*\*节能、攻击者代价更大、不易受“规模经济”的影响。 **不足：**“无利害关系“（Nothing at stake）”攻击问题。 \*\*使用者：\*\*Ethereum（即将推出）、Peercoin、Nxt。 **类型：有竞争共识。 解释： 类似于财产储存在银行，这种模式会根据你持有数字货币的量和时间，分配给你相应的利息。 简单来说，就是一个根据你持有货币的量和时间，给你发利息的一个制度，在股权证明POS模式下，有一个名词叫币龄**，每个币每天产生1币龄，比如你持有100个币，总共持有了30天，那么，此时你的币龄就为3000，这个时候，如果你发现了一个POS区块，你的币龄就会被清空为0。你每被清空365币龄，你将会从区块中获得0.05个币的利息(假定利息可理解为年利率5%)，那么在这个案例中，利息 = 3000 \* 5% / 365 = 0.41个币，这下就很有意思了，持币有利息。以太坊就是采用POS共识算法。 从某种角度来看，PoS有点像银行存款，你持有的时间越长，本金越大，你得到的利息会越多。 **技术原理：** 每个旷工都有出块(即挖矿)的权力，只要出块成功，就有系统给出的奖励，这里不需要通过复杂的计算来挖矿，问题只在于谁来出块，股权越大，出块的概率就越大，反之，则相反。POS有很多变种，股权可以是持有币的数量，或者支付的数量等等。

go的demo代码实现:

```javascript
package main

import (
    "time"
    "strconv"
    "crypto/sha256"
    "math/rand"
    "fmt"
    "encoding/hex"
)

//实现pos挖矿的原理

type Block struct {
    Index int
    Data string //
    PreHash string
    Hash string
    Timestamp string
    //记录挖矿节点
    Validator *Node

}

func genesisBlock() Block  {

    var genesBlock  = Block{0, "Genesis block","","",time.Now().String(),&Node{0, 0, "dd"}}
    genesBlock.Hash = hex.EncodeToString(BlockHash(&genesBlock))
    return genesBlock
}

func BlockHash(block *Block) []byte  {
    record := strconv.Itoa(block.Index) + block.Data + block.PreHash + block.Timestamp + block.Validator.Address
    h := sha256.New()
    h.Write([]byte(record))
    hashed := h.Sum(nil)

    return hashed
}

//创建全节点类型
type Node struct {
    Tokens int //持币数量
    Days int //持币时间
    Address string //地址
}


//创建5个节点
//算法的实现要满足 持币越多的节点越容易出块
var nodes = make([]Node, 5)
//存放节点的地址
var addr = make([]*Node, 15)


func InitNodes()  {

    nodes[0] = Node{1, 1, "0x12341"}
    nodes[1] = Node{2, 1, "0x12342"}
    nodes[2] = Node{3, 1, "0x12343"}
    nodes[3] = Node{4, 1, "0x12344"}
    nodes[4] = Node{5, 1, "0x12345"}

    cnt :=0
    for i:=0;i<5;i++ {
        for j:=0;j<nodes[i].Tokens * nodes[i].Days;j++{
            addr[cnt] = &nodes[i]
            cnt++
        }
    }

}

//采用Pos共识算法进行挖矿
func CreateNewBlock(lastBlock *Block, data string) Block{

    var newBlock Block
    newBlock.Index = lastBlock.Index + 1
    newBlock.Timestamp = time.Now().String()
    newBlock.PreHash = lastBlock.Hash
    newBlock.Data = data


    //通过pos计算由那个村民挖矿
    //设置随机种子
    rand.Seed(time.Now().Unix())
    //[0,15)产生0-15的随机值
    var rd =rand.Intn(15)

    //选出挖矿的旷工
    node := addr[rd]
    //设置当前区块挖矿地址为旷工
    newBlock.Validator = node
    //简单模拟 挖矿所得奖励
    node.Tokens += 1
    newBlock.Hash = hex.EncodeToString(BlockHash(&newBlock))
    return newBlock
}

func main()  {

    InitNodes()

    //创建创世区块
    var genesisBlock = genesisBlock()

    //创建新区快
    var newBlock = CreateNewBlock(&genesisBlock, "new block")

    //打印新区快信息
    fmt.Println(newBlock)
    fmt.Println(newBlock.Validator.Address)
    fmt.Println(newBlock.Validator.Tokens)

}
```

复制

输出结果：

```javascript
{1 new block 72e8838ad3bb761c7d3ba42c4e6bad86409dd3f4ce958c890409c4b9ddf44171 e4f9575cfb14ee146810862c9e5cc78ebff185f5888f428dbb945bd9060b31f7 2018-06-29 19:29:04.827332898 +0800 CST m=+0.000837770 0xc42007e0a0}
0x12341
2
```

复制

#### 2.3 委任权益证明（DPOS，Delegated Proof-of-Stake） <a href="#id-48tn0" id="id-48tn0"></a>

**优点：** 节能、快速、高流量博客网站Steemit就使用了它。EOS 的块时间是 0.5 秒。 **不足：** 略为中心化、拥有高权益的参与者可投票使自己成为一名验证者。这是近期已在 EOS 中出现的问题。 \*\*采用者：\*\*BitShares、Steemit、EOS、Lisk、Ark。 \*\*类型：\*\*协同型共识 **解释**：在 DPoS 系统中，权益持有者可以选举领导者（或称为见证人，Witness）。经权益持有者授权，这些领导者可进行投票。该机制使得 DPoS 要快于正常的 PoS。 例如，EOS 中选举出 21 位见证人，并且有一堆节点（潜在的见证人）作为候选者。一旦见证人节点死亡或是做出了恶意行为，新节点就会立刻替代见证人节点。见证人会因为生成区块而获得一笔支付费用。该费用是由权益持有者设立的 。 通常，所有节点采用轮询方式，一次生成一个区块。该机制防止一个节点发布连续的块，进而执行“双重支付”攻击。如果一个见证人在分配给他的时间槽中未生成区块，那么该时间槽就被跳过，并由下一位见证人生成下一个区块。如果见证人持续丢失他的区块，或是发布了错误的交易，那么权益持有者将投票决定其退出，用更好的见证人替换他。 在 DPoS 中，矿工可以合作生成块，而不是像在 PoW 和 PoS 中那样竞争生成。通过区块生成的部分中心化，DPoS 的运行可以比其它共识算法呈数量级快。 从某种角度来看，DPOS有点像是议会制度或人民代表大会制度。如果代表不能履行他们的职责（当轮到他们时，没能生成区块），他们会被除名，网络会选出新的超级节点来取代他们。EOS就是采用DPOS共识算法。 **技术原理：** 假设n为21，竞选的节点有几百个，持币人对这些节点进行投票，选出票数最多的21位，由这21位轮流来出块。 GO DEMO简单实现：

```javascript
package main

import (
    "fmt"
    "math/rand"
    "time"
    "strconv"
    "crypto/sha256"
    "encoding/hex"
)

type Block struct {
    Index int
    Timestamp string
    Prehash string
    Hash string
    Data []byte

    delegate *Node// 代理 区块由哪个节点挖出
}


func GenesisBlock()  Block {
    gene := Block{0, time.Now().String(),"", "", []byte("genesis block"), nil}

    gene.Hash = string(blockHash(gene))

    var delegate *Node = new(Node)
    delegate.Name = "Genis Block"
    delegate.Votes = 0;
    gene.delegate = delegate

    return gene
}

func blockHash(block Block) []byte  {

    record := strconv.Itoa(block.Index) + block.Timestamp + block.Prehash + hex.EncodeToString(block.Data)

    h := sha256.New()
    h.Write([]byte(record))
    hashed := h.Sum(nil)
    return hashed
}


//节点类型
type Node struct {
    Name  string //节点名称
    Votes int    // 被选举的票数
}

func (node *Node)GenerateNewBlock(lastBlock Block, data []byte) Block  {

    var newBlock = Block{lastBlock.Index+1, time.Now().String(), lastBlock.Hash, "", data, nil}

    newBlock.Hash = hex.EncodeToString(blockHash(newBlock))
    newBlock.delegate = node
    return newBlock

}

//创建节点
var NodeArr = make([]Node,10)
func CreateNode() {

    for i := 0; i < 10; i++ {
        name := fmt.Sprintf("NODE %d num", i+1)
        NodeArr[i] = Node{name, 0}
    }

}

//简单模拟投票
func Vote()  {
    for i := 0; i < 10; i++ {
        rand.Seed(time.Now().UnixNano())
        vote := rand.Intn(10) + 1
        NodeArr[i].Votes = vote
    }
}


//选出票数最多的前3位
func SortNodes() []Node  {
    n:= NodeArr
    for i := 0; i<len(n) ;i++  {
        for j := 0; j < len(n)-1 ;j++  {
            if n[j].Votes < n[j+1].Votes {
                n[j],n[j+1] = n[j+1],n[j]
            }
        }
    }

    return n[:3]
}


func main() {

    CreateNode()
    fmt.Println(NodeArr)
    Vote()
    nodes := SortNodes()

    fmt.Println(nodes)


    //创建创世区块
    gene := GenesisBlock()

    lastBlock := gene
    for i:= 0; i< len(nodes) ;i++  {
        //打印新区块信息
        // var node *Node
         node := lastBlock.delegate
         fmt.Println("区块号:",lastBlock.Index,"节点名称:",node.Name,"节点投票数:",node.Votes)

        lastBlock =  nodes[i].GenerateNewBlock(lastBlock,[]byte(fmt.Sprintf("new block %d",i)))
    }

}
```

复制

输出结果：

```javascript
[{NODE 1 num 0} {NODE 2 num 0} {NODE 3 num 0} {NODE 4 num 0} {NODE 5 num 0} {NODE 6 num 0} {NODE 7 num 0} {NODE 8 
num 0} {NODE 9 num 0} {NODE 10 num 0}]
[{NODE 1 num 3} {NODE 2 num 3} {NODE 3 num 3}]
区块号: 0 节点名称: Genis Block 节点投票数: 0
区块号: 1 节点名称: NODE 1 num 节点投票数: 3
区块号: 2 节点名称: NODE 2 num 节点投票数: 3
```

复制

#### 2.4 拜占庭容错（PBFT，Practical Byzantine Fault Tolerance） <a href="#id-8u1a1" id="id-8u1a1"></a>

\*\*优点：\*\*高速、可扩展。 \*\*不足：\*\*通常用于[私有网络](https://cloud.tencent.com/product/vpc?from\_column=20065\&from=20065)和许可网络。 \*\*采用者：\*\*Hyperledger Fabric、Stellar、Ripple、Dispatch \*\*解释：\*\*拜占庭将军问题是分布式计算中的一个经典问题。问题描述为，几位拜占庭将军分别率领部队合力包围了一座城市。他们必须一致决定是否发起攻城。如果一些将军在没有其他将军参与的情况下决定发起攻城，那么他们的行动将以失败告终。将军们之间相互隔着一定的距离，必须依靠信息传递进行交流。 一些加密货币协议在达成共识时使用了特定版本的 BFT，每种版本都具有各自的优缺点： \[1] 实用拜占庭容错（PBFT，Practical Byzantine Fault Tolerance）：首个提出的该问题解决方案称为“实用拜占庭容错”（PBFT），当前已被 Hyperledger Fabric 采用。PBFT 使用了较少（少于 20 个，之后会稍有增加）的预选定将军数，因此运行非常高效。它的优点是高交易通量和吞吐量，但是不足之处在于是中心化的，并用于许可网络。

从某种角度来看，PBFT有点像《天黑请闭眼杀人游戏》的玩法。

\[2] 联邦拜占庭协议（FBA，Federated Byzantine Agreement）：另一类拜占庭将军问题的解决方案是 FBA，已被 Stellar 和 Ripple 等代币使用。FBA 的通用理念是每个拜占庭将军负责自身的链、消息一旦到来，通过排序建立事实。在 Ripple 中，将军（验证者）是 Ripple 基金会预先选定的。在 Stellar 中，任何人都可以成为验证者，需要用户选择去相信哪个验证者。 由于 FBA 可提供令人难以置信的吞吐量、低交易开销和网络扩展性，我相信 FBA 类公式算法是目前提出的最好的分布式共识发现算法。 **技术原理：** PBFT基于拜占庭将军问题，一致性的确保主要分为这三个阶段：预准备（pre-prepare）、准备(prepare)和确认(commit)。流程如下图所示：

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/lduz9rkjcf.png" alt=""><figcaption></figcaption></figure>

其中C为发送请求端，0123为服务端，3为宕机的服务端，具体步骤如下：

\*\*1.Request：\*\*请求端C发送请求到任意一节点，这里是0 \*\*2.Pre-Prepare：\*\*服务端0收到C的请求后进行广播，扩散至123 \*\*3.Prepare：\*\*123,收到后记录并再次广播，1->023，2->013，3因为宕机无法广播 \*\*4.Commit：\*\*0123节点在Prepare阶段，若收到超过一定数量的相同请求，则进入Commit阶段，广播Commit请求； \*\*5.Reply：\*\*0123节点在Commit阶段，若收到超过一定数量的相同请求，则对C进行反馈； GO demo代码样例：

```javascript
package main

import (
    "os"
    "fmt"
    "net/http"
    "io"
)

//声明节点信息,代表各个小国家
type nodeInfo struct {
    //标示
    id string
    //准备访问的方法
    path string
    //服务器做出的相应
    writer http.ResponseWriter

}

//存放四个国家的地址
var nodeTable = make(map[string]string)

//拜占庭在Fabric中的使用
func main() {

    //获取执行的参数
    userId :=os.Args[1]//获取执行的第一个参数
    fmt.Println(userId)

    //./main Apple

    //创建四个国家的地址
    nodeTable = map[string]string {
        "Apple":"localhost:1111",
        "MS":"localhost:1112",
        "Google":"localhost:1113",
        "IBM":"localhost:1114",
    }

    node:=nodeInfo{userId,nodeTable[userId],nil}
    fmt.Println(node)

    //http协议的回调函数
    //http://localhost:1111/req?warTime=8888
    http.HandleFunc("/req",node.request)
    http.HandleFunc("/prePrepare",node.prePrepare)
    http.HandleFunc("/prepare",node.prepare)
    http.HandleFunc("/commit",node.commit)

    //启动服务器
    if err:=http.ListenAndServe(node.path,nil);err!=nil {
        fmt.Print(err)
    }



}

//此函数是http访问时候req命令的请求回调函数
func (node *nodeInfo)request(writer http.ResponseWriter,request *http.Request){
    //设置允许解析参数
    request.ParseForm()
    //如果有参数值，则继续处理
    if (len(request.Form["warTime"])>0){
        node.writer = writer
        //激活主节点后，广播给其他节点,通过Ａpple向其他节点做广播
        node.broadcast(request.Form["warTime"][0],"/prePrepare")

    }


}


//由主节点向其他节点做广播
func (node *nodeInfo)broadcast(msg string ,path string ){
    //遍历所有的国家
    for nodeId,url:=range nodeTable {

        if nodeId == node.id {
            continue
        }
        //调用Get请求
        //http.Get("http://localhost:1112/prePrepare?warTime=8888&nodeId=Apple")
        http.Get("http://"+url+path+"?warTime="+msg+"&nodeId="+node.id)
    }

}

func (node *nodeInfo)prePrepare(writer http.ResponseWriter,request *http.Request) {
    request.ParseForm()
    //fmt.Println("hello world")
    //在做分发
    if(len(request.Form["warTime"])>0){
        //分发给其他三个人
        node.broadcast(request.Form["warTime"][0],"/prepare")
    }

}

func (node *nodeInfo)prepare(writer http.ResponseWriter,request *http.Request){

    request.ParseForm()
    //调用验证
    if len(request.Form["warTime"])>0{
        fmt.Println(request.Form["warTime"][0])
    }
    if len(request.Form["nodeId"])>0 {
        fmt.Println(request.Form["nodeId"][0])
    }

    node.authentication(request)
}


var authenticationsuccess = true
var authenticationMap = make(map[string]string)
//获得除了本节点外的其他节点数据
func (node *nodeInfo)authentication(request *http.Request) {

    //接收参数
    request.ParseForm()

    if authenticationsuccess!=false  {
        if len(request.Form["nodeId"])>0 {
            authenticationMap[request.Form["nodeId"][0]]="ok"
        }
    }

    if len(authenticationMap)>len(nodeTable)/3 {
        //则拜占庭原理实现,通过commit反馈给浏览器
        node.broadcast(request.Form["warTime"][0],"/commit")

    }
}


func (node *nodeInfo)commit(writer http.ResponseWriter,request *http.Request){

    //给浏览器反馈相应
    io.WriteString(node.writer,"ok")

}
```

复制

如何运行：开启4个终端，eg：

> ./pbft Apple ./pbft IBM ./pbft MS ./pbft Google

然后在浏览器输入：[http://localhost:1112/req?warTime=1234](https://cloud.tencent.com/developer/tools/blog-entry?target=https%3A%2F%2Flinks.jianshu.com%2Fgo%3Fto%3Dhttp%253A%252F%252Flocalhost%253A1112%252Freq%253FwarTime%253D1234\&source=article\&objectId=1669859) 输出结果：

> okokok

#### 2.5 分布式一致性协议- RAFT算法 <a href="#id-2ruv7" id="id-2ruv7"></a>

**优点：** 模型比Paxos更简单，但提供了同等的安全性。有多种语言的实现可用。 \*\*不足：\*\*通常用于私有网络和许可网络。 \*\*采用者：\*\*IPFS Private Cluster、Quorum。 **解释：** 将拜占庭将军问题根据常见的工作上的问题进行简化：假设将军中没有叛军，信使的信息可靠但有可能被暗杀的情况下，将军们如何达成一致性决定？ 对于这个简化后的问题，有许多解决方案，第一个被证明的共识算法是 Paxos，由拜占庭将军问题的作者 Leslie Lamport 在1990年提出，但其论文难懂而出名，所以斯坦福大学的教授在2014年发表了新的分布式协议 Raft。与 Paxos 相比，Raft 有着基本相同运行效率，但是更容易理解，也更容易被用在系统开发上。 我们还是用拜占庭将军的例子来帮助理解 Raft。

> 假设将军中没有叛军，信使的信息可靠但有可能被暗杀的情况下，将军们如何达成一致性决定？

Raft 的解决方案大概可以理解成 先在所有将军中选出一个大将军，所有的决定由大将军来做。选举环节：比如说现在一共有3个将军 A, B, C，每个将军都有一个随机时间的倒计时器，倒计时一结束，这个将军就会把自己当成大将军候选人，然后派信使去问其他几个将军，能不能选我为总将军？假设现在将军A倒计时结束了，他派信使传递选举投票的信息给将军B和C，如果将军B和C还没把自己当成候选人（倒计时还没有结束），并且没有把选举票投给其他，他们把票投给将军A，信使在回到将军A时，将军A知道自己收到了足够的票数，成为了大将军。在这之后，是否要进攻就由大将军决定，然后派信使去通知另外两个将军，如果在一段时间后还没有收到回复（可能信使被暗杀），那就再重派一个信使，直到收到回复。 **技术原理：** Raft要求系统在任意时刻最多只有一个Leader，正常工作期间只有Leader和Followers。Raft算法将时间分为一个个的任期（term），每一个term的开始都是Leader选举。在成功选举Leader之后，Leader会在整个term内管理整个集群。如果Leader选举失败，该term就会因为没有Leader而结束。

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/292ylwp8o7.png" alt=""><figcaption></figcaption></figure>

**（1）Raft 节点状态**

从拜占庭将军的故事映射到分布式系统上，每个将军相当于一个分布式网络节点，每个节点有三种状态：Follower，Candidate，Leader，状态之间是互相转换的，可以参考下图：

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/u07i996c5z.png" alt=""><figcaption></figcaption></figure>

每个节点上都有一个倒计时器 (Election Timeout)，时间随机在 150ms 到 300ms 之间。有几种情况会重设 Timeout： （1）收到选举的请求 （2）收到 Leader 的 Heartbeat (后面会讲到) 在 Raft 运行过程中，最主要进行两个活动： （1）选主 Leader Election （2）复制日志 Log Replication

**技术原理** **（1）选主 Leader Election** 1）正常情况下选主 \[图片上传失败...(image-8988e9-1595654507761)]

假设现在有如图5个节点，5个节点一开始的状态都是 Follower。

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/4ril8p825r.png" alt=""><figcaption></figcaption></figure>

在一个节点倒计时结束 (Timeout) 后，这个节点的状态变成 Candidate 开始选举，它给其他几个节点发送选举请求 (RequestVote)

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/as2sdk14v1.png" alt=""><figcaption></figcaption></figure>

其他四个节点都返回成功，这个节点的状态由 Candidate 变成了 Leader，并在每个一小段时间后，就给所有的 Follower 发送一个 Heartbeat 以保持所有节点的状态，Follower 收到 Leader 的 Heartbeat 后重设 Timeout。

这是最简单的选主情况，**只要有超过一半的节点投支持票了，Candidate 才会被选举为 Leader**，5个节点的情况下，3个节点 (包括 Candidate 本身) 投了支持就行。

（2） 2.2 Leader 出故障情况下的选主

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/slu0hc9tpz.png" alt=""><figcaption></figcaption></figure>

一开始已经有一个 Leader，所有节点正常运行。

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/78dj1ql5ho.png" alt=""><figcaption></figcaption></figure>

Leader 出故障挂掉了，其他四个 Follower 将进行重新选主。

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/ai1iejoypz.png" alt=""><figcaption></figcaption></figure>

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/kvk13tq7qo.png" alt=""><figcaption></figcaption></figure>

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/ujieo237t8.png" alt=""><figcaption></figcaption></figure>

4个节点的选主过程和5个节点的类似，在选出一个新的 Leader 后，原来的 Leader 恢复了又重新加入了，这个时候怎么处理？在 Raft 里，第几轮选举是有记录的，重新加入的 Leader 是第一轮选举 (Term 1) 选出来的，而现在的 Leader 则是 Term 2，所有原来的 Leader 会自觉降级为 Follower

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/bxaggpqy9e.png" alt=""><figcaption></figcaption></figure>

（3）2.3 多个 Candidate 情况下的选主

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/qjsk8wtvu3.png" alt=""><figcaption></figcaption></figure>

假设一开始有4个节点，都还是 Follower。

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/o1mzacno5x.png" alt=""><figcaption></figcaption></figure>

有两个 Follower 同时 Timeout，都变成了 Candidate 开始选举，分别给一个 Follower 发送了投票请求。

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/0tc4y4ubak.png" alt=""><figcaption></figcaption></figure>

两个 Follower 分别返回了ok，这时两个 Candidate 都只有2票，要3票才能被选成 Leader。

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/u6o5n2hji6.png" alt=""><figcaption></figcaption></figure>

两个 Candidate 会分别给另外一个还没有给自己投票的 Follower 发送投票请求。

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/o5chfqzj8j.png" alt=""><figcaption></figcaption></figure>

但是因为 Follower 在这一轮选举中，都已经投完票了，所以都拒绝了他们的请求。所以在 Term 2 没有 Leader 被选出来。

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/cs9wney3z3.png" alt=""><figcaption></figcaption></figure>

这时，两个节点的状态是 Candidate，两个是 Follower，但是他们的倒计时器仍然在运行，最先 Timeout 的那个节点会进行发起新一轮 Term 3 的投票。

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/jgevimv14h.png" alt=""><figcaption></figcaption></figure>

两个 Follower 在 Term 3 还没投过票，所以返回 OK，这时 Candidate 一共有三票，被选为了 Leader。

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/ja7je0jeze.png" alt=""><figcaption></figcaption></figure>

如果 Leader Heartbeat 的时间晚于另外一个 Candidate timeout 的时间，另外一个 Candidate 仍然会发送选举请求。

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/z8at0r03jz.png" alt=""><figcaption></figcaption></figure>

两个 Follower 已经投完票了，拒绝了这个 Candidate 的投票请求。

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/ympbw4rr9e.png" alt=""><figcaption></figcaption></figure>

Leader 进行 Heartbeat， Candidate 收到后状态自动转为 Follower，完成选主。

**实现代码参考：** [https://github.com/goraft/raft](https://cloud.tencent.com/developer/tools/blog-entry?target=https%3A%2F%2Flinks.jianshu.com%2Fgo%3Fto%3Dhttps%253A%252F%252Fgithub.com%252Fgoraft%252Fraft\&source=article\&objectId=1669859) 或者 [https://github.com/happyer/distributed-computing/tree/master/src/raft](https://cloud.tencent.com/developer/tools/blog-entry?target=https%3A%2F%2Flinks.jianshu.com%2Fgo%3Fto%3Dhttps%253A%252F%252Fgithub.com%252Fhappyer%252Fdistributed-computing%252Ftree%252Fmaster%252Fsrc%252Fraft\&source=article\&objectId=1669859)

#### 2.6 有向无环图（DAG，Directed Acyclic Graphs） <a href="#flmkc" id="flmkc"></a>

**优点：** 由于 DAG 的非线性结构，它是高度可扩展的、快速、节能、立即实现终结性（Finality）。 \*\*不足：\*\*只能通过使用 Oracle 实现智能合约。 \*\*采用者：\*\*Iota、HashGraph、Byteball、RaiBlocks/Nano。 \*\*解释：\*\*DAG 是一种更通用形式的区块链。由于其独特结构，DAG 内在支持高可扩展性，因此也得到了广泛的使用。

从根本上说，任何区块链系统都具有线性结构，因为区块是依次添加到链中的。这使得相比于并行向链中添加区块，线性区块链在本质上是非常缓慢的。但是对于 DAG 而言，每个区块和交易只需数个前期区块得到确认，就可以并行地添加到区块和交易中。这意味着，DAG 在本质上是高可扩展的。

DAG 存在多种变体，取决于： · 如何选取前期区块验证的算法，也称为“Tip 选择算法”。 · 交易完成的顺序。 · 如何抵达完成状态。

下面列出一些广为使用的 DAG 项目。

**1 Tangle（IOTA）**

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/rwodzdk6qc.gif" alt=""><figcaption></figcaption></figure>

image

\*\*解释：\*\*Tangle是一种 DAG 共识算法，由 IOTA 使用。为了发送一个 IOTA 交易，用户需要验证接收到的前两个交易。在更多交易添加到 Tangle 的情况下，这种二对一、前瞻性支付的共识可加强交易的有效性。由于共识是由交易确定的，因此理论上，如果有人可以生成三分之一的交易，那么他就可以说服网络中的其余部分，使得他的无效交易变成有效的。一旦交易量足够大，使得个人难以创建三分之一交易量，这时 IOTA 就会在一个称为“协调器（The Coordinator）”的中心节点上对网络中的所有交易做“复核”（double-checking）。按 ITOA 的说法，协调员的工作类似于辅助轮。一旦 Tangle 达到一定的规模，协调员就会被从中移除。

**2 Hashgraph** 解释：Hashgraph 是由 Leemon Baird 开发的一种 Gossip 协议共识。节点随机与其它节点共享自身已知的交易，最终所有交易都被以 Gossip 协议传播到（Gossip around）到所有节点。Hashgraph 对于私有网络是一个很好的选择。但我们并不会看到它实现在以太坊这样的公共网络中，或是不通过 Gossip 协议随机传播交易。

**3 Holochain** 解释：Holochain 十分类似于 HashGraph，但不同于 Hashgraph。它提供了一种可用于构建去中心化应用的数据结构。用户可以具有自己的链，并向其中添加包括金融交易在内的数据。链可以采用复杂的方式合并、拆分和交互。数据以去中心化的方式存储（类似于 Bittorrent）。数据具有一个哈希值，即一个对应于数据的数学指纹。如果有人意图篡改数据，那么我们就会注意到在数据和哈希值之间存在不匹配，这样就可拒绝数据为无效的。数字签名保证了数据的作者身份。Holochain 可看成是“Bittorrent+git+ 数字签名”。

**4 Block-Nano**

解释：Nano（以前称为 Raiblocks）是以缠绕在区块链上的方式运行，这种方式被称为“块状格子”（Block-lattice）。在 Block-lattice 结构中，每个用户（地址）都有自己的链，只有用户本身可写，每个用户都拥有所有链的副本。

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/nx32elbwtc.jpeg" alt=""><figcaption></figcaption></figure>

每个交易都可分解为发送者链上的发送区块，以及接收者链上的接收区块。Block-lattice 看上似乎太简单，以至于无法工作，但它已经在实际运行了。Block-lattice 的独特结构的确无法抵制一些独特的攻击向量，例如 Penny-spend 攻击。在这种攻击中，攻击者通过向大量空钱包发送数额可忽略不计的金钱，导致必须要追踪的链数量急剧膨胀。

**5 SPECTRE**

解释：SPECTRE，即“序列化 PoW 事件并通过递归选举确认交易”（Serialization of Proof-of-work Events， Confirming Transactions via Recursive Elections），是提议的一种 Bitcoin 扩展解决方案。它利用 PoW 和 DAG 的组合实现可扩展的共识。在 SPECTER 中，一个挖掘的区块指向多个父节点，而不仅仅是单个节点，这使得网络每秒可以处理多个区块。而挖掘指向某些父区块的区块，这将支持区块的有效性。与 PoW 的“最长链胜出”的原则相比，SPECTER 使用的原则可描述为“拥有最多子节点的区块胜出”。SPECTRE 尚未得到实际运行测试，因此可能会存在一些新的攻击向量。但我认为，SPECTRE 很有可能成为一种修正 Bitcoin 问题的潜在好做法。

**6 ByteBall**

解释：ByteBall 使用 DAG 建立交易间的偏序关系，此外还在 DAG 中添加了“主链”（MC，Main Chain）。

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/nr4zjj696o.jpeg" alt=""><figcaption></figcaption></figure>

[图 DAG 中加粗显示的“主链”](https://cloud.tencent.com/developer/tools/blog-entry?target=https%3A%2F%2Flinks.jianshu.com%2Fgo%3Fto%3Dhttp%253A%252F%252Ffile.elecfans.com%252Fweb1%252FM00%252F81%252F1A%252Fo4YBAFwuz7qASkljAAB3bVrOWlk614.jpg\&source=article\&objectId=1669859)

MC 允许在交易间定义全序关系，即更早加入（直接或间接）MC 的交易，必定更早出现在全序中。如果存在“双重支付”问题，那么将视较早出现在全序中的交易版本为有效的，而其它所有的交易均被视为是无效的。

根据交易在图中的位置，MC 可得到确定性的定义。相关详细信息，请参阅白皮书。作为一般性规则，MC 倾向于采纳由一些总所周知用户所给出的交易，这样的用户被称为“证人”（Witnesses）。证人列表是由用户自己定义的，因为列表中包括了用户发布的每个交易。然后，MC 沿着 DAG 内路径推进。推进原则包括：

· MC 上相邻交易的证人列表要么完全相同，要么只存在一个突变。

· 与其它链相比，MC 中为经过最多数量的由见证人认证的交易。

ByteBall 也是首个在系统中包含 Oracle 的平台。Oracle 是在 DAG 中添加智能合约功能所必需的。

#### 2.7 容量证明（PoC，Proof of Capacity） <a href="#d31lm" id="d31lm"></a>

**优点：** 它类似于 PoW，只是使用空间替代了计算。因此更加环境友好。

可用于恶意软件检测。通过确定处理器的 L1 缓存是否为空（例如，具有足够空间在没有缓存未命中的情况下计算 PoSpace 过程），或是包含一个拒绝被逐出（evicted）的例程。

可用于反垃圾邮件措施，以及防范拒绝服务（DoS）攻击。

\*\*不足：\*\*激励机制可能存在问题。

**使用者：** Butcoin、Chia、SpaceMint。

\*\*类型：\*\*协同型共识。

\*\*解释：\*\*PoSpace，也称为 PoC，通过分配一定数量的内存或磁盘空间用于解决服务提供者所提供挑战的方式，显示了某个人对某个服务（例如发送邮件）具有合法的兴趣。该理念是由 Dziembowski 等在 2015 年形式化定义的。虽然 Ateniese 等人的论文名称也是“Proof-of-space”，但它事实上一种采用 MHF（Memory Hard Function，一种计算代价取决内存的哈希算法）的 PoW 协议。

PoSpace 非常类似于 PoW，只是使用存储替代了 Pow 中的计算。PoSpace 与 MHF 和可回收性证明（PoR，Proof of Retrievability）有关，但也在很大程度上存在着差异。

PoSpace 是由证明者 （Prover） 发送给验证者 （Verifier） 的一小块数据，该数据确认了证明者已经保留了一定量的空间。出于实用性上的考虑，验证过程需要尽量高效，即消耗尽可能少的空间和时间。出于公平性上的考虑，如果验证者没有保留所声明数量的空间，那么它应该难以通过验证。PoSpace 的一种实现方式是通过使用一个难以实现 Pebbling 的图。验证者请求证明者构建对一个“非 Pebbling 图”标记。证明者提交标记，进而验证者请求证明者在提交中开放多个随机位置。

由于存储的通用本质，以及存储所需的更低耗能，PoSpace 被认为是一种更公平、更绿色的替换方法。

#### 2.8 延迟工作量证明（dPoW，Delayed Proof-of-Work）、 <a href="#id-25qsu" id="id-25qsu"></a>

**优点：** 节能、安全性增加、可以通过非直接提供 Bitcoin（或是其它任何安全链），添加价值到其它区块链，无需付出 Bitcoin（或是其它任何安全链）交易的代价。 **不足：** 只有使用 PoW 或 PoS 的区块链，才能采用这种共识算法。 在“公证员激活”（Notaries Ac[TI](https://cloud.tencent.com/developer/tools/blog-entry?target=https%3A%2F%2Flinks.jianshu.com%2Fgo%3Fto%3Dhttp%253A%252F%252Fbbs.elecfans.com%252Fzhuti\_715\_1.html\&source=article\&objectId=1669859)ve）模式下，必须校准不同节点（公证员或正常节点）的哈希率，否则哈希率间的差异会爆炸（下文将给出详细解释）。 \*\*采用者：\*\*Komodo \*\*类型：\*\*协同型共识（Collabora[TI](https://cloud.tencent.com/developer/tools/blog-entry?target=https%3A%2F%2Flinks.jianshu.com%2Fgo%3Fto%3Dhttp%253A%252F%252Fbbs.elecfans.com%252Fzhuti\_715\_1.html\&source=article\&objectId=1669859)ve consensus） \*\*解释：\*\*dPoW 是一种混合共识方法，允许一个区块链利用第二个区块链的哈希算力（Hashing Power）所提供的安全。该机制是通过一组公证员节点（Notary Node）实现的。公证员节点实现将第一个区块链的数据添加到第二个区块链中。进而，第二个区块链请求在两个区块链间达成妥协，弱化第一个区块链的安全。Komodo是首个使用该共识方法的区块链，它就是附加于 Bitcoin 区块链之上的。

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/q3bbv53aig.png" alt=""><figcaption></figcaption></figure>

使用 dPoW 的区块链也可以使用 PoW 或 PoS 共识方法工作，并可以附加在任何采用 PoW 的区块链上。但对于由 dPoW 提供安全的区块链，当前 Bitcoin 给出了最高安全层级的哈希率。下图展示了主区块链的单个记录以及其所附着的 PoW 区块链。

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/gkczwo9rgh.png" alt=""><figcaption></figcaption></figure>

image.png

dPoW 系统中有两种类型的节点：公证人节点和正常节点。64 个公证人节点是由 dPoW 区块链的权益持有者（stakeholder）选举产生的，它们可从 dPoW 区块链向所附加的 PoW 区块链添加经公证确认的块。一旦添加了一个块，该块的哈希值将被添加到由 33 个公证人节点签署的 Bitcoin 交易中，并创建一个哈希到 Bitcoin 区块链的 dPow 块记录。该记录已被网络中的大多数公证人节点公证。

为避免公证人节点间在挖矿上产生战争，进而降低网络的效率，Komodo 设计了一种采用轮询机制的挖矿方法。该方法具有两种运行模式。在“无公证人”（No Notary）模式下，支持所有网络节点参与挖矿，这类似于传统 PoW 共识机制。而在“公证人激活”（Notaries Ac[TI](https://cloud.tencent.com/developer/tools/blog-entry?target=https%3A%2F%2Flinks.jianshu.com%2Fgo%3Fto%3Dhttp%253A%252F%252Fbbs.elecfans.com%252Fzhuti\_715\_1.html\&source=article\&objectId=1669859)ve）模式下，网络公证人使用一种显著降低的网络难度率挖矿。“公证人激活”模式下，允许每位公证人使用其当前的难度挖掘一个区块，而其它公证人节点必须采用 10 倍难度挖矿，所有正常节点使用公证人节点难度的 100 倍挖矿。

但这会导致一些问题。我在与 Komodo 创始人的一次谈话中提及，这将导致公证人矿工和正常矿工间的哈希率存在很高的差异：

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/rtdztnfmn4.png" alt=""><figcaption></figcaption></figure>

image.png

图 本文作者与 Komodo 创始人间就不一致性问题进行交流的截图

dPoW 系统在设计上支持区块链在没有公证人节点的情况下继续运行。在这种情况下，dPoW 区块链可以基于初始的共识方法继续运行，但将不再具有所附着区块链增添的安全。

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/rfh1p585wi.png" alt=""><figcaption></figcaption></figure>

所有使用 dPoW 的区块链可增加安全，同时降低能耗。例如，Komodo 使用 Equihash 哈希算法防止使用 ASIC 挖矿。其公证人节点依赖于一种轮询挖矿方法，奖励机制考虑了降低节点间竞争的可能性。这些节点将会引发过度耗能或算力。

此外通过非直接提供 Bitcoin 安全，Komodo 这类 dPoW 区块链可以向其它区块链添加价值，无需付出任何 Bitcoin 交易的代价。Komodo 此后附着到 Bitcoin，而第三个使用 dPoW 的区块链可以将自身附着到 Komodo。使用这种方式，dPoW 区块链不必直接附着到 Bitcoin 区块链，就从 Bitcoin 的高哈希率中受益。

最后一点，公证人节点和正常节点分离的功能，确保了初始共识机制在公证人节点失败时继续运行。这种相互独立性建立了一种奖励机制，使得其它网络无需依赖于 Bitcoin 网络的直接功能，即可支持 Bitcoin 网络的继续维护。

#### 2.9 权威证明（PoA，Proof-of-Authority） <a href="#a2qfe" id="a2qfe"></a>

\*\*优点：\*\*节能、快速。 \*\*不足：\*\*略为中心化。虽然可用于公有区块链，但是通常用于私有区块链和许可区块链。

\*\*使用者：\*\*POA.Network、Ethereum Kovan testnet、VeChain。 \*\*类型：\*\*协同型共识。

\*\*解释：\*\*基于 PoA 的网络、事务和区块，是由一些经认可的账户认证的，这些被认可的账户称为“验证者”（Validator）。验证者运行的软件，支持验证者将交易（transaction）置于区块中。该过程是自动的，无需验证者持续监控计算机，但需要维护计算机（权威节点）不妥协（uncompised）。

验证者必须满足以下三个条件： 1. 其身份必须在链上得到正式验证，信息可在公有可用域中交叉验证。 2. 其资格必须难以获得，这样所得到的验证块的权利才弥足珍贵（例如，潜在的验证者需要获得公证书）。 3. 建立权威的检查和程序必须完全统一。

使用 PoA，每个个体都具有变成验证者的权利，因此存在一旦获取就保持验证者位置的动机。通过对身份附加一个声誉，可以鼓励验证者去维护交易的过程。因为验证者并不希望让自己获得负面声誉，这会使其失去来之不易的验证者地位。

#### 2.10 权重证明（PoWeight，Proof-of-Weight） <a href="#id-8tb0t" id="id-8tb0t"></a>

\*\*优点：\*\*节能、高度可定制和可扩展 \*\*不足：\*\*可能难以实现激励、 \*\*采用者：\*\*Algorand。 \*\*类型：\*\*有竞争共识。 \*\*解释：\*\*权重证明（PoWeight）是一类很宽泛的共识算法，它基于Algorand共识模型。其基本理念是在 PoS 中，用户所拥有的网络中令牌的百分比，表示了该用户“发现”下一个区块的概率。PoWeight 系统中还使用了其它一些相对加权值，实现包括声望证明（PoR，Proof of Reputation）和空间证明（Proof of Space）。

#### 2.11. 声誉证明（PoR，Proof of Reputation） <a href="#id-22j74" id="id-22j74"></a>

\*\*优点：\*\*非常适用于私有区块链和许可区块链。 \*\*不足：\*\*只能用于私有区块链和许可区块链。 \*\*采用者：\*\*GoChain。 \*\*类型：\*\*协同型共识。 \*\*解释：\*\*PoR 类似于 PoA。GoChain 文档中给出了如下描述： PoR 共识模型依赖参与者在保持[网络安全](https://cloud.tencent.com/product/ns?from\_column=20065\&from=20065)中的声誉。参与者（区块签名者）必须具有足够重要的声誉。一旦他们尝试欺骗系统，那么他们将要面对严重的财政上的和自己名声上的后果。这是一个相对的概念，如果他们被抓到试图欺骗，那么几乎所有的业务将会受到严重的影响。规模越大的企业，通常将会失去更多。这样，相比使用更少的企业（即更小规模的商业），规模更大的企业更易于被选定。

一旦一个企业证明了自己的声誉，并通过了验证，那么他们必须经投票参与到权威节点网络中。这时，PoR 的操作与 PoA 网络一样，即只有权威节点可以签名并验证区块。

#### 2.12. 所用时间证明（PoET，Proof of Elapsed Time） <a href="#cfs53" id="cfs53"></a>

**优点：** 参与代价低。更多人可轻易加入，进而达到去中心化。 对于所有参与者而言，更易于验证领导者是通过合法选举产生的。 控制领导者选举过程的代价，是与从中获得的价值成正比的。 **不足：** 尽管 PoET 的代价低，但是必须要使用特定的硬件。因此不会被大规模采纳。 不适用于公有区块链。

\*\*采用者：\*\*HyperLedger Sawtooth

\*\*类型：\*\*有竞争共识

\*\*解释：\*\*PoET 共识机制算法通常用于许可区块链网络，它可决定网络中获得区块者的挖矿权利。许可区块链网络需要任何预期参与者在加入前验证身份。根据公平彩票系统的原则，每个节点具有同等的可能成为胜出者。PoET 机制赋予大量可能的网络参与者以平等胜出的机会。

PoET 的工作机制如下：网络中的每位参与节点都必须等待一个随机选取的时期，首个完成设定等待时间的节点将获得一个新区块。区块链网络中的每个节点会生成一个随机的等待时间，并休眠一个设定的时间。最先醒来的节点，即具有最短等待时间的节点，唤醒并向区块链提交一个新区块，然后广播必要的信息到整个对等网络中。同一过程将会重复，以发现下一个区块。

在 PoET 网络共识机制中，需要确保两个重要因素。第一，参与节点在本质上会自然地选取一个随机的时间，而非某一个参与者为胜出而刻意选取了较短的时间。第二，胜出者的确完成了等待时间。

PoET 理念是由著名的芯片制造巨头 Intel于 2016 年早期提出的。Intel 为解决“随机领导者选举”的计算问题，实现了一个可用的高科技工具。

这种内在机制允许应用在受保护的环境中执行受信任的代码，它确保了上面提出的两个要求得到满足，即随机选择所有参与节点的等待时间，以及胜出参与者真正完成了等待时间。

这种在安全环境中运行可信代码的机制也同时考虑到了其它一些网络的需求。它确保了受信代码的确运行在安全环境中，并不可被其它外部参与者更改。它也确保了结果可被外部参与者和实体验证，进而提高了网络共识的透明度。

PoET 通过控制代价实现了共识过程，该代价依然是与从过程中获得的价值成正比。这是保证加密货币经济持续繁荣的一个关键需求。

#### 2.13 历史证明（PoHistory，Proof of History） <a href="#c8s8t" id="c8s8t"></a>

采用者：Solana

解释：其基本理念是不相信交易中的时间戳，而是证明交易在某个事件之前或之后的某个时刻发生。

如果我们对某期《纽约时报》的封面拍了张照片，那么我们就创建了一个证明，即我们的拍照时间是在该报纸发行之后，或许也可能是我们有某种途径影响了纽约时报的正常发行。我们可以使用 PoHistory 创建一个历史记录，证明一个事件是发生在特定时间之后的。

<figure><img src="https://ask.qcloudimg.com/http-save/yehe-2874029/2y2kifk8hv.jpeg" alt=""><figcaption></figcaption></figure>

[区块链共识算法全面详解](https://cloud.tencent.com/developer/tools/blog-entry?target=https%3A%2F%2Flinks.jianshu.com%2Fgo%3Fto%3Dhttp%253A%252F%252Ffile.elecfans.com%252Fweb1%252FM00%252F81%252F1A%252Fo4YBAFwuz7mAed46AABNrEyaj-g466.jpg\&source=article\&objectId=1669859)

PoHistory 是一种高频可验证延迟函数（VDF，Verifiable Delay Function）。VDF 求值需要完成特定数量的顺序步骤，然后生成一个唯一的输出。该输出可被高效地和公开地验证。

VDF 的一个特定实现使用了持续运行于其上的顺序抗预映射哈希（Pre-image Resistant Hash），其中前一次循环生成的输出将用于下一次循环的输入。计数和当前输出形成周期性记录。

如果使用了 SHA256 哈希函数，那么不使用 2128核的暴力攻击，该过程是不可能并行化的。

因此我们可以确认，每个计数器在生成过程中都的确经历了一定的时间。进而，每个计数器记录的顺序与实时情况是一致的。

#### 2.14 权益流通证明（PoSV，Proof of Stake Velocity） <a href="#fptb2" id="fptb2"></a>

采用者：Reddcoin

解释：PoSV 是作为 PoW 和 PoS 的一种替代方法而提出的，其目的是提高 P2P 网络的安全性，进而用于确认 Reddcoin 交易。Reddcoin 是一种加密货币，专为加速数字化时代的社交交互而提出的。PoSV 在设计上鼓励所有者（权益）和活动（流通），直接对应于 Reddcoin 作为真实货币的两个主要功能，即存储价值和交换中介。Reddcoin 也可在异构社交场景中作为计量单位使用。

#### 2.15 重要性证明（PoImportance，Proof of Importance） <a href="#eat10" id="eat10"></a>

优点：在权益计算方面要优于 PoS。

使用者：NEM

解释：NEM 共识网络不仅依赖于代币的数量，而且依赖于生成系统行动得到回报的可能性。区块收益机率是各种因素之一，此外还包括不好的名声（受控于不同的框架设计目的）、差额，以及从该处做出和得到的交易数量。它也被称为“重要性计算”（Importance Calculation），因为它可为“有用的”系统成员提供更全面的图像。

一名用户要具有资格执行重要性计算，其账户余额至少需要为 10000 枚 XEM。考虑到只有不到 90 亿枚 XEM 在流通，实现这一目标并非过于昂贵。在未来 10000 枚 XEM 的阈值有可能会发生变化，但就目前而言，它仍然没有变化。重要性计算是使用特定算法完成的，而不仅仅考虑用户份额的概率和规模。

需要指出的是，NEM 的 PoImportance 对任何操控都具有抵制力。该共识的底层机制可缓解女巫攻击（Sybil Attack）和循环攻击问题。谨记，“PoImportance 并非 PoS”，尽管两者很容易被同等看待。

#### 2.16 烧毁证明（PoBurn，Proof of Burn） <a href="#id-7duqk" id="id-7duqk"></a>

采用者：Slimcoin、TGCoin（第三代代币）。

解释：PoBurn 并非在昂贵的计算设备上一掷千金，而通过发送代币到一个不可检索地址实现“烧钱”（Burn）。将代币发送到一个并不存在的地址，用户将根据某个随机选择过程，获得整个生命时间内对系统挖矿的特权。

PoBurn 有多种实现方式，矿工可以烧毁原生的货币，或者烧毁一些其它区块链的货币，例如比特币等。烧毁的代币越多，用户就越有机会被选中去挖掘下一个区块。

随时间的流逝，用户在系统的权益会得到弱化。因此，最终用户为增加在这个博彩中被选中的机会，会考虑烧掉更多的代币（这可类比于比特币的挖矿过程，用户必须不断投资更现代的计算设备以维持哈希能力）。

尽管 PoBurn 是一种有意思的 PoW 替代者，但是该协议依然会毫无必要地浪费资源。另一个批评是，挖矿能力只会偏向于那些愿意烧掉更多钱的人。

#### 2.17 身份证明（PoI，Proof of Identity） <a href="#frt6c" id="frt6c"></a>

解释：PoI 是一块表示了加密事实的数据。它支持用户指定一个私钥，并对应到一个经认证的身份，加密将附着到一个指定的交易。来自于某些组中的每个个体都可以创建 PoF（因为它只是一块数据），并将该数据展示给其它任何处理节点的人。

#### 2.18 活动证明（PoActivity，Proof Of Activity） <a href="#id-873hf" id="id-873hf"></a>

使用者：Decred

解释：为避免出现恶性通货膨胀（当大量货币充斥系统时就会发生），比特币将只生成两千一百万枚。这意味着，在某些时候，比特币区块奖励补贴将终止，比特币矿工将只能收取交易费用。

一些人猜测这可能会导致由“公地悲剧（Tragedy of the commons）”所引发的安全问题，人们出于自身利益考虑行事并破坏系统。因此，人们提出了PoActivity作为一种替代 Bitcoin 的激励结构。PoActivity 是一种结合了 PoW 和 PoS 的混合方法。

在 PoActivity 中，挖矿一开始使用的是传统的 PoW，矿工们争相解决加密难题。根据实现，挖掘的区块不包含任何交易，它们更像模板。因此，胜出的区块将只包含头部信息，以及矿工的奖励地址。

此时，系统将切换到 PoS。PoActivity 根据头部信息选择一组随机验证者对新区块签名。如果一位验证者所拥有的系统中代币越多，那么该验证者被选中的可能性也会越大。一旦所有验证者已签名，那么模板就会变成一个完整的区块。

如果在完成区块时，某些选定的验证者是不可用的，那么就选择下一个胜出区块，并选择一组新的验证者，依此类推，直到区块收到到正确数量的签名。费用由矿工和在区块上签名的验证者分摊。

对 PoActivity 的批评包括挖掘区块耗能过高（与 PoW 一样），以及无法阻止验证者做双重签名（与 PoS 一样）。

#### 2.19 时间证明（PoTime，Proof of Time） <a href="#cpp65" id="cpp65"></a>

使用者：Chronologic

解释：PoTime 是一种由 Chronologic 提出的共识算法。Chronologic 设计构建一种独立的区块链，其首席开发人员提出：我们的问题在于，Solidity 中一个变量可存储的最大数是 1076 的数量级。这使我们很难处理时间生成和令牌生成。

#### 2.20 存在证明（PoExistence，Proof of Existence） <a href="#id-2kgmd" id="id-2kgmd"></a>

使用者：Poex.io、HeroNode、DragonChain。

解释：PoExistence 是一种在线服务，它通过比特币区块链对交易打时间戳，验证在特定时间是否存在计算机文件。PoExistence 是作为一项开源项目在 2013 年提出的，由 Manuel Araoz 和 Esteban Ordano 开发。

用例：

不泄露实际内容的数字签署协议（Digital Sign Agreement）。

不泄露实际数据，展示数据的属主。

记录时间戳。

证明属主。

检查文档完整性。

#### 2.21 Ouroboros <a href="#arnk0" id="arnk0"></a>

采用者：Cardano

解释：Ouroboros 是 Cardano 使用的共识算法。它是 PoS 的一个变种，具有严格的安全性保证。

#### 2.22 可收回证明（PoR，Proof of Retrievability） <a href="#id-3acln" id="id-3acln"></a>

采用者：Microsoft

解释：PoR 是一种紧凑证明，表示文件系统（证明者）中的目标文件 F 对客户端（验证者）而言是完整的。由于使用 PoR 比传输文件 F 本身而言具有更低的通信复杂性，因此 PoR 对于构建高可靠的远程存储系统是一种颇具吸引力的构建模块。作为一种共识算法，PoR 对于云计算系统非常有用。

#### 2.23. 授权拜占庭容错算法（dBFT，Delegated Byzantine Fault Tolerance） <a href="#id-8vrer" id="id-8vrer"></a>

优点：快速、可扩展。

不足：每个人都争相成为根链。其中可能存在多个根链。

采用者：Neo。

解释：授权拜占庭容错算法，简称 dBFT，是一种支持通过代理投票实现大规模参与共识的拜占庭容错共识算法。在 Neo 中，令牌持有者可以通过投票选取其支持的 bookkeeper。之后，选定的 bookkeeper 组采用 BFT 算法达成共识，并生成新区块。Neo 网络中的投票是实时的，而非因人而异的。

dBFT 可为具有个共识节点的共识系统提供\（f = \{{n-1} \over 3}\）容错。这种容错也涵盖了安全性和可用性、不受将军和拜占庭错误影响，并且适合任何网络环境。dBFT 具有很好的最终性（finality），这意味着一旦最终确认，区块将不可分叉，交易将不可再撤销或是回滚。

Neo 的 dBFT 机制生成一个区块需 15 到 20 秒钟。交易吞吐量测定约为 1000 TPS。这对于公共区块链而言，这是很好的性能。通过一定优化，dBFT 具有达到一万 TPSS 的潜力，这样就可支持大规模的商业应用。

dBFT 中加入了[数字身份](https://cloud.tencent.com/product/tdid?from\_column=20065\&from=20065)技术，这意味着 bookkeeper 可以是真实的个人，也可以是某些机构。因此，dBFT 根据存在于其本身之中的司法判决，可以冻结、撤销、继承、检索和拥有代币兑换权。它有利于实现合规金融资产在 Neo 网络中的注册。Neo 网络从设计上，就是在必要时为此提供支持。

#### 2.24 恒星共识（Stellar Consensus） <a href="#id-5ns5b" id="id-5ns5b"></a>

优点：去中心化控制、低延迟、灵活的信任机制、渐进安全（Asymptotic security）。

采用者：Stellar

解释：恒星共识基于上文介绍的联邦拜占庭共识（FBA）。

恒星共识协议（SCP，Stellar Consensus Protocol）提供了一种不依赖闭合系统实现准确记录金融交易而达成共识的方法。SCP 具有一组可验证的安全属性，这些属性根据如何安全地保持活力而做了优化。一旦出现分区或不当行为节点，它将会终止网络过程，直至达成共识。SCP 同时具备四种属性：去中心控制、低延迟、灵活信任机制和渐进安全。

#### 2.25 置信度证明（PoB，Proof of Believability） <a href="#id-1sh9j" id="id-1sh9j"></a>

优点：

通过使用一种称为“Servi”的理念，PoB 比传统 PoS 更加去中心化（细节在下文给出）。

相比于传统的 PoS，具有更快的最终性（Finality）。

采用者：IOST

解释：传统的 PoS 共识机制面临的主要挑战是趋向于中心化。为了降低这种风险，IOST 引入了“Servi”概念。Servi 不仅衡量了用户对社区的贡献，而且鼓励成员为 IOSChain 的持续发展做出贡献。Servi 具有以下属性：

不可交易性（Non-tradable）：由于 Servi 并非设计作为一种交换媒介，因此 Servi 不能以任何方式交易或做交换。

自毁性（Self-destructive）：验证区块后，系统将自动清除验证者拥有的 Servi 余额。通过这种方式，具有高可信度分值的节点可轮流验证区块，确保了公平区块的生成。

自发行性（Self-issuance）：Servi 在做出某些贡献之后（例如，提供社区服务、估其他实体提供的服务，以及其它一些特殊贡献），将会自动生成并存入用户帐户。

传统的区块链系统在安全性和吞吐量间存在着固有的折衷，具体取决于分片（shard）的大小。具有大量小分片的系统可提供更好的性能，但抵抗不良行为者的稳定性低，反之也是如此（这也是 Casper 面临的一个问题）。为了在保持安全和提高吞吐量的情况下打破这种权衡，IOST 创新性地提出了一种用于 IOSChain 的 PoB 共识协议。PoB 确保了节点产生行为不端的可能性微乎其微，同时通过确定分片规模（size-one-shard），显著地提高了交易吞吐量。

PoB 共识协议使用一种分片内“可信度优先”的方法。该协议将所有的验证者分为两组，一组是可信的联盟，另一组是正常的联盟。在第一阶段，可信的验证者快速地处理交易。之后在第二阶段，普通验证者对交易做抽样并验证，提供最终结果，确保可验证性。节点被选入可信联盟的机会是由可信度分值确定的。可信度分值由多个因素计算，包括令牌余额、对社区的贡献、评论等。具有较高可信度分值的人，更有可能被选入可信联盟。可信验证者遵循一定的程序，决定已提交的交易及其订单的集合，并按顺序处理它们。可信验证者也会构成一些较小的组，甚至可以每组一名验证者。交易将在这些可信验证者之间随机分配。因此，PoB 会产生具有极低延迟的较小区块。

但是，由于只有一个节点在执行验证，因此 PoB 可能会存在安全问题。行为不当的验证者可能会提交一些已损坏的交易。为了解决这个安全问题，PoB 指定了一个采样概率。普通验证者根据概率对交易做采样，并检测交易的不一致性。如果验证者被检测出存在不良行为，那么该验证者将会失去所有系统中的令牌和声誉，而被欺诈的用户将获得所有损失的补偿。“可信度优先”使处理交易非常快，因为只有一个（可信的）验证者执行验证，并且该验证者不太可能存在行为不端。

### 3，参考 <a href="#id-1ii1v" id="id-1ii1v"></a>

（1）分布式共识算法专栏 - 汇集各种共识算法 [https://recomm.cnblogs.com/blogpost/11284374?page=1](https://cloud.tencent.com/developer/tools/blog-entry?target=https%3A%2F%2Flinks.jianshu.com%2Fgo%3Fto%3Dhttps%253A%252F%252Frecomm.cnblogs.com%252Fblogpost%252F11284374%253Fpage%253D1\&source=article\&objectId=1669859)

（2）区块链共识算法全面详解 [http://www.elecfans.com/blockchain/843819.html](https://cloud.tencent.com/developer/tools/blog-entry?target=https%3A%2F%2Flinks.jianshu.com%2Fgo%3Fto%3Dhttp%253A%252F%252Fwww.elecfans.com%252Fblockchain%252F843819.html\&source=article\&objectId=1669859)

（3）共识算法DPOS原理及实现 [https://www.meiwen.com.cn/subject/hxqzyftx.html](https://cloud.tencent.com/developer/tools/blog-entry?target=https%3A%2F%2Flinks.jianshu.com%2Fgo%3Fto%3Dhttps%253A%252F%252Fwww.meiwen.com.cn%252Fsubject%252Fhxqzyftx.html\&source=article\&objectId=1669859)

（4）拜占庭PBFT简单实现 [https://www.meiwen.com.cn/subject/prvjuftx.html](https://cloud.tencent.com/developer/tools/blog-entry?target=https%3A%2F%2Flinks.jianshu.com%2Fgo%3Fto%3Dhttps%253A%252F%252Fwww.meiwen.com.cn%252Fsubject%252Fprvjuftx.html\&source=article\&objectId=1669859)

（5）PBFT算法 [https://www.meiwen.com.cn/subject/owzvyxtx.html](https://cloud.tencent.com/developer/tools/blog-entry?target=https%3A%2F%2Flinks.jianshu.com%2Fgo%3Fto%3Dhttps%253A%252F%252Fwww.meiwen.com.cn%252Fsubject%252Fowzvyxtx.html\&source=article\&objectId=1669859)
