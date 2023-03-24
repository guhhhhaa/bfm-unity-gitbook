# What Is the R-Breaker Trading Strategy?

[Skip to content](https://www.antrade.io/guide/docs/en/strategy\_r-breaker/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/en/)[Free AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/en)
* [Strategy](https://www.antrade.io/guide/docs/en/en-strategies/)
* [What Is the R-Breaker Trading Strategy?](https://www.antrade.io/guide/docs/en/strategy\_r-breaker/)

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

## What Is the R-Breaker Trading Strategy?

4 months ago[AntBot](https://www.antrade.io/guide/docs/en/author/antbot/)11 minutes

**Contents：**

* [**What is the R-Breaker Trading Strategy?**](https://www.antrade.io/guide/docs/en/strategy\_r-breaker/#R-Breakerstrategy)\

* [**Resistance and Support**](https://www.antrade.io/guide/docs/en/strategy\_r-breaker/#ResistanceandSupport)\

* [**Strategy logic**](https://www.antrade.io/guide/docs/en/strategy\_r-breaker/#Strategylogic)\

* [**How to start an R-Breaker strategy bot?**](https://www.antrade.io/guide/docs/en/strategy\_r-breaker/#HowtostartanR-Breakerstrategybot?)\

* [**The R-Breaker strategy backtest**](https://www.antrade.io/guide/docs/en/strategy\_r-breaker/#TheR-Breakerstrategybacktest)\

* [**Advantages and disadvantages of the R-Breaker strategy**](https://www.antrade.io/guide/docs/en/strategy\_r-breaker/#AdvantagesanddisadvantagesoftheR-Breakerstrategy)

**What is the R-Breaker Trading Strategy?**

The R-Breaker strategy was developed by Richard Saidenberg and published in 1994. It was selected as one of the top ten **most profitable** trading strategies by the American _Futures Truth_ magazine for 15 consecutive years. Compared with other strategies, the R-Breaker is a trading strategy that combines **trend** and **trend**–**reversal**. Not only can you **capture the trend** of the market to **obtain large profits**, but you can also take the initiative to **stop the profit in time** and **track the trend reverse.**

The R-Breaker strategy is mainly divided into two parts: **Reversal** and **Trend**. **Follow** the trend when you have **no positions** and wait for a **reversal signal** when you **open positions**.

**Resistance and Support**

The R-Breaker strategy is a price support and resistance strategy. It calculates seven prices based on yesterday’s highest, lowest and closing prices: a central price (pivot), three support levels (s1, s2, s3), and three resistance levels (r1, r2, r3). Then, according to the positional relationship between the current price and these support and resistance levels, to form the trigger conditions for buying and selling, and through a certain algorithm adjustment, adjust the distance between these seven prices, further changing the trigger value of the transaction.

| **Calculation**                                              |
| ------------------------------------------------------------ |
| Breakthrough buying price (resistance level r3) = H + 2P -2L |
| Observing selling price (resistance level r2) = P + H – L    |
| Reverse selling price (resistance level r1) = 2P – L         |
| Center price (pivot) = (H + C + L)/3                         |
| Reverse buying price (support level s1) = 2P – H             |
| Observing buying price (support level s2) = P – (H – L)      |
| Breakthrough selling price (support level s3) = L – 2(H – P) |

From this we can see that the R-Breaker strategy draws a grid-like price line based on yesterday’s price, and updates these price lines once a day. In technical analysis, the support and resistance levels, and the role of the two can be converted to each other. When the price successfully breaks up the resistance level, the resistance level becomes the support level; when the price successfully breaks down the support level, the support level becomes the resistance level.

In actual trading, these support and resistance levels indicate to the trader the direction of opening and closing positions and the precise trading points. Traders with specific opening and closing conditions can flexibly customize according to intraday prices, central prices, resistance levels, and support levels, and can also manage positions based on these grid price lines.

**Strategy logic**

Next, let us see how the R-Breaker strategy uses these support and resistance levels.&#x20;

If there is no holding position, enter the trend mode. When the price is greater than the breakthrough buying price, open long positions; when the price is less than the breakthrough selling price, open short positions.

* **Trend mode**
  * Open long positions: if there is no holding position and the price is greater than the breakthrough buying price.
  * Open short positions: if there is no holding position and the price is less than the breakthrough selling price.
  * Close long position: if you are holding a long position, and the highest price of the day is greater than the observing selling price, and the price is less than the reverse selling price.
  * Close short position: if you are holding a short position, and the lowest price of the day is less than the observing buying price, and the price is greater than the reverse buying price.

If there are holding positions, they enter the reversal mode. When there are holding long positions, and the highest price on the day is greater than the observing selling price, and the price falls below the reverse selling price, the long position will be closed and the short position will be open synchronously. When holding short positions, and the lowest price of the day is less than the observing buying price, and the price breaks through the reverse buying price, the short position will be closed and the long position will be open.

* **Reverse mode**
  * Open long position: if you holding a short position, and the lowest price of the day is less than the observing buying price, and the price is greater than the reverse buying price.
  * Open short position: if you are holding a long position, and the highest price of the day is greater than the observing selling price, and the price is less than the reverse selling price.
  * Close long position: if long positions are held and the price is less than the breakthrough selling price.
  * Close short position: if short positions are held and the price is greater than the breakthrough buying price.

As shown below:

<figure><img src="https://antrade.io/guide/docs/en/wp-content/uploads/2022/12/%E7%A4%BA%E6%84%8F%E5%9B%BE-1.jpg" alt=""><figcaption></figcaption></figure>

First, let’s take a look at the relationship between these 6 prices and the previous day’s price.

* Reverse selling price and reverse buying price

According to the derivation of the formula, it is found that these two prices have no definite relationship with the highest and lowest prices of the previous day.

* Observing selling price and observing buying price

Subtract the highest price of the previous day from the observing selling price, and find that (H+P-L)-H = P – L >0, indicating that the observing selling price > the highest price of the previous day; the observing buying price < the lowest price of the previous day.

* Breakthrough buying price and breakthrough selling price

Breakthrough buying price>observing selling price>the highest price of the previous day, it can be explained that the breakthrough buying price>>the highest price of the previous day. After making a difference, it can be found that the breakthrough buying price – the highest price of the previous day = 2\[(C-L)+(H-L)]/3.

The expressions of K-line:

* The longer the K-line of the previous day, the longer the lower shadow, and the higher the breakthrough buying price.
* The longer the K-line of the previous day, the longer the upper shadow, and the higher the breakthrough selling price.

In this way, the logic behind the R-Breaker can be explained.

When today’s price breaks through the highest point of the previous day, it will be an upward trend in terms of form, and it has certain conditions for opening long positions, but this condition alone is not sufficient. If the lower shadow line of the previous day is longer, it means that the game between long and short sides is fierce, and the power of long position is strong. Therefore, you can set a higher breakthrough buying price. Once the breakthrough shows that long position has firmly gained the upper hand, then there is reason to believe that it will continue to rise in the future. The same can explain the logic behind the breakthrough selling price.

* When holding a long position, if the price continues to rise, the position will be closed before the end of the day to make a profit. If the price does not rise but falls, and falls below the observing selling price, the price is still above the highest price of the previous day, so continue to wait and see. If it continues to fall until it falls below the reverse selling price, close the position and stop the loss.
* When holding a short position, if the price continues to fall, the position will be closed before the end of the day to make a profit. If the price does not fall but rises when it rises to observing buying price, the price is still below the lowest price of the previous day at this time, so continue to wait and see. If it continues to rise until it reaches the reverse buying price, close the position and stop the loss.

The figure below is the R-Breaker strategy pattern in TradingView.

<figure><img src="https://antrade.io/guide/docs/cn/wp-content/uploads/2022/11/1668482276769.png" alt=""><figcaption></figcaption></figure>

**How to start an R-Breaker strategy bot?**

1\. Log into your AntBot account to find **\[R-Breaker]** in the **\[Robot]** of the **\[Trades]** interface and **click** the button on the right to enter the parameter setting page.

2\. Choose crypto based on personal criteria and preferences.

3\. Fill in **\[Initial Positions]**.

* **\[Initial Positions]**: The position amount of the robot’s first open position. Beginners are advised to keep the default values.

4\. Set **\[Leverage]**, **\[Max order] \[Running Mode]** **\[Direction]** **\[Take-Profit]** and **\[Stop-Loss]**.

* **\[Leverage]**: Using leverage can be regarded as borrowing funds from the exchange to hold positions. The multiple of this position funds relative to the principal is the leverage, and increasing leverage will magnify profits and losses. It is recommended to keep the default value of 5x leverage for beginners.
* **\[Max Order]**: The maximum number that bots are allowed to increase positions consecutively from the state of unopened position.
* **\[Running Mode]**: It is divided into cycle and single. Cycle means that the robot will repeat the next round of opening positions after each take-profit and closing position, and the robot will only stop when it reaches the profit or loss conditions preset in the **\[Take-Profit ]** and **\[ Stop-Loss ]**. Single means that the robot will automatically terminate the operation after completing a cross-position take profit.
* **\[Auto]**: According to the trading signal, going long when a long position signal is released, and going short when a short position signal is released.
* **\[Long]**: Only run long position signal.
* **\[Short]**: Only run short position signal.
* **\[Take-Profit]**

1. \[AI Tracking] is the default value, the robot calculates the signal every 30 minutes. When the signal reverses, it will take profit and close the positions, and the robot will enter the next cycle.
2. If there is a preset ratio value, the robot will close the position and take profit when the rate of return of the robot’s position reaches the preset value, and the robot will enter the next cycle.

* **\[Stop-Loss]**

1. \[AI Tracking] is the default value, when the robot builds a position, it pre-embeds the stop loss ratio according to the real price fluctuation of the 30-minute period. When the position loss rate reaches this preset value, it will close the position and stop loss, and the robot will enter the next cycle.
2. If there is a preset ratio value, the robot will close the position and stop the loss if the loss rate of the robot’s position reaches the preset value, and the robot will enter the next cycle.

5\. Click **\[Launch]** to successfully create an R-Breaker robot.

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2022/12/%E6%9C%AA%E6%A0%87%E9%A2%98-4.jpg" alt=""><figcaption></figcaption></figure>

**The R-Breaker strategy backtest**

Timeframe: 30 minutes\
The entry amount: $1,000, and the amount of each entry transaction is 100% cash.\
Trading range: Jan. 1, 2022 to Dec. 19, 2022\
Symbol: BTCUSDT\
Fees: 0.04%

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2022/12/1671421944332.png" alt=""><figcaption></figcaption></figure>

**Advantages and disadvantages of the R-Breaker strategy**

Advantages:

1\. When the market is in a consolidation period, this strategy will filter out some small fluctuations, that is, not to enter the market casually when the fluctuation between the observing buying price and the observing selling price.

2\. The distance between the observing buying price and the observing selling price will change with the fluctuations. If the consolidation fluctuations shrink for several consecutive days, the distance between the six prices of R-Breaker will also shrink accordingly. When the consolidation breaks through, an open signal will be issued to grab the advantage.

3\. The R-Breaker strategy is composed of two sub-strategies of trend and trend-reverse, which is easy to grasp the balance of the market. For example, when the trend strategy retraces, the trend-reverse strategy can first close the position to keep the profit, or even open the opposite position to catch the reverse market.

Disadvantages:

1\. In a period of rapid rise and fall in the market, it is easier to trigger the six price levels, and the stop-loss is frequent.

2\. During the long-term consolidation period, filter conditions need to be added to control the distance between the six prices not to be too small to avoid frequent opening of positions.

3\. It is necessary to add a mechanism for excessively frequent transactions within a period of time. For example, the fluctuation range of the previous day is small, resulting in a relatively close distance between the six prices, and the price fluctuations of the next day are severe, which will also cause frequent opening and closing of positions.

References:

[https://medium.com/@FMZ\_Quant/commodity-futures-r-breaker-strategy-f9275c360aa](https://medium.com/@FMZ\_Quant/commodity-futures-r-breaker-strategy-f9275c360aa)

[https://www.myquant.cn/docs/python\_strategyies/425](https://www.myquant.cn/docs/python\_strategyies/425)

[https://www.tradingview.com/script/fYqAT2ys-blackcat-L2-Intraday-R-Breaker-Indicator/](https://www.tradingview.com/script/fYqAT2ys-blackcat-L2-Intraday-R-Breaker-Indicator/)

[#bot](https://www.antrade.io/guide/docs/en/tag/bot/)[#R-Breaker](https://www.antrade.io/guide/docs/en/tag/r-breaker/)[#strategy](https://www.antrade.io/guide/docs/en/tag/strategy/)[#trading](https://www.antrade.io/guide/docs/en/tag/trading/)[#trend-following](https://www.antrade.io/guide/docs/en/tag/trend-following/)@AntBot free trading bot\
