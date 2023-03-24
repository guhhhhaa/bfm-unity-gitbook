# What Is the Classic Grid Trading Strategy?

[Skip to content](https://www.antrade.io/guide/docs/en/strategy\_grid/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/en/)[Free AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/en)
* [Strategy](https://www.antrade.io/guide/docs/en/en-strategies/)
* [What Is the Classic Grid Trading Strategy?](https://www.antrade.io/guide/docs/en/strategy\_grid/)

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

## What Is the Classic Grid Trading Strategy?

5 months ago[AntBot](https://www.antrade.io/guide/docs/en/author/antbot/)6 minutes

**Contents:**

* [**Principles of grid strategy**](https://www.antrade.io/guide/docs/en/strategy\_grid/#Principles-of-grid-strategy)\

* [**How to reduce risk?**](https://www.antrade.io/guide/docs/en/strategy\_grid/#How-to-reduce-risk?)\

* [**How to amplify the benefits?**](https://www.antrade.io/guide/docs/en/strategy\_grid/#How-to-amplify-the-benefits?)\

* [**How to start a robot with Classic Grid strategy?**](https://www.antrade.io/guide/docs/en/strategy\_grid/#How-to-start-a-bot-with-Classic-Grid?)

**Principles of grid strategy**

The classic grid is the most traditional version that best represents the essence of the grid strategy.

The grid trading strategy is essentially an automatic trading system that buys low and sells high. First of all, you need to set an appropriate interval and grid size, and then match the corresponding funds and positions. When the price falls, it will be bought in batches. When the price rises, it will be sold in batches. It is a trading method to harvest profits from price fluctuations through repeated buying low and selling high behaviors.

For easy understanding, the following schematic diagram is provided for reference:

<figure><img src="https://antrade.io/guide/docs/en/wp-content/uploads/2022/10/What-is-thie-Grid-Trading-Strategy.gif" alt=""><figcaption></figcaption></figure>

Grid trading method does not rely on artificial thinking, does not need to study the market does not need to feel, is completely a kind of program behavior, very suitable for computer automation, the use of market fluctuations in the grid range to buy low sell high, in order to repeatedly cycle the difference to earn profits.

The grid trading method is a kind of front-side trading. Different from back-side trading, the grid trading method does not follow the market to chase ups and downs. Instead, go against the trend, buying when prices fall and selling when prices rise.

**How to reduce risk?**

Choose assets with long-term upward trends and continuous new highs in price. If the target is selected correctly, the profit is basically locked in, and at most it only loses time.

In order to reduce the time cost, it is best to choose to start the robot in the undervalued sideways area. If the grid is drawn in an overvalued area, the stock price may not be able to come back for a long period of time when the market situation takes a sharp turn. At this time, we can only wait for the endogenous growth of the target or the next stock price rebound driven by market sentiment, which requires a large time cost and psychological cost.

**How to amplify the benefits?**

**1. Among the targets with the same fluctuation frequency, choose the variety with large fluctuation range.**

Among the targets with the same fluctuation frequency, the grid spacing can be set larger for varieties with larger fluctuation range, which means that the income harvested by each grid in the same period is higher.

A simple diagram is as follows:

In the figure above, B stands for buying, S stands for selling, the black line is the target with small fluctuation range, and the red line is the target with large fluctuation range. Obviously, the grid operation under the trend of the red line is more profitable.

**2. Among the targets with the same fluctuation range, choose the product with higher fluctuation frequency.**

Among the targets with the same fluctuation range, the higher the fluctuation frequency, the higher the frequency of profit harvesting, and the higher the income.

A simple diagram is as follows:

In the figure above, B stands for buying and S stands for selling. The black line is the target with low frequency, and the red line is the target with high frequency. Obviously, the frequency of harvesting under the trend of the red line is higher, so the profit is higher.

So how to screen out the varieties with large fluctuation range and high fluctuation frequency?

In addition to some quantitative data, there is a simple method for ordinary traders: overlap the K-lines of several targets for alternative operations. In this way, it is easy to compare and distinguish the targets with relatively excellent fluctuation and frequency.

Summarize the key elements in the selection of targets for grid trading operations: **high-quality undervalued assets with large fluctuation range and high fluctuation frequency.**

**How to start a bot with Classic Grid?**

1\. Log into your AntBot account to find **\[Classic Grid]** in the **\[Robot]** of the **\[Trades]** interface and **click** the button on the right to enter the parameter setting page.

2\. Choose **crypto** based on personal criteria and preferences.

3\. Fill in the detailed parameters. The following parameters may help you.

* **\[Grid Positions]**: The amount of funds in each grid in USDT.\

* **\[Grid Interval]**: The Profit of per grid.\

* **\[Grid Number]**: Maximum limit on the number of grids.\

* **\[Price Ceiling]**: When the price is higher than the preset price, long and short robots will not open but close their positions until the price falls back to the preset price.\

* **\[Price Floor]**: When the price is lower than the preset price, the long and short robots will not open but only close their positions until the price rises back to the preset price.\

* **\[Trailing Profit]**: Taking the long robot as an example, when the price falls back from the new highest price and the percentage of the fall reaches the preset value, and the price also meets the take-profit ratio at the same time, the position will be closed. For the short robot, when the market price rebounds from the new lowest price and the rising ratio reaches the preset value, and the price also meets the take-profit ratio at the same time, the position will be closed.\

* **\[Trailing Stop]**: Taking the long robot as an example, when the price rebounds from the new lowest price and the rising ratio reaches the preset value, and the price also meets the price gap at the same time, the position will be increased; for the short robot, when the price falls from the new highest price and the falling ratio reaches the preset value, and the price also meets the price gap at the same time, the position will be increased.
* **\[Take-profit]**

**Take profit by price**

If the latest price is higher than the preset price, the long robot will automatically close the position and stop working. And if the latest price is lower than the preset price, the short robot will automatically close the position and stop working.

**Take profit by amount**

PnL + Floating> the preset amount, the bot will automatically close the positions.

* **\[Stop-loss]**

**Stop loss by price**

If the latest price is lower than the preset price, the long robot will automatically close the position and stop working. And if the latest price is higher than the preset price, the short robot will automatically close the position and stop working.

**Stop loss by amount**

PnL + Floating > the preset amount, the bot will automatically close the positions.

4\. Click **\[Launch]** to successfully create a Classic Grid robot.

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2022/12/%E6%9C%AA%E6%A0%87%E9%A2%98-1-2.jpg" alt=""><figcaption></figcaption></figure>

[#AntBot](https://www.antrade.io/guide/docs/en/tag/antbot/)[#buys low and sells high](https://www.antrade.io/guide/docs/en/tag/buys-low-and-sells-high/)[#Dual](https://www.antrade.io/guide/docs/en/tag/dual/)[#Grid](https://www.antrade.io/guide/docs/en/tag/grid/)[#strategy](https://www.antrade.io/guide/docs/en/tag/strategy/)@AntBot free trading bot\
