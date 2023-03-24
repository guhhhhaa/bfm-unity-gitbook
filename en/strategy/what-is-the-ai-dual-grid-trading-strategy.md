# What Is the AI Dual Grid Trading Strategy?

[Skip to content](https://www.antrade.io/guide/docs/en/strategy\_dual\_grid/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/en/)[Free AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/en)
* [Strategy](https://www.antrade.io/guide/docs/en/en-strategies/)
* [What Is the AI Dual Grid Trading Strategy?](https://www.antrade.io/guide/docs/en/strategy\_dual\_grid/)

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

## What Is the AI Dual Grid Trading Strategy?

5 months ago[AntBot](https://www.antrade.io/guide/docs/en/author/antbot/)4 minutes

#### What is the AI Dual Grid Strategy? <a href="#ey6rh2" id="ey6rh2"></a>

The AI Dual Grid Strategy is a Futures Grid Strategy that can holding long and short at the same time for oscillating market. It is an extension of the AI Grid of AntBot, and can be thought of as two independent AI Grid robots running at 5x leverage and in opposite directions.

**The Profit principle of AI Dual Grid**

When a long robot’s position of a grid reaches a take-profit ratio and is stopped out, the short robot will purchase a grid of short positions at the same price as the long robot’s take profit just now, so that whenever one grid generates a profit in the direction of the current trend, the other grid will lose money and vice versa. This is a AI Dual Grid operation feature.

In this case, each side of the grid should have its own take-profit and stop-loss, managing both grids independently to lock in profits in a volatile market.

This is the profit principle of AI Dual Grid. The AI Dual Grid strategy helps to reach the total profit target faster and minimizes retractions.

As shown in the chart below:

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2022/12/double_grid_setup.webp" alt=""><figcaption></figcaption></figure>

**What problem does it solve?**

The AI Dual Grid is one of the original strategies of AntBot Team. It perfectly solves the three major problems of the classic grid strategy.

1.Beyond the grid price range does not generate profits.\
The AI Dual Grid while running long and short two directional strategies, regardless of price increases and decreases will have profits generated.

2.Low capital efficiency.\
Still because the AI Dual Grid runs both long and short direction robots, long and short can only be trapped on one side, the other side will definitely continue to generate profits.\
In addition, the AI Dual Grid strategy will be based on different underlying support resistance and volatility to develop their own grid interval to achieve the best ratio of returns / risk.\
3.No automatic adjustment after breaking the price range

**What are the features of AntBot’s AI Dual Grid**

1.There is no limit order, and the margin is shared to prevent liquidation.\
2.The take profit of each grid is calculated and executed independently, and the take profit is divided into positions to improve the liquidity of funds.\
3.Two independently operating long grids and short grids should be considered as two separate systems, as both have clear profit and sell boundaries.\
4.There is a difference in the display of profit and loss in the trading records of AntBot and the exchange, because AntBot calculates the profit and loss of the grid based on the opening and closing price of each grid, while the exchange calculates the profit and loss of each order based on the average position price .

<figure><img src="https://antrade.io/guide/docs/en/wp-content/uploads/2022/10/What-is-the-AI-Dual-Grid-Strategy-0002.jpg" alt=""><figcaption></figcaption></figure>

As a result of running both a long grid strategy and a short grid strategy on an underlying, there is always a brief floating loss on one side, or even both, which is normal performance. The AI Dual Grid is a regression-based strategy and an investment-based strategy that holds risk in order to obtain corresponding profits.

**Pros and Cons of AI Dual Grid**

Pros:\
No need to predict market movements.\
Works well in volatile, directionless markets.\
Can be very effective under the right conditions – especially when prices move quickly within the grid range.

Cons:\
Grid strategies require separate P\&L calculations for each asset traded, which differs from the exchange-based P\&L calculation on an average price basis, leading to incomprehensible and inconvenient reconciliations for users.\
Multiple grids mean more complex trading and money management is required.\
When there is a strong directional trend, the breakout of the grid range will result in a relatively large floating loss.

[#AntBot](https://www.antrade.io/guide/docs/en/tag/antbot/)[#Dual Grid](https://www.antrade.io/guide/docs/en/tag/dual-grid/)[#strategy](https://www.antrade.io/guide/docs/en/tag/strategy/)[#trading](https://www.antrade.io/guide/docs/en/tag/trading/)@AntBot free trading bot\
