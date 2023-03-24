# What Is the Momentum Trading Strategy?

[Skip to content](https://www.antrade.io/guide/docs/en/strategy-momentum/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/en/)[Free AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/en)
* [Strategy](https://www.antrade.io/guide/docs/en/en-strategies/)
* [What Is the Momentum Trading Strategy?](https://www.antrade.io/guide/docs/en/strategy-momentum/)

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

## What Is the Momentum Trading Strategy?

3 months ago[AntBot](https://www.antrade.io/guide/docs/en/author/antbot/)5 minutes

**Contents:**

* [What is momentum trading strategy?](https://www.antrade.io/guide/docs/en/strategy-momentum/#What-is-momentum-trading-strategy?)\

* [Why does the momentum strategy work?](https://www.antrade.io/guide/docs/en/strategy-momentum/#Why-does-the-momentum-strategy-work?)\

* [How the AntBot momentum strategy is implemented?](https://www.antrade.io/guide/docs/en/strategy-momentum/#How-the-AntBot-momentum-strategy-is-implemented?)\

* [Risks of momentum strategy](https://www.antrade.io/guide/docs/en/strategy-momentum/#Risks-of-momentum-strategy)\

* [Momentum strategy backtest results and robustness analysis](https://www.antrade.io/guide/docs/en/strategy-momentum/#Momentum-strategy-backtest-results-and-robustness-analysis)\

* [How to start the momentum strategy robot?](https://www.antrade.io/guide/docs/en/strategy-momentum/#How-to-start-the-momentum-strategy-robot?)

**What is the momentum trading strategy?**

AntBot’s momentum strategy is a trend trading strategy that analyzes price inertia to capture trading edges. By calculating the speed of price fluctuations, signals such as the price entering a strong peak and turning into a weak trough are obtained. **The momentum strategy deserves to be one of the most popular in the investment world**, and the vast majority of CTA strategies in current futures are momentum strategies.

**Why does the momentum strategy work?**

**The Momentum Effect, also known as the Inertia Effect, is the basis of the momentum strategy. It refers to the tendency of asset prices to continue the original direction of movement.** This means that assets with higher profits in the past will still receive higher profits in the future. **Therefore, investors can obtain low-cost excess returns by buying assets with good historical performance and selling assets with poor performance.**

**How the AntBot momentum strategy is implemented?**

**AntBot employs linear regression modeling to plot the momentum of the futures price to judge the high probability trend of the price based on the strength of the momentum.** Linear regression is a well-established statistical technique that can be easily applied to software and calculations. Businesses can use linear regression to transform raw data into business intelligence and actionable insights in a reliable and predictable way. Scientists in many fields, including biology and behavioral, environmental, and social sciences, use linear regression for preliminary data analysis and prediction of future trends. Many data, such as machine learning and artificial intelligence, use the scientific approach of linear regression to solve complex problems.

**Risks of the momentum strategy**

1\. AntBot’s momentum strategy monitors the market in real-time and actively reduces the number of orders opened by the trend strategy when entering the sideways stage, which will cause the robot to need a long wait for entry, requiring sufficient patience from the trader.

2\. It will lead to continuous losses in extremely unfavorable markets, such as high frequency of price fluctuations and large price volatility. AntBot’s momentum strategy has a built-in 2 Average True Range(ATR) real-time trailing stop-loss by default to avoid risks, allowing traders to reduce the opening amount moderately depending on their own funds, and resume them when the market picks up.

**The momentum strategy backtest results and robustness analysis**

Timeframe: 120 minutes\
The entry amount: $1,000, each entry transaction amount is 100% cash\
Trading range: Jan. 1, 2022 to Dec. 23, 2022\
Symbol: ETHUSDT\
Fees: 0.04%

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2023/01/1672826537256.png" alt=""><figcaption></figcaption></figure>

**How to start the momentum strategy robot?**

1\. Log into your AntBot account to find **\[Momentum]** in the **\[Robot]** of the **\[Trades]** interface and **click** the button on the right to enter the parameter setting page.

2\. Choose **crypto** based on personal criteria and preferences.

3\. Fill in **\[Initial Positions]**, or slide the box below to set it. Beginners are advised to keep the default value.

* **\[Initial Positions]:** The position amount of the robot’s first open position.

4\. It is recommended that novices keep the default values of all detailed parameters, and directly click **\[Launch]** to run the robot.

* **\[Leverage]:** Using leverage can be regarded as borrowing funds from the exchange to hold positions. The multiple of this position funds relative to the principal is the leverage, and increasing leverage will magnify profits and losses. It is recommended to keep the default value of 5x leverage for beginners.
* **\[Max Order]:** The maximum number that bots are allowed to increase positions consecutively from the state of unopened position.
* **\[Running Mode]:** It is divided into cycle and single. Cycle means that the robot will repeat the next round of opening positions after each take-profit and closing position, and the robot will only stop when it reaches the profit or loss conditions preset in the **\[Take-Profit]** and **\[Stop-Loss]**. Single means that the robot will automatically terminate the operation after completing a cross-position take profit.
* **\[Auto]:** According to the trading signal, going long when a long position signal is released, and going short when a short position signal is released.
* **\[Long]:** Only run long position signal.
* **\[Short]:** Only run short position signal.
* **\[Take-Profit]**

1\. \[Trailing By AI] is the default value, the robot calculates the signal every 30 minutes. When the signal reverses, it will take profit and close the positions, and the robot will enter the next cycle.

2\. If there is a preset ratio value, the robot will close the position and take profit when the rate of return of the robot’s position reaches the preset value, and the robot will enter the next cycle.

* **\[Stop-Loss]**

1\. \[Trailing By AI] is the default value, when the robot builds a position, it pre-embeds the stop loss ratio according to the real price fluctuation of the 30-minute period. When the position loss rate reaches this preset value, it will close the position and stop loss, and the robot will enter the next cycle.

2\. If there is a preset ratio value, the robot will close the position and stop the loss if the loss rate of the robot’s position reaches the preset value, and the robot will enter the next cycle.

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2022/12/%E6%9C%AA%E6%A0%87%E9%A2%98-1-5.jpg" alt=""><figcaption></figcaption></figure>

[#AntBot](https://www.antrade.io/guide/docs/en/tag/antbot/)[#Momentum](https://www.antrade.io/guide/docs/en/tag/momentum/)[#strategy](https://www.antrade.io/guide/docs/en/tag/strategy/)[#trading](https://www.antrade.io/guide/docs/en/tag/trading/)@AntBot free trading bot\
