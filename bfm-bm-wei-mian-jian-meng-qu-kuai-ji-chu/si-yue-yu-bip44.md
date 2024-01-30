# 私钥与BIP44

#### 什么是加密数字资产钱包

在区块链中，我们的数字资产并没有保存在钱包服务商（例如 imToken）的服务器中，而是「保存」在由私钥推导出来的钱包地址中，放置在区块链网络上。只有拥有地址对应的的私钥，才有转移资产的权力。

因此，数字货币钱包实际上就是一个生成和存储私钥的工具，它并不保存资产，资产全部都是在链上的。

创建钱包地址的关键就是随机生成一把私钥，私钥是一个 32 字节的数字。生成私钥的本质就是在 1 到 2^256 之间选一个数字。因此生成私钥的第一步就是找到一个安全的获取真随机数的办法，来保证获得的随机数是不可预测或不可重复的。

例如：你可以抛硬币 256 次，用纸笔记录正反面并转换为 0 和 1，随机得到的 256 位二进制数字可以作为钱包的私钥。

#### BIP 32 是如何来的？ <a href="#bip-32" id="bip-32"></a>

钱包是私钥管理工具，我们可以根据使用需求生成很多私钥。但是你会发现备份和管理私钥是非常麻烦的。最早期的 BTC 钱包就是这样的，所以他还有一个昵称“Just a Bunch Of Keys”（一堆私钥）。为了解决这种麻烦，就有了 [BIP32 31](https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki) 提议：根据一个随机数种子通过分层确定性推导的方式得到 N 个私钥，这样保存的时候，只需要保存一个种子就可以了，私钥可以通过种子推导出来，如图：

[![](https://imtoken.fans/uploads/default/optimized/1X/cad0544331290fc3d4ee8087c251ca573243d5b4\_2\_602x397.png)1055×697 177 KB](https://imtoken.fans/uploads/default/original/1X/cad0544331290fc3d4ee8087c251ca573243d5b4.png)

（图片来自 Mastering Bitcoin）

注：BIP （Bitcoin Improvement Proposals），比特币改进建议，BIP32 是第 32 个改进建议。BIP32 提案名称：Hierarchical Deterministic Wallets，就是我们说的分层确定性钱包（HD 钱包）。

一句话概括下BIP32就是：为了避免管理一堆私钥的麻烦提出的分层推导方案。

#### 秘钥路径及 BIP44 <a href="#bip44" id="bip44"></a>

通过这种分层方式推导出来的秘钥，通常用路径来表示，每个级别之间用斜杠 / 来表示，由主私钥衍生出的私钥起始以“m”打头。因此，第一个母密钥生成的子私钥是 m/0。第一个公共钥匙是 M/0。第一个子密钥的子密钥就是 m/0/1，以此类推。

BIP44 则是为这个路径约定了一个规范的含义(也扩展了对多币种的支持)，BIP44 指定了包含 5 个预定义树状层级的结构：

m / purpose’ / coin’ / account’ / change / address\_index

m 是固定的，Purpose 也是固定的，值为 44（或者 0x8000002C）

**Coin type**

这个代表的是币种，0 代表比特币，1 代表比特币测试链，60 代表以太坊

完整的币种列表地址：[https://github.com/satoshilabs/slips/blob/master/slip-0044.md 189](https://github.com/satoshilabs/slips/blob/master/slip-0044.md)

**Account**

代表这个币的账户索引，从0开始

**Change**

常量 0 用于外部链，常量 1 用于内部链（也称为更改地址）。外部链用于在钱包外可见的地址（例如，用于接收付款）。内部链用于在钱包外部不可见的地址，用于返回交易变更。 (所以一般使用 0)

**address\_index**

这就是地址索引，从 0 开始，代表生成第几个地址，官方建议，每个 account 下的 address\_index 不要超过 20

根据 EIP85 提议的讨论以太坊钱包也遵循 BIP44 标准，确定路径是 m/44’/60’/a’/0/n

a 表示帐号，n 是第 n 生成的地址，60 是在 SLIP44 提案中确定的以太坊的编码。所以大家在使用 imToken 导入助记词的时候会看到选择路径的选项，原因就在这里。

[![](https://imtoken.fans/uploads/default/optimized/1X/e57141610c87b2c8bc031139e6dee920a1427707\_2\_326x500.png)556×850 111 KB](https://imtoken.fans/uploads/default/original/1X/e57141610c87b2c8bc031139e6dee920a1427707.png)

一句话概括下 BIP44 就是：给 BIP32 的分层路径定义规范。

#### 什么是 BIP39？ <a href="#bip39" id="bip39"></a>

BIP32 能够让我们保存一个随机数种子，而不是一堆密钥。但是对于大部分用户来讲，还是非常不友好，这就促使了 [BIP39 29](https://github.com/bitcoin/bips/blob/master/bip-0039.mediawiki) 的出现。它使用助记词的方式生成种子，这种情况下用户只要记住助记词，就可以创造出随机种子作为 BIP32 的种子。

![](https://imtoken.fans/uploads/default/original/1X/a33800fe0bbc2e6d51ac3b6cca0e2019f610a1e9.png)

（做一个对比，备份助记词比备份随机数种子要方便很多）

整个过程包含两步：1.生成助记词 2.助记词推导出种子

**生成助记词方式**

助记词生成的过程是这样的：先生成一个128位随机数，再加上对随机数做的校验4位，得到132位的一个数，然后按每11位做切分，这样就有了12个二进制数，然后用每个数去查BIP39定义的单词表，这样就得到12个助记词，这个过程图示如下：

[![](https://imtoken.fans/uploads/default/optimized/1X/cb2275cd1499f2bf51e1496b8cd1a58c420606b9\_2\_483x500.png)795×822 56.4 KB](https://imtoken.fans/uploads/default/original/1X/cb2275cd1499f2bf51e1496b8cd1a58c420606b9.png)

（图来源于网络）

**助记词推导种子**

这个过程使用密钥拉伸（Key stretching）函数，用来增强弱密钥的安全性。（这里就不详细说明了，有兴趣的小伙伴可以自行查找资料）

一句话概括下BIP39就是：通过定义助记词让种子的备份更友好。

#### 总结 <a href="#e680bbe7bb93" id="e680bbe7bb93"></a>

HD 钱包（Hierarchical Deterministic Wallets）是在 BIP32 中提出的为了避免管理一堆私钥的麻烦提出的分层推导方案。

BIP44 是给 BIP32 的分层增强了路径定义规范，同时增加了对多币种的支持。

BIP39 则通过定义助记词让种子的备份更友好。

imToken 完全遵循这几种标准，所以只要支持这几种协议的钱包助记词都可以导入 imToken。

参考资料：

[分层确定性钱包 HD Wallet 介绍 87](https://zhuanlan.zhihu.com/p/30297080)

[深入浅出区块链博客 21](https://learnblockchain.cn/)
