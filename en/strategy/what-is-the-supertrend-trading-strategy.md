# What Is the SuperTrend Trading Strategy?

[Skip to content](https://www.antrade.io/guide/docs/en/strategy\_supertrend/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/en/)[Free AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/en)
* [Strategy](https://www.antrade.io/guide/docs/en/en-strategies/)
* [What Is the SuperTrend Trading Strategy?](https://www.antrade.io/guide/docs/en/strategy\_supertrend/)

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

## What Is the SuperTrend Trading Strategy?

4 months ago[AntBot](https://www.antrade.io/guide/docs/en/author/antbot/)5 minutes

**Contents：**

* [**What is the SuperTrend Trading Strategy?**](https://www.antrade.io/guide/docs/en/strategy\_supertrend/#WhatistheSuperTrendTradingStrategy?)\

* [**Calculation of ATR indicator**](https://www.antrade.io/guide/docs/en/strategy\_supertrend/#CalculationofATRindicator)\

* [**The calculation formula of the SuperTrend strategy**](https://www.antrade.io/guide/docs/en/strategy\_supertrend/#ThecalculationformulaoftheSuperTrendstrategy)\

* [**How to start a bot with the SuperTrend strategy?**](https://www.antrade.io/guide/docs/en/strategy\_supertrend/#HowtostartabotwiththeSuperTrendstrategy?)\

* [**Advantages and risks of the SuperTrend strategy**](https://www.antrade.io/guide/docs/en/strategy\_supertrend/#AdvantagesandrisksoftheSuperTrendstrategy)\

* [**Optimization of the SuperTrend strategy**](https://www.antrade.io/guide/docs/en/strategy\_supertrend/#OptimizationoftheSuperTrendstrategy)\

* [**The SuperTrend strategy backtest**](https://www.antrade.io/guide/docs/en/strategy\_supertrend/#TheSuperTrendstrategybacktest)

**What is the SuperTrend Trading Strategy?**

The SuperTrend strategy is based on the **SuperTrend technical indicator**. The SuperTrend indicator is an automatic **trailing stop loss indicator** based on N times Average True Range(**ATR**), which intuitively provides a **trend indicator** for **buying** and **sellin**g signals. . Breakthrough of the ATR channels defines pivot \[hl/2], up \[hl/2 + N\*ATR(M)], and down \[hl/2 – N\*ATR(M)]. If the closing price **falls below** the down, the trend turns downward, then **go short-selling**; if the closing price **breaks through the up**, the trend turns upward, then **go long-buying**.

**Calculation of ATR indicator**

ATR (Average True Range) measures the amplitude of price fluctuations over time, using the average value as the result. And here the size of amplitude is based on the largest of the following three:

1. The distance between the highest and lowest point of the day
2. The distance between the previous day’s closing price and the day’s highest price
3. The distance between the previous day’s closing price and the day’s lowest price

**The calculation formula of the SuperTrend strategy:**

* When going long:

SuperTrend = (highest price + lowest price)/2 – N\*ATR(M)

In the drawing, this value only moves up but not down, the recent highest value is taken.

* When going short:

SuperTrend = (highest price + lowest price)/2 + N\*ATR(M)

where N = 3, M = 10

**How to start a bot with the SuperTrend strategy?**

1\. Log into your AntBot account and find **\[SuperTrend]** in the **\[Robot]** of the **\[Trades]** interface and **click** the button on the right to enter the parameter setting page.

2\. Choose crypto based on personal criteria and preferences.

3\. Set **\[Initial Positions]**.

* **\[Initial Positions]**: The position amount of the robot’s first open position. Beginners are advised to keep the default values.

4\. Set **\[Running Mode]\[Direction]\[Leverage]** **\[Profit]** and **\[Loss]**.

* **\[Running Mode]**: It is divided into cycle and single. Cycle means that the robot will repeat the next round of opening positions after each take-profit and closing position, and the robot will only stop when it reaches the profit or loss conditions preset in the \[optional]. Single means that the robot will automatically terminate the operation after closing the position and taking a profit.
* **\[Auto]**: Going long when a long position signal is released, and going short when a short position signal is released according to the trading signal.
* **\[Long]**: Only run long position signal.
* **\[Short]**: Only run short position signal.
* **\[Leverage]**: Using leverage can be regarded as borrowing funds from the exchange to hold positions. The multiple of this position funds relative to the principal is the leverage, and increasing leverage will magnify profits and losses. It is recommended to keep the default value of 5x leverage for beginners.
* **\[Take-Profit]**

1. \[AI Tracking] is the default value, the robot calculates the signal every 30 minutes. When the signal reverses, it will take profit and close the positions, and the robot will enter the next cycle.
2. If there is a preset ratio value, the robot will close the position and take profit when the rate of return of the robot’s position reaches the preset value, and the robot will enter the next cycle.

* **\[Stop-Loss]**

1. \[AI Tracking] is the default value, when the robot builds a position, it pre-embeds the stop loss ratio according to the real price fluctuation of the 30-minute period. When the position loss rate reaches this preset value, it will close the position and stop loss, and the robot will enter the next cycle.
2. If there is a preset ratio value, the robot will close the position and stop the loss if the loss rate of the robot’s position reaches the preset value, and the robot will enter the next cycle.

5\. Click **\[Launch]** to successfully create a SuperTrend robot.

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2022/12/%E6%9C%AA%E6%A0%87%E9%A2%98-1.jpg" alt=""><figcaption></figcaption></figure>

**Advantages and risks of the SuperTrend strategy**

SuperTrend has a very good trend following, but there are few signals and the transaction is not flexible enough. On the basis of the original strategy, we added orbit-like algorithms and mobile opens, which are suitable for 30-minute periods or time periods below the daily line, suitable for running with small funds, and this strategy has no future functions and no price-stealing problems.

**Optimization of the SuperTrend strategy**

In the face of a slow and continuous unilateral market, the classic SuperTrend strategy will not be able to perceive the price breakthrough signal, leading to continuous losses in the account, which is a relatively large psychological burden on traders. AntBot records the opening price for each order of the SuperTrend strategy. When the price continues to reach a range of 3 times ATR on one side, it will close the position and stop the loss.

**The SuperTrend strategy backtest**

Timeframe: 30 minutes\
Parameters: ATR M=10, N = 3\
Go long in an upward trend, and close when it falls below; only long positions;\
The entry amount is $1,000, and the amount of each entry transaction is 100% cash;\
Trading range: Jun. 1, 2022 to Nov. 17, 2022\
Symbol: ETHUSDT\
Fees: 0.04%

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2022/12/1671422249325.png" alt=""><figcaption></figcaption></figure>

References:

[https://fintastic.trading/wisdom\_box/supertrend-指標](https://fintastic.trading/wisdom\_box/supertrend-%E6%8C%87%E6%A8%99)

[https://elearnmarkets.com/blog/supertrend-indicator-strategy-trading](https://elearnmarkets.com/blog/supertrend-indicator-strategy-trading)

[https://www.tradingview.com/script/r6dAP7yi/](https://www.tradingview.com/script/r6dAP7yi/)

[#AntBot](https://www.antrade.io/guide/docs/en/tag/antbot/)[#atr](https://www.antrade.io/guide/docs/en/tag/atr/)[#bot](https://www.antrade.io/guide/docs/en/tag/bot/)[#strategy](https://www.antrade.io/guide/docs/en/tag/strategy/)[#supertrend](https://www.antrade.io/guide/docs/en/tag/supertrend/)[#trading](https://www.antrade.io/guide/docs/en/tag/trading/)[#trend-following](https://www.antrade.io/guide/docs/en/tag/trend-following/)@AntBot free trading bot\
