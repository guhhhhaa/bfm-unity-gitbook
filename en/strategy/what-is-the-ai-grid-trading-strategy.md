# What Is the AI Grid Trading Strategy?

[Skip to content](https://www.antrade.io/guide/docs/en/en\_strategy\_grid\_ai/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/en/)[Free AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/en)
* [Strategy](https://www.antrade.io/guide/docs/en/en-strategies/)
* [What Is the AI Grid Trading Strategy?](https://www.antrade.io/guide/docs/en/en\_strategy\_grid\_ai/)

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

## What Is the AI Grid Trading Strategy?

5 months ago[AntBot](https://www.antrade.io/guide/docs/en/author/antbot/)9 minutes

**Contents：**

* [**What is the AI Grid Trading Strategy?**](https://www.antrade.io/guide/docs/en/en\_strategy\_grid\_ai/#cc6h2k)\

* [**Profitability of AI grid strategy**](https://www.antrade.io/guide/docs/en/en\_strategy\_grid\_ai/#fqiguh)\

* [**Profitability of dual grid**](https://www.antrade.io/guide/docs/en/en\_strategy\_grid\_ai/#8sit9u)\

* [**What problem does the dual grid strategy solve?**](https://www.antrade.io/guide/docs/en/en\_strategy\_grid\_ai/#What1)\

* [**The characteristics of AntBot’s dual grid**](https://www.antrade.io/guide/docs/en/en\_strategy\_grid\_ai/#characteristics)\

* [**Introduction to Parameter**](https://www.antrade.io/guide/docs/en/en\_strategy\_grid\_ai/#8yigtw)\

* [**Take-Profit and Stop-Loss**](https://www.antrade.io/guide/docs/en/en\_strategy\_grid\_ai/#7g3xto)\

* [**How to start a bot of AI Grid?**](https://www.antrade.io/guide/docs/en/en\_strategy\_grid\_ai/#2scltn)\

* [**Pros and Cons of AI Dual Grid**](https://www.antrade.io/guide/docs/en/en\_strategy\_grid\_ai/#Pros-and-cons)

**What is the AI Grid Trading Strategy?**

The AI Grid Trading Strategy is an oscillating trading strategy deeply optimized by the AntBot team based on the classic grid strategy for the return/risk ratio. Both spot and futures can be traded using AI gird strategy.

The AI grid strategy is an automated strategy that executes buying low and selling high in a specific price range. You only need to set the highest price and lowest price in the range, determine the number of grids to be subdivided, and start running the strategy. The strategy calculates the price of each small grid to buy low and sell high, automatically placing orders, and continuously absorbing low and sell high to earn the profit brought by volatility as the market fluctuates.

**Profitability of AI grid strategy**

By setting the price range, the robot will divide the funds into many parts, buy one if the price falls by one grid, then place a sell order that is one grid higher than the buying price, and sell when the price rises to this grid. Each time the selling price is a little higher than the buying price. If it keeps falling, keep buying until the lower limit of the range; If it keeps rising, keep selling until the upper limit of the range. If the price goes up or down, buy low and sell high. In this way, with market fluctuations and cyclic placing orders and transactions, you can continue to earn fluctuation gains in the volatile market.

<figure><img src="https://antrade.io/guide/docs/en/wp-content/uploads/2022/10/What-is-the-AI-Grid-Trading-Strategy.png" alt=""><figcaption></figcaption></figure>

**Profitability of dual grid**

The dual grid strategy is a futures grid strategy that can go long and short at the same time for volatile markets. It is a strategy extended from AntBot’s spot AI grid, which can be seen as two AI grid robots running independently with 5x leverage in opposite directions.

When the grid position of the long robot reaches the take-profit ratio and closes the position, the short robot will buy a short position at the same price as the take-profit price of the long robot, so that whenever one grid generates profits in the direction of the current trend, the other grid takes loses, and vice versa. This is the dual grid operation feature.

In this case, each side of the grid should have its own profit and stop-loss. In the fluctuating market, the trades of the two sides are independently managed to achieve profit locking.

This is how the dual grid profit. The two-way grid strategy helps to reach total profit targets faster and minimize drawdowns.\
As shown below:

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2022/12/double_grid_setup.webp" alt=""><figcaption></figcaption></figure>

**What problem does the dual grid strategy solve?**

The dual grid is one of the original strategies of the AntBot team. It perfectly solves the three major problems of the classic grid strategy.

**1. No profit is generated beyond the grid interval.**\
The dual grid runs the robot in both long and short at the same time, and profits will be generated regardless of whether the price rises or falls.

**2. Low fund efficiency.**\
The unilateral grid encounters a continuous reverse market, continues to invest funds to increase positions, and can only wait for the price to return to profit before it can generate profits.\
The dual grid runs the long and short robots of the same futures asset at the same time. If the price continues to fall, the long robot increases positions, the short robot will continue to close the position to take profit at this time. On the contrary, if the price continues to rise, the short robot increases the position, and the long robot will continue to close the positions to take profits at this time. At the same time, you only need to prepare one piece of funds to increase the position of the robot in one direction, and take one margin risk and get two profit returns.\
In addition, AntBot’s dual grid strategy will develop its own grid range according to the support resistance level and volatility of different targets, balancing the risk and return ratio.

**3. After breaking the price range (the net), it cannot be automatically adjusted in time.**\
AntBot’s dual grid has no upper and lower price, after breaking through the grid on one side, the AI system will recalculate the support and resistance level, invest the initial position again, and track the market profit one by one when the price continues to be unilateral.

**The characteristics of AntBot’s dual grid**

1\. There is no limit order, and the margin is shared to prevent liquidation.

2\. The take profit of each grid is independently calculated and executed, and the profit is divided to improve the liquidity of funds.

3\. Two independent long and short grids are considered two separate systems because both have clear profit and selling boundaries.

4\. There is a difference in the PnL display in the trading records of AntBot and the exchange, because AntBot calculates the PnL of the grid according to the opening price and closing price of each grid, while the exchange calculates the PnL of each order based on the average price of the position.

**Introduction to Parameters**

* **\[Long]:** Only long positions will be opened and closed, suitable for volatile upward markets.\

* **\[Short]:** Only short positions will be opened and closed, suitable for volatile downward markets.\

* **\[Shock]:** When the price continues to rise, open short and close long, when the price continues to fall, open long and close short, suitable for range-bound market.\

* **\[Grid Positions]:** The amount of position the robot holds when it first opens a position from an un-held state. It is recommended that beginners keep the default values.\

* **\[Grid Interval(%)]:** The robot will cover a new grid or close a position on a grid according to this ratio.\

* **\[Grid Number]:** Maximum limit on the number of grids.\

* **\[Leverage]:** Using leverage can be regarded as borrowing funds from the exchange to hold positions. The multiple of the enlarged principal is the leverage, and increasing leverage will magnify PnL. It is recommended to keep the default value of 5x leverage for beginners.\

* **\[Risk]:** The higher the risk level, the smaller the “Grid Interval(%)”, Conserved< Steady < Radical.\

* **\[Higher Price]:** The highest price that the strategy is expected to support, i.e. when the market price reaches this point, all grids are just holding positions. When choosing a short or shock robot, increasing the grid interval or number of grids may increase this price.\

* **\[Lower Price]:** The lowest price that the strategy is expected to support, i.e. when the market price reaches this point, all grids are just holding positions, and increasing the grid interval or number of grids when choosing a long or shock robot can reduce this price.\

* **\[Grid Layouts]：**\
  Geometric: The price distance for each grid is multiplied by a fixed ratio. For example 1, 2, 4, 8…\
  Arithmetic(%): The price distance of each grid is added according to a fixed value. For example 1, 2, 3, 4…\

* **\[Strike Price]:** Which is the limit price where the bot will be launched.\

* **\[Trailing Profit(%)]:** When the market price falls from a new high (long robot) or rises from a new low (short robot) and the ratio reaches this preset value, it will take profit.\

* **\[Trailing Stop(%)]:** When the market price rises from a new low (long robot) or falls back from a new high (short robot), and the ratio reaches this preset value and meets the grid interval, it will increase positions to cover the grids.

**Take-Profit and Stop-Loss**

* **Take Profit by Price:** If the latest price is higher than the preset price, the long robot will automatically close the position and stop working. And if the latest price is lower than the preset price, the short robot will automatically close the position and stop working.
* **Take-Profit by Amount:** When PnL + Floating > the preset amount, the robot will close all its positions and stop.
* **Stop Loss by Price:** If the latest price is lower than the preset price, the long robot will automatically close the position and stop working. And if the latest price is higher than the preset price, the short robot will automatically close the position and stop working.
* **Stop-Loss by Amount:** When PnL + Floating < -the preset amount, the robot will close all its positions and stop.

**How to start a bot of AI Grid?**

You only need to select the crypto to be traded, fill in the grid positions in each grid according to the funds you hold, and then click \[Launch] to start the AI Grid robot.

It is suggested that beginners keep the default parameters. You can make profits first, then gradually familiarize yourself with the strategy through the use of each parameter, and then you can design the parameters you want independently, and finally use AntBot, a powerful tool, to improve your trading profitability.

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2022/12/%E6%9C%AA%E6%A0%87%E9%A2%98-1-3.jpg" alt=""><figcaption></figcaption></figure>

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2022/12/%E6%9C%AA%E6%A0%87%E9%A2%98-2-2.jpg" alt=""><figcaption></figcaption></figure>

**Pros and Cons of AI Dual Grid**

Pros:

1\. No need to predict the trend of the market.\
2\. Works well in volatile and ranging markets.\
3\. Can be very effective – especially if the price moves rapidly within the grid range.

Cons:

1\. The grid strategy requires independent settlement of PnL for each order asset, which is different from the way the exchange settles PnL at the average price, resulting in incomprehension and inconvenient reconciliation for traders.\
2\. Multiple grids mean more complex trading and money management are required.\
3\. When there is a strong directional trend when breaking the grid interval, there will be a relatively large unrealized loss.

[#AI Grid](https://www.antrade.io/guide/docs/en/tag/ai-grid/)[#AntBot](https://www.antrade.io/guide/docs/en/tag/antbot/)[#Dual](https://www.antrade.io/guide/docs/en/tag/dual/)[#strategy](https://www.antrade.io/guide/docs/en/tag/strategy/)@AntBot free trading bot\
