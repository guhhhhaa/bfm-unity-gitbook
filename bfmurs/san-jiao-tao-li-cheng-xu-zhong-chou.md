# 三角套利程序众筹

## 众筹声明

[https://github.com/zlq4863947/triangular-arbitrage2](https://github.com/zlq4863947/triangular-arbitrage2) 

这个是大神的Github地址。

![](../.gitbook/assets/image%20%2841%29.png)

需要找24个人，每人出500，体验一个三角套利程序，然后众筹成功，我拿2000，大神拿10000，我负责承担风险和大神沟通，并保证会指导所有使用者使用三角套利程序。如果程序可以稳定盈利，Ellite大神会额外获得2000元等值的群荣誉代币——BFM代币，BFM代币可在PancakeSwap兑换为BNB

![](../.gitbook/assets/a3f955270ba357c39d29a9106ba641f1.jpg)

谁想参与众筹三角套利程序?事先说明，Ellite大神拥有5年以上开发经验，而且精通各种技术，我认为中国找不到第二个Ellite大神。

众筹期2个月。打U到这个ID，然后我会和Ellite大神交涉，如果大神交付成功，我会转给他，如果交付失败，我不会转给他，会退回到你们的支付地址。

或者你们也可以考虑自己直接和Ellite大神沟通，上面有Ellite大神的支付ID  如果众筹失败，我会转给Ellite大神价值1000元人民币的USDT，并赠送价值1000元人民币的BFM代币，但是条件是要保证大神留在这个群（QQ群：708912525），接受我们的膜拜。 

众筹期，2021年9月17日到2021年11月17日。

## 内容

## triangular-arbitrage2

[![triangular-arbitrage2 Logo](https://github.com/zlq4863947/triangular-arbitrage2/raw/main/assets/images/logo.svg)](https://github.com/zlq4863947/triangular-arbitrage2)

开源的自动化三角套利交易程序。

前一版本程序地址: [https://github.com/zlq4863947/triangular-arbitrage](https://github.com/zlq4863947/triangular-arbitrage)

[see the English](https://github.com/zlq4863947/triangular-arbitrage2/blob/main/README_EN.md)

### 技术架构

* 开发语言: [typescript](https://github.com/microsoft/TypeScript)
* 技术库: [rxjs](https://github.com/ReactiveX/rxjs) 、[nestjs](https://github.com/nestjs/nest)
* 数字货币相关库: [ccxt](https://github.com/ccxt/ccxt) 、[binance](https://github.com/tiagosiebler/binance)
* 测试库: [jest](https://github.com/facebook/jest)
* 虚拟环境容器: docker
* 数据库: mysql 8.0
* 依赖管理工具: [yarn](https://github.com/yarnpkg/yarn) （不是npm）

### 免责声明

* `triangular-arbitrage2` 不是万无一失、百分之百、一定盈利交易机器人。需要您自行担风险使用它。
* 数字货币仍处于萌芽实验阶段，`triangular-arbitrage2`也是如此。这意味着，两种都可能随时失败。
* `triangular-arbitrage2`分为 `Basic`\(免费版\) 和 `Pro`\(付费版\)。
  * `Basic`\(免费版\)，没有真实交易功能，您需要自行增加此功能，并承担由此产生的风险。
  * `Pro`\(付费版\)，本人负责保证和维护此机器人的策略及交易的准确无误，不保证百分比盈利，交易产生的风险需自行承担。
* 切勿让机器人长时间不受监控。 `triangular-arbitrage2` 并不知道什么时候需要停止，所以如果发生太多损失或出现问题，请准备好停止它。

### 机器人说明

|  | Basic\(免费版\) | Pro\(付费版\) |
| :--- | :--- | :--- |
| 开源 | ○ | △ |
| 命令行应用 | ○ | ○ |
| 支持的交易所 | 1（币安） | 1+n \(币安+其他交易所\) |
| 多种类日志记录 | ○ | ○ |
| 自动计算交易费率 | ○ | ○ |
| 模拟交易 | ○ | ○ |
| 真实交易 | × | ○ |
| 收益报表 | × | ○ |
| 多种执行策略 | × | ○ |
| 维护与支援 | github论坛 | 实时 |

* 付费版可通过以下方式联系咨询
  * email: [zlq4863947@gmail.com](mailto:zlq4863947@gmail.com)
  * qq: 442540141

### 快速开始

#### 1，环境安装

* 安装nodejs（最新版就可以）
* 执行 `npm install` （安装程序依赖）

#### 2、设置配置文件

* **config/default.sample.toml**更改为**config/default.toml**
* 自己修改成想要的配置，例如:币安的apikey

#### 3、启动命令行机器人

**免费版命令行应用**

* `npm run start:cli`

**付费版命令行应用**

* `npm run start:pro-cli`（需求提前安装docker）

### 捐赠

程序开发不易，需要大量的时间和精力。如果有人为开发捐款，我将非常感谢。

#### BTC

`1J3hX6en3147VtEJvS2WbFrJ1emNcfcTdz`

#### ETH

`0x8bb4a5f034B4822E0D1B51f4E07ce1eee7Bc8D8C`

### License: GPL3

