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

如果你还在被HD钱包(分层确定性钱包)、BIP32、BIP44、BIP39搞的一头雾水，来看看这边文章吧。

### 数字钱包概念 <a href="#shu-zi-qian-bao-gai-nian" id="shu-zi-qian-bao-gai-nian"></a>

钱包用来存钱的，在区块链中，我们的数字资产都会对应到一个账户地址上， 只有拥有账户的钥匙（私钥）才可以对资产进行消费（用私钥对消费交易签名）。\
私钥和地址的关系如下：![关系](https://img.learnblockchain.cn/2018/9efa20eff737374479d9c6bb86db82b3.png!wl)\
（图来自精通比特币）\
一句话概括下就是：**私钥通过椭圆曲线生成公钥， 公钥通过哈希函数生成地址，这两个过程都是单向的。**

因此实际上，数字钱包实际是一个管理私钥（生成、存储、签名）的工具，注意钱包并不保存资产，资产是在链上的。

### 如何创建账号 <a href="#ru-he-chuang-jian-zhang-hao" id="ru-he-chuang-jian-zhang-hao"></a>

创建账号关键是生成一个私钥， 私钥是一个32个字节的数， **生成一个私钥在本质上在1到2^256之间选一个数字**。\
因此生成密钥的第一步也是最重要的一步，是要找到足够安全的熵源，即随机性来源，只要选取的结果是不可预测或不可重复的，那么选取数字的具体方法并不重要。

比如可以掷硬币256次，用纸和笔记录正反面并转换为0和1，随机得到的256位二进制数字可作为钱包的私钥。

从编程的角度来看，一般是通过在一个密码学安全的随机源(不建议大家自己去写一个随机数)中取出一长串随机字节，对其使用SHA256哈希算法进行运算，这样就可以方便地产生一个256位的数字。

> 实际过程需要比较下是否小于n-1（n = 1.158 \* 10^77, 略小于2^256），我们就有了一个合适的私钥。否则，我们就用另一个随机数再重复一次。这样得到的私钥就可以根据上面的方法进一步生成公钥及地址。

### BIP32 <a href="#bip32" id="bip32"></a>

钱包也是一个私钥的容器，按照上面的方法，我们可以生成一堆私钥（一个人也有很多账号的需求，可以更好保护隐私），而每个私钥都需要备份就特别麻烦的。

> 最早期的比特币钱包就是就是这样，还有一个昵称：“Just a Bunch Of Keys(一堆私钥)“

为了解决这种麻烦，就有了[BIP32 提议](https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki)： 根据一个随机数种子通过分层确定性推导的方式得到n个私钥，这样保存的时候，只需要保存一个种子就可以，私钥可以推导出来，如图：

![推导](https://img.learnblockchain.cn/2018/450b5358b96ef5b32ec775efed901f2a.png!wl/scale/50)\
（图来自精通比特币）上图中的孙秘钥就可以用来签发交易。

> 补充说明下 BIP: Bitcoin Improvement Proposals 比特币改进建议, bip32是第32个改进建议。\
> BIP32提案的名字是：Hierarchical Deterministic Wallets， 就是我们所说的HD钱包。

来分析下这个分层推导的过程，第一步推导主秘钥的过程：\
![推导主秘钥的过程](https://img.learnblockchain.cn/2018/3ec7468aa49d907b0ec66b5d8b41a0a1.png!wl/scale/40)

根种子输入到HMAC-SHA512算法中就可以得到一个可用来创造主私钥(m) 和 一个主链编码（ a master chain code)这一步生成的秘钥（由私钥或公钥）及主链编码再加上一个索引号，将作为HMAC-SHA512算法的输入继续衍生出下一层的私钥及链编码，如下图：![衍生](https://img.learnblockchain.cn/2018/a9a6e6a31f39e812f579a4c8bdf09347.png!wl/scale/40)

> 衍生推导的方案其实有两个：一个用父私钥推导（称为强化衍生方程），一个用父公钥推导。同时为了区分这两种不同的衍生，在索引号也进行了区分，索引号小于2^31用于常规衍生，而2^31到2^32-1之间用于强化衍生，为了方便表示索引号i'，表示2^31+i。

因此增加索引（水平扩展）及 通过子秘钥向下一层（深度扩展）可以无限生成私钥。

注意， 这个推导过程是确定（相同的输入，总是有相同的输出）也是单向的，子密钥不能推导出同层级的兄弟密钥，也不能推出父密钥。如果没有子链码也不能推导出孙密钥。现在我们已经对分层推导有了认识。

一句话概括下BIP32就是：**为了避免管理一堆私钥的麻烦提出的分层推导方案。**

#### 秘钥路径及BIP44 <a href="#mi-yao-lu-jing-ji-bip44" id="mi-yao-lu-jing-ji-bip44"></a>

通过这种分层（树状结构）推导出来的秘钥，通常用路径来表示，每个级别之间用斜杠 / 来表示，由主私钥衍生出的私钥起始以“m”打头。因此，第一个母密钥生成的子私钥是m/0。第一个公共钥匙是M/0。第一个子密钥的子密钥就是m/0/1，以此类推。

BIP44则是为这个路径约定了一个规范的含义(也扩展了对多币种的支持)，BIP0044指定了包含5个预定义树状层级的结构：\
`m / purpose' / coin' / account' / change / address_index`\
m是固定的, Purpose也是固定的，值为44（或者 0x8000002C）\
**Coin type**\
这个代表的是币种，0代表比特币，1代表比特币测试链，60代表[以太坊](https://learnblockchain.cn/2017/11/20/whatiseth/)\
完整的币种列表地址：[https://github.com/satoshilabs/slips/blob/master/slip-0044.md](https://github.com/satoshilabs/slips/blob/master/slip-0044.md)\
**Account**\
代表这个币的账户索引，从0开始\
**Change**\
常量0用于外部(收款地址)，常量1用于内部（也称为找零地址）。外部用于在钱包外可见的地址（例如，用于接收付款）。内部链用于在钱包外部不可见的地址，用于返回交易变更。 (所以一般使用0)\
**address\_index**\
这就是地址索引，从0开始，代表生成第几个地址，官方建议，每个account下的address\_index不要超过20

根据 [EIP85提议的讨论](https://github.com/ethereum/EIPs/issues/85)以太坊钱包也遵循BIP44标准，确定路径是`m/44'/60'/a'/0/n`\
a 表示帐号，n 是第 n 生成的地址，60 是在 [SLIP44 提案](https://github.com/satoshilabs/slips/blob/master/slip-0044.md)中确定的以太坊的编码。所以我们要开发以太坊钱包同样需要对比特币的钱包提案BIP32、BIP39有所了解。

一句话概括下BIP44就是：**给BIP32的分层路径定义规范**

### BIP39 <a href="#bip39" id="bip39"></a>

BIP32 提案可以让我们保存一个随机数种子（通常16进制数表示），而不是一堆秘钥，确实方便一些，不过用户使用起来(比如冷备份)也比较繁琐，这就出现了[BIP39](https://github.com/bitcoin/bips/blob/master/bip-0039.mediawiki)，它是使用助记词的方式，生成种子的，这样用户只需要记住12（或24）个单词，单词序列通过 PBKDF2 与 HMAC-SHA512 函数创建出随机种子作为 BIP32 的种子。

可以简单的做一个对比，下面那一种备份起来更友好：

```cpp
// 随机数种子
090ABCB3A6e1400e9345bC60c78a8BE7
// 助记词种子
candy maple cake sugar pudding cream honey rich smooth crumble sweet treat
```

使用助记词作为种子其实包含2个部分：助记词生成及助记词推导出随机种子，下面分析下这个过程。

#### 生成助记词 <a href="#sheng-cheng-zhu-ji-ci" id="sheng-cheng-zhu-ji-ci"></a>

助记词生成的过程是这样的：先生成一个128位随机数，再加上对随机数做的校验4位，得到132位的一个数，然后按每11位做切分，这样就有了12个二进制数，然后用每个数去查[BIP39定义的单词表](https://github.com/bitcoin/bips/blob/master/bip-0039/bip-0039-wordlists.md)，这样就得到12个助记词，这个过程图示如下：

![过程图](https://img.learnblockchain.cn/2018/71c0af9474a51296096c3c806ca8f1a1.png!wl/scale/70)\
（图来源于网络）

下面是使用bip39生成生成助记词的一段代码：

```js
var bip39 = require('bip39')
// 生成助记词
var mnemonic = bip39.generateMnemonic()
console.log(mnemonic)

```

#### 助记词推导出种子 <a href="#zhu-ji-ci-tui-dao-chu-zhong-zi" id="zhu-ji-ci-tui-dao-chu-zhong-zi"></a>

这个过程使用密钥拉伸（Key stretching）函数，被用来增强弱密钥的安全性，PBKDF2是常用的密钥拉伸算法中的一种。\
PBKDF2基本原理是通过一个为随机函数(例如 HMAC 函数)，把助记词明文和盐值作为输入参数，然后重复进行运算最终产生生成一个更长的（512 位）密钥种子。这个种子再构建一个确定性钱包并派生出它的密钥。

密钥拉伸函数需要两个参数：助记词和盐。盐可以提高暴力破解的难度。 盐由常量字符串 "mnemonic" 及一个可选的密码组成，注意使用不同密码，则拉伸函数在使用同一个助记词的情况下会产生一个不同的种子，这个过程图示图下:

![过程图](https://img.learnblockchain.cn/2018/d37f78f8f2d859369d99fc5e0a76c184.png!wl/scale/80)\
（图来源于网络）

同样代码来表示一下：

```js
var hdkey = require('ethereumjs-wallet/hdkey')
var util = require('ethereumjs-util')

var seed = bip39.mnemonicToSeed(mnemonic, "pwd");
var hdWallet = hdkey.fromMasterSeed(seed);

var key1 = hdWallet.derivePath("m/44'/60'/0'/0/0");
console.log("私钥："+util.bufferToHex(key1._hdkey._privateKey));

var address1 = util.pubToAddress(key1._hdkey._publicKey, true);
console.log("地址："+util.bufferToHex(address1));
console.log("校验和地址："+ util.toChecksumAddress(address1.toString('hex')));
```

校验和地址是[EIP-55](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-55.md)中定义的对大小写有要求的一种地址形式。

密码可以作为一个额外的安全因子来保护种子，即使助记词的备份被窃取，也可以保证钱包的安全（也要求密码拥有足够的复杂度和长度），不过另外一方面，如果我们忘记密码，那么将无法恢复我们的数字资产。

一句话概括下BIP39就是：**通过定义助记词让种子的备份更友好**

我为大家录制了一个视频：[**以太坊去中心化网页钱包开发**](https://ke.qq.com/course/356068?flowToken=1010359)，从如何创建账号开始，深入探索BIP32、BIP44、BIP39等提案，以及如何存储私钥、发送离线签名交易和Token。

### 小结 <a href="#xiao-jie" id="xiao-jie"></a>

HD钱包（Hierarchical Deterministic Wallets）是在BIP32中提出的为了避免管理一堆私钥的麻烦提出的分层推导方案。\
而BIP44是给BIP32的分层增强了路径定义规范，同时增加了对多币种的支持。\
BIP39则通过定义助记词让种子的备份更友好。

目前我们的市面上单到的以太币、比特币钱包基本都遵循这些标准。

最后推荐一个[Chaintool 助记词账号生成](https://chaintool.tech/generateWallet)
