# What Is the Infinity Grid Trading Strategy?

[Skip to content](https://www.antrade.io/guide/docs/en/infinity\_grid/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/en/)[Free AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/en)
* [Strategy](https://www.antrade.io/guide/docs/en/en-strategies/)
* [What Is the Infinity Grid Trading Strategy?](https://www.antrade.io/guide/docs/en/infinity\_grid/)

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

## What Is the Infinity Grid Trading Strategy?

2 months ago[AntBot](https://www.antrade.io/guide/docs/en/author/antbot/)6 minutes

**Contents**:

* [What is the Infinity Grid trading strategy?](https://www.antrade.io/guide/docs/en/infinity\_grid/#What-is-the-Infinity-Grid-trading-strategy?)\

* [Trading principle of the Infinite Grid strategy](https://www.antrade.io/guide/docs/en/infinity\_grid/#Trading-principle-of-the-Infinite-Grid-strategy)\

* [Features of AntBot Infinity Grid](https://www.antrade.io/guide/docs/en/infinity\_grid/#Features-of-AntBot-Infinity-Grid)\

* [How to reduce the risk of Infinite Grid?](https://www.antrade.io/guide/docs/en/infinity\_grid/#How-to-reduce-the-risk-of-Infinite-Grid?)\

* [How to start an Infinite Grid robot?](https://www.antrade.io/guide/docs/en/infinity\_grid/#How-to-start-an-Infinite-Grid-robot?)\

* [Advantages and Disadvantages](https://www.antrade.io/guide/docs/en/infinity\_grid/#Advantages:)

#### What is the Infinity Grid trading strategy? <a href="#what-is-the-infinity-grid-trading-strategy" id="what-is-the-infinity-grid-trading-strategy"></a>

**The Infinite Grid trading strategy is a spot trading strategy optimized for oscillatory rising markets.** No matter how much the price rises, there will always be a part of the asset that can be sold for profit, which perfectly avoids the situation that there are no holding assets to sell when the market continues to rise. In a market that fluctuates and upwards, the infinite grid will only sell the “profit” after the asset appreciates, ensuring that the trader always has the same value as the initial positions. **As long as this asset keeps oscillating and increasing, you can use the infinite grid to not only earn oscillating profits but also get unilateral upward trend profits.**

#### Trading principle of the Infinite Grid strategy <a href="#trading-principle-of-the-infinite-grid-strategy" id="trading-principle-of-the-infinite-grid-strategy"></a>

AntBot’s Infinite Grid is very simple, which is to keep your spot at a certain amount.

For example, suppose you create an Infinite Grid of BTC for 1,000 USDT. Buy 500 USDT worth of BTC at the current price and keep the remaining 500 USDT. Assume that a single grid is set at 10%. (Regardless of fees)

If the value of BTC rises by 10% to reach 550 USDT, sell 50 USDT of BTC. At this time, 500 USDT of BTC and 550 USDT are held. Of this, 50 USDT is the grid profit, and a part of BTC will be sold for each transaction. USDT increases after selling, and so does the total profit.

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2023/01/up@2x.jpg" alt=""><figcaption></figcaption></figure>

If the value of BTC drops 10% to 450 USDT, take out the reserved 50 USDT to buy BTC, so that BTC remains at 500 USDT. At this point, the overall value becomes 950 USDT, the amount of USDT decreases, and the amount of BTC increases. The total profit is reduced by 50 USDT.

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2023/01/down@2x.jpg" alt=""><figcaption></figcaption></figure>

Since the value of BTC has been maintained at 500 USDT, as long as its price does not return to zero, then the grid can cycle to buy low and sell high to produce grid profits, called Infinite Grid.

#### Features of AntBot’s Infinity Grid <a href="#features-of-antbot-infinity-grid" id="features-of-antbot-infinity-grid"></a>

* **First of all, AntBot’s Infinite Grid strategy only supports spot robots.**\

* **The system default sets the grid interval based on the asset** **volatility (the grid interval can be as low as 0.25%).**\

* **AntBot’s Infinity Grid supports small funds initiation of the robot. For example, the Infinity Grid robot can be activated with 200 USDT.**\

* **The robot automatically finds the recent support of the asset as the lowest limit price (Price Floor) to achieve the best risk-reward ratio. (To reduce risk, the purchase of assets is stopped when the price is lower than this price.)**

#### How to reduce the risk of Infinite Grid? <a href="#how-to-reduce-the-risk-of-infinite-grid" id="how-to-reduce-the-risk-of-infinite-grid"></a>

When the price falls for a long time, it will still cause floating losses. Because when the price continues to drop, the system will constantly help you buy the coin to maintain the total value of the assets in your hand, then the funds will be continuously consumed, and there will be a large floating loss. **Therefore, before opening the Infinite Grid robot, you should choose a crypto that is optimistic about the expected future growth in the long term, and reasonably set the price floor of the Infinite Grid operation according to your own capital situation to reduce the risk,** and you can also set take-profit and stop-loss as the appearance conditions of the robot.

#### How to start an Infinite Grid robot? <a href="#how-to-start-an-infinite-grid-robot" id="how-to-start-an-infinite-grid-robot"></a>

1\. Log into your AntBot account to find **\[Infinite** **Grid]** in the **\[Robot]** of the **\[Trades]** interface and **click** the button on the right to enter the parameter setting page.

2\. Choose **crypto** based on personal criteria and preferences.

3\. Fill in the detailed parameters. The following parameters may help you.

* **\[Grid Interval]:** The profit per grid.
* **\[Max Positions]:** The amount of funds you plan to put into the bot. There is a minimum investment amount due to the minimum trading volume requirement for each crypto.
* **\[Price Floor]:** When the price is lower than the preset price, the robots will not open but only close their positions until the price rises back to the preset price. It is possible that this is a time when a significant decline is taking place and it is not advisable to buy too much. Also, avoid spending all your remaining funds.

Take-profit

* **Take Profit by Price:** If the latest price is higher than the preset price, the long robot will automatically close the position and stop working. And if the latest price is lower than the preset price, the short robot will automatically close the position and stop working.
* **Take-Profit by Amount:** When PnL + Floating > the preset amount, the robot will close all its positions and stop.

Stop-loss

* **Stop Loss by Price:** If the latest price is lower than the preset price, the long robot will automatically close the position and stop working. And if the latest price is higher than the preset price, the short robot will automatically close the position and stop working.
* **Stop-Loss by Amount:** When PnL + Floating < -the preset amount, the robot will close all its positions and stop.

4\. Click **\[Launch]** to successfully create an Infinite Grid robot.

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2023/01/%E6%9C%AA%E6%A0%87%E9%A2%98-4@2x.jpg" alt=""><figcaption></figcaption></figure>

**Advantages:**

1\. Because of market volatility, the total profit obtained by the Infinite Grid robot is much higher than that of holding spot assets.

2\. It is suitable for long-term investment and will not stop trading if it exceeds the price range like the [Classic Grid](https://www.antrade.io/guide/docs/en/strategy\_grid/) trading. The Infinite Grid will be more suitable for long-term investment than the Classic Grid trading.

3\. It is a grid-based trading method that ignores price ranges. As long as the price fluctuations reach the grid interval set by the strategy, it can constantly sell high and buy low to arbitrage profits.

4\. No matter how the price rises or falls, Infinity Grid always holds the equivalent value of crypto assets.

5\. No matter how high the price ups, there will always be assets that cannot be sold out, and even if the final price increases ten thousand times, there will still be some left to sell, as there is no single trade in the process that sells it all.

6\. It is suitable for holding a trading pair for a long time, such as BTC/USDT, ETH/USDT, etc.

**Disadvantages:**

1\. There is no price range for Infinite Grid trading, so there will be funds in an idle state. Compared to the Classic Grid, the Infinite Grid has a lower utilization rate of funds. It is difficult to see high profits in the short term.

2\. The investment amount is relatively large. The Infinite Grid does not have a price ceiling, and the trading range is wider. So a larger amount of funds is required to ensure smooth trading.

[#AntBot](https://www.antrade.io/guide/docs/en/tag/antbot/)[#Infinity Grid](https://www.antrade.io/guide/docs/en/tag/infinity-grid/)[#strategy](https://www.antrade.io/guide/docs/en/tag/strategy/)@AntBot free trading bot\
