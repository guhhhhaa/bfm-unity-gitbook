# What Is the Relative-value Trading Strategy?

[Skip to content](https://www.antrade.io/guide/docs/en/strategy\_relative-value/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/en/)[Free AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/en)
* [Strategy](https://www.antrade.io/guide/docs/en/en-strategies/)
* [What Is the Relative-value Trading Strategy?](https://www.antrade.io/guide/docs/en/strategy\_relative-value/)

Search for:

STRATEGY

*
  * [What Is the Infinity Grid Trading Strategy?](https://www.antrade.io/guide/docs/en/infinity\_grid/)
  * [What is the Regular Investment Strategy?](https://www.antrade.io/guide/docs/en/regular\_investment/)
  * [What is the Formation Trading Strategy?](https://www.antrade.io/guide/docs/en/strategy\_formation/)
  * [What Is the Momentum Trading Strategy?](https://www.antrade.io/guide/docs/en/strategy-momentum/)
  * [What Is the D-KAMA Trading Strategy?](https://www.antrade.io/guide/docs/en/strategy\_d-kama/)
  * [What Is the R-Breaker Trading Strategy?](https://www.antrade.io/guide/docs/en/strategy\_r-breaker/)
  * [What Is the SuperTrend Trading Strategy?](https://www.antrade.io/guide/docs/en/strategy\_supertrend/)
  * [What Is the Relative-value Trading Strategy?](https://www.antrade.io/guide/docs/en/strategy\_relative-value/)
  * [What Is the Classic Grid Trading Strategy?](https://www.antrade.io/guide/docs/en/strategy\_grid/)
  * [What Is the DCA Trading Strategy?](https://www.antrade.io/guide/docs/en/strategy\_dca/)
  * [What Is the AI Grid Trading Strategy?](https://www.antrade.io/guide/docs/en/en\_strategy\_grid\_ai/)
  * [What Is the AI Beta Trading Strategy?](https://www.antrade.io/guide/docs/en/strategy\_ai\_beta/)
  * [What Is the Rebalancing Trading Strategy?](https://www.antrade.io/guide/docs/en/strategy\_rebalancing/)
  * [What Is the AI Dual Grid Trading Strategy?](https://www.antrade.io/guide/docs/en/strategy\_dual\_grid/)

## What Is the Relative-value Trading Strategy?

4 months ago[AntBot](https://www.antrade.io/guide/docs/en/author/antbot/)8 minutes

**Contents:**

* [**What is the Relative-value strategy?**](https://www.antrade.io/guide/docs/en/strategy\_relative-value/#WhatistheRelative-valuestrategy?)\

* [**How to configure a crypto portfolio in the Relative-value strategy?**](https://www.antrade.io/guide/docs/en/strategy\_relative-value/#HowtoconfigureacryptoportfoliointheRelative-valuestrategy?)\

* [**How to start a bot with the Relative-value strategy?**](https://www.antrade.io/guide/docs/en/strategy\_relative-value/#HowtostartabotwiththeRelative-valuestrategy?)\

* [**Advantages and risks of the Relative-value strategy**](https://www.antrade.io/guide/docs/en/strategy\_relative-value/#AdvantagesandrisksoftheRelative-valuestrategy)\

* [**The Relative-value strategy optimization method**](https://www.antrade.io/guide/docs/en/strategy\_relative-value/#TheRelative-valuestrategyoptimizationmethod)

**What is the Relative-value strategy?**

The essence of the Relative-value strategy is **arbitrage**, which is to use the **pricing difference** between **associated assets** to establish **long** and **short** positions to arbitrage the **profit**s of **spread** that the pricing returns to normal.

The basic principle is that the market’s pricing of certain assets is distorted due to special reasons. When the value of one asset is overvalued and another related asset is undervalued, they can be bought the undervalued asset and sold the overvalued asset until the price of the two tends to converge and close position, so as to obtain the profit from the spread.

Relative-value strategy is a good asset allocation variety. Adding it to a crypto portfolio (i.e., a crypto pair) can better improve the overall risk-adjusted profit while reducing the volatility of the crypto pair. **Not only does it meet the needs of the prudent investor, it better meets the asset allocation needs of investors of all risk preference types.**

\
**How to configure a crypto portfolio in the Relative-value strategy?**

When the prices of two related cryptos diverge, the Relative-value strategy works in large part by capturing their relative value differentials.

In general, a pair of cryptos that have a relatively stable spread relationship in price over time is first captured. As the spread between the associated cryptos gets wider, or as they get smaller, and then the relationship breaks down or deviates from the usual range, then the magnitude of the change creates relative value opportunities.

Relative-value strategy bot arbitrages by buying one cryptocurrency and selling another at the same time when the price of the cryptos has exceeded its historical range or when the price tends to converge.

<figure><img src="https://antrade.io/guide/docs/en/wp-content/uploads/2022/11/%E5%8E%9F%E7%90%86%E5%9B%BE2.jpg" alt=""><figcaption></figcaption></figure>

<figure><img src="https://antrade.io/guide/docs/en/wp-content/uploads/2022/11/%E5%8E%9F%E7%90%86%E5%9B%BE1.jpg" alt=""><figcaption></figcaption></figure>

Based on the arbitrage nature of the Relative-value strategy, arbitrage opportunities in cryptos mainly exist in the following contexts:

* The first is to compare projects of the same blockchain, allowing investors to arbitrage at the protocol or industry level, but to avoid those public chains that may affect performance because of technical differences.
* The second is to compare the same type of projects on different public chains. There are two different potential goals here: first, similar projects across public chains, which is based on the following judgment – that is, one chain has a comparative advantage over another chain in this application field, which often leads to that protocol performing better than its counterpart on another chain, even if they have similar fundamentals. Second, due to the open-source nature of cryptos, some projects are often “forked”, resulting in completely different project teams operating the same codebase, and project teams, upgradeability, or other specificity factors are a project’s protective shield, there is an arbitrage pricing differentials opportunity.
* The final approach is to compare blockchains from the ground up, around throughput, scalability, user(project) uptake of the public chain, etc. Since the comparison of public chains usually has many different angles, it is recommended that you do some supplementary reading on PoS verification, security, and staking.

AntBot divides cryptos into different sections based on the analysis of the above three aspects, and also provides crypto pairs with the most similar properties for traders’ reference.

<figure><img src="https://antrade.io/guide/docs/en/wp-content/uploads/2022/11/7857e1f072955a9598204329eb69ce2.jpg" alt=""><figcaption></figcaption></figure>

**How to start a bot with the Relative-value strategy？**

1\. Log into your AntBot account to find the **\[Relative-value]** in the **\[Robot]** of the **\[Trades]** interface and click the button on the right to enter the parameter setting page.

2\. Choose a **crypto pair** based on personal criteria and preferences.

3\. Select **\[Long/Short ], \[Short /Long]** or **\[Shock]**. Here take \[ETH/BTC] for example.

* **\[Short/Long]**: Profit will be made when ETH is up more than BTC or BTC is down more than ETH.
* **\[Long/Short]**: Profit will be made when ETH is bigger than BTC’s drop or BTC is bigger than ETH’s rise.
* **\[Shock]**: Profit in all the above four cases.

4\. Set **\[Initial Positions]**, **\[Leverage]**, **\[Risk Level]**, **\[Running Mode]**, and **\[Max Order]**.

* **\[Initial Positions]**: The position amount of the robot’s first open position. Beginners are advised to keep the default values.
* **\[Leverage]**: Using leverage can be regarded as borrowing funds from the exchange to hold positions. The multiple of this position funds relative to the principal is the leverage, and increasing leverage will magnify profits and losses. It is recommended to keep the default value of 5x leverage for beginners.
* **\[Risk Level]**: The greater the risk, the greater the price gap and take-profit percentage when adding positions, and the risk level is radical > steady > conserved.&#x20;
* **\[Running Mode]**: It is divided into cycle and single. Cycle means that the robot will repeat the next round of opening positions after each take-profit and closing position, and the robot will only stop when it reaches the profit or loss conditions preset in the \[Optional]. Single means that the robot will automatically terminate the operation after completing a cross-position take profit.
* **\[Max Order]**: The maximum number that bots are allowed to increase positions consecutively from the state of unopened position.

5\. If you want to use the parameters recommended by the system, then you can turn on **\[Smart Mode]**. If you’re going to set them by yourself, then you can fill in the **\[Size Multiple]**, **\[Price gap]**, and **\[Take-Profit]**.

* **\[Smart Mode]**: The parameters of Size Multiple, Price Gap, and Take-Profit cannot be manually modified after turning on Smart Mode. The cloud AI algorithm will monitor market volatility and adjust the parameters in real-time.
* **\[Size Multiple]**: Taking the last open position as the base multiplied by Size Multiple equals the current follow-up investment.
* **\[Price gap**(%)**]**: Taking the last opening price as a reference, the position will be increased if the market price rises or falls by this preset ratio.
* **\[Take-Profit**(%)**]**: When the return on invested assets reaches this preset value, the position will be closed and the robot will enter the next cycle.

6\. Optionally fill in the **\[Profit]** and **\[Loss]**.

* **\[Profit]**:
  * **Take-profit by Amount**: When PnL + Floating-PnL > the preset amount, the robot will automatically close its positions and stop.
* **\[Loss]**:
  * **Stop-Loss by Amount**: When Floating-Loss amount > the preset amount, the robot will automatically close its positions and stop.

7\. Click **\[Launch]** to successfully create a Relative-value robot.

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2022/12/%E6%9C%AA%E6%A0%87%E9%A2%98-3.jpg" alt=""><figcaption></figcaption></figure>

**Advantages and risks of the Relative-value strategy**

**Advantages:**

**1. Low market correlation**

The Relative-value strategy does not do directional trading in the crypto market, does not predict the rises and falls of the market prices, focuses on the spread in price differences, and holds long and short positions at the same time, which has a low degree of correlation with the market.

**2. Low volatility**

The price difference between related crypto-assets is usually relatively small, and the Relative-value strategy is more robust than other strategies. Adding the Relative-value strategy to crypto asset allocation can effectively diversify risks and reduce the volatility of crypto asset portfolios. If leverage is not used, after deducting related transaction costs, most of them will experience relatively stable growth, and the income of this strategy will not appear to explosive growth.

**3. Suitable for the volatile market**

The Relative-value strategy and trend strategy form natural complementary advantages and are more suitable for volatile market conditions. From the perspective of market adaptability, the Relative-value strategy captures the fluctuation of the relevant cryptos price difference, while the trend strategy faces the risk of repeated stop loss in the volatile market. Therefore, the Relative-value strategy is outstanding in the volatile market.

**Risk:**

Mainly from the risk of convergence shock, the so-called convergence shock refers to the situation in which the price trend of the associated crypto assets does not converge due to some special reasons. Since the Relative-value strategy makes use of the high probability that the associated crypto assets tend to converge to make profits. If the direction deviates, a small probability event occurs, and the spread cannot converge which is resulting in losses. In addition, in order to obtain higher returns, the Relative-value strategy will enlarge the leverage. If the leverage multiple is too high, when occurs a small probability event, there may also be a large loss.\
In order to reduce the impact of convergence shock, it is necessary to diversify strategies among crypto assets. If there are only one or similar strategies, it may be fatal when losses occur, but in the case of a combination of multiple strategies, when a certain strategy is at risk, the effect of the combination will not be too great.

**The Relative-value strategy optimization method**

After the Relative-value strategy is optimized, it provides dual arbitrage, when the spread is getting bigger and bigger and the spread is getting smaller and smaller, the Relative-value robot can both obtain the profit from the spread by establishing long and short positions. Two Relative-value robots are activated for the same crypto pair at the same time. At this time, one robot chooses divergence(Long/Short) and the other robot chooses convergence(Short/Long), which can double the income.

References :

[https://www.crystalfunds.com/insights/relative-value-hedge-funds](https://www.crystalfunds.com/insights/relative-value-hedge-funds)

[https://www.barclayhedge.com/insider/hedge-fund-strategy-relative-value-arbitrage](https://www.barclayhedge.com/insider/hedge-fund-strategy-relative-value-arbitrage)

[https://www.hfr.com/hfr-hedge-fund-strategy-definitions-relative-value](https://www.hfr.com/hfr-hedge-fund-strategy-definitions-relative-value)

[https://thebusinessprofessor.com/en\_US/investments-trading-financial-markets/capital-structure-arbitrage-definition](https://thebusinessprofessor.com/en\_US/investments-trading-financial-markets/capital-structure-arbitrage-definition)

[#AntBot](https://www.antrade.io/guide/docs/en/tag/antbot/)[#bot](https://www.antrade.io/guide/docs/en/tag/bot/)[#Relative-value](https://www.antrade.io/guide/docs/en/tag/relative-value/)[#strategy](https://www.antrade.io/guide/docs/en/tag/strategy/)@AntBot free trading bot\
