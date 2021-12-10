# Cross-Chain Bridge

{% hint style="info" %}
二层协议：

* ****[**Arbitrum Bridge**](https://bridge.arbitrum.io)****
* [**Optimism Bridge**](https://gateway.optimism.io)
* ****[**Polygon Bridge**](https://wallet.polygon.technology/bridge)****

第三方桥：

* [**cBridge**](https://cbridge.celer.network)（♻️ ETH；Arbitrum；Optimism；Polygon；BSC）
* [**Hop Protocol**](https://app.hop.exchange)（♻️ ETH；Arbitrum；Optimism；Polygon）
* [**DeGate**](https://bridge.degate.com)（ETH <> Arbitrum）
* ****[**RenBridge**](https://bridge.renproject.io/mint)**（**BTC <> Arbitrum）
* ****[**Anyswap**](https://anyswap.exchange/dashboard)**（**ETH <> Arbitrum）
* [**Allbridge**](https://app.allbridge.io)（sol↔erc20↔heco↔polygon↔bsc）

一层公链：

* [**Binance Bridge**](http://binance.org/en/bridge)****
* ****[**Solana Wormhole Bridge**](zhi-hui-shi-kua-lian-qiao.md#can-kao)****
* ****[**Fantom Anyswap Bridge**](https://ftm.anyswap.exchange/bridge)****
* [**Avalanche Bridge**](https://bridge.avax.network/login)
* [**Near Rainbow Bridge**](https://ethereum.bridgetonear.org)
{% endhint %}

## 参考

* [从以太坊迁徙到热门L1\&L2，这些跨链桥你必须知道](https://www.163.com/dy/article/GJQ1V4CG0514832I.html)
* [相比以太坊 L2 官方跨链桥，第三方桥便宜好用吗？](https://www.8btc.com/article/6689730)
* [Celer cBridge操作指南：手把手教你如何完成Layer2跨链](https://www.8btc.com/article/6688136)
* [干货 | 迎接Layer 2夏天，这些工具你得提前准备](https://www.8btc.com/article/6687854)
* [收藏！一文了解跨链桥设计类型及项目分布](https://www.8btc.com/article/6683702)

| 工具                    | 网址                                                                                                                                                               | 简介                                                                                                             |
| --------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| 抹茶和gate等交易所           |                                                                                                                                                                  | 普通用户跨链首选中心化交易所，个人用的最多的是抹茶和gate，他俩支持多链usdt\&usdc的充提币，充提币之前一定要再三确认好目标地址和链。但要明白交易所的资产跨链最终也是用的下面的这些去中心化跨链工具。       |
| allbridge             | [app.allbridge.io](https://www.google.com/url?q=http://app.allbridge.io/\&sa=D\&source=editors\&ust=1631629363816000\&usg=AOvVaw2jHYnwg3ZQ1JNsAUiUnUSi)          | 支持sol↔erc20↔heco↔polygon↔bsc 六月刚推出的跨链桥，有matic和solana官方背书，往sol跨资产首选去中心化桥。                                       |
| Binance官方桥            | [binance.org/en/bridge](https://www.google.com/url?q=http://binance.org/en/bridge\&sa=D\&source=editors\&ust=1631629363816000\&usg=AOvVaw0BZg4ar52SQCUToeoGsH8T) | 支持bsc↔erc20↔trx，用过多次，非常好用，eth和bsc之间跨链首选桥。                                                                      |
| 麦子钱包带的跨链              | [xpollinate.io](https://www.google.com/url?q=http://xpollinate.io\&sa=D\&source=editors\&ust=1631629363817000\&usg=AOvVaw3CJGiJgQLKtZxBmGUjucOS)                 | 支持bsc↔matic↔ftm↔xdai，比较不错，也会遇到流动性不足，如果是usdc的话建议试一下用1inch换成usdt或者dai再跨。我一般bsc和matic之间跨链就用这个，手续费万分之五，速度比较快。      |
| evodefi               | [bridge.evodefi.com](https://www.google.com/url?q=http://bridge.evodefi.com\&sa=D\&source=editors\&ust=1631629363817000\&usg=AOvVaw1ysB0GNJaIUVQIjWtf1B7o)       | 支持bsc↔ftm↔heco↔hsc↔eth 这个我没咋用，好像是手续fee比较高（千分之五）                                                                |
| 一个跨链版的1inch           | li.finance/swap                                                                                                                                                  | 可以直接实现bsc↔matic↔xdai三条链上的token直接swap功能，项目处于beta阶段，可能会出现问题。                                                     |
| Anyswap               | anyswap.exchange/swap                                                                                                                                            | 跨链界最强王者：支持erc20,bsc,fsn,matic,ftm,xdai等其他乱七八糟小链的互跨，去中心化程度高，使用难度和门槛较高，有时会有链间流动性不足的问题。                           |
| Xdai跨链                | [bridge.xdaichain.com](https://www.google.com/url?q=http://bridge.xdaichain.com\&sa=D\&source=editors\&ust=1631629363817000\&usg=AOvVaw0DxwDuiEy7Yeu3UWF85H7x)   | xdai↔erc20 xdai官方桥。                                                                                            |
| Fantom跨链              | multichain.xyz                                                                                                                                                   | ftm↔erc20 主要都用这个，手续fee比较高。这个你在他网站上找不到任何联系方式，但他好像是跟anyswap一家的，出了事可以去找anyswap维权。                                 |
| matic的官方桥             | wallet.matic.network/login/                                                                                                                                      | matic↔erc20 注意：从erc20跨到matic上面只需要不到十分钟和少量eth手续费，但是从matic上面跨到erc20上面一定要注意看出现的提示，有需要几分钟的，有需要三小时的，跨matic币就需要最多7天。 |
| wbtc官网                | wbtc.network/dashboard/partners                                                                                                                                  | 冰糖橙跨链到以太坊上推荐大家使用wbtc官网上面的工具wrap成WBTC。                                                                          |
| tp钱包的闪兑：Xswap         |                                                                                                                                                                  | 支持eth↔bsc↔heco↔trx↔matic↔oec↔ftm↔eos↔hsc↔btc↔dot↔ksm↔lost这么多链的互跨，功能有点强大。                                       |
| cbridge.celer.network | cbridge.celer.network                                                                                                                                            | 7月新出的跨链桥，支持eth↔bsc↔matic↔xdai↔arbitrum互跨，手续费很低。                                                                |
| 跨链桥                   | [https://www.cointofu.com/cross-chain-bridge](https://www.cointofu.com/cross-chain-bridge)                                                                       | 只要选你想把资金从哪个链转去哪个链，就会自动输出对应的结果                                                                                  |
