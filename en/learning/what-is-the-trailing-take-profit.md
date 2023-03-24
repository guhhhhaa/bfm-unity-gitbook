# What is the Trailing Take-Profit

[Skip to content](https://www.antrade.io/guide/docs/en/en-trailing-tp/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/en/)[Free AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/en)
* [Learning](https://www.antrade.io/guide/docs/en/en-learning/)
* [What is the Trailing Take-Profit](https://www.antrade.io/guide/docs/en/en-trailing-tp/)

Search for:

LEARNING

*
  * [What is a Golden Cross and a Death Cross? ](https://www.antrade.io/guide/docs/en/what-is-a-golden-cross-and-a-death-cross/)
  * [What is the Golden Cross?](https://www.antrade.io/guide/docs/en/what-is-the-golden-cross/)
  * [Instantly Improve Your Trading Strategy with Support and Resistance](https://www.antrade.io/guide/docs/en/instantly-improve-your-trading-strategy-with-support-and-resistance/)
  * [The Ultimate Moving Average Trading Guide](https://www.antrade.io/guide/docs/en/the-ultimate-moving-average-trading-guide/)
  * [10  Price Action Candlestick Patterns You Must Know](https://www.antrade.io/guide/docs/en/10-candlestick-patterns-you-must-know/)
  * [Detailed Explanation of Support and Resistance](https://www.antrade.io/guide/docs/en/support-resistance/)
  * [Can Automated Trading Bots Really Make Money?](https://www.antrade.io/guide/docs/en/robots-make-money/)
  * [How are AntBot’s Initial Positions Calculated?](https://www.antrade.io/guide/docs/en/antbots-initial-positions-calculated/)
  * [Can API-Keys of Two Exchanges Be Imported Under One Account?](https://www.antrade.io/guide/docs/en/two-api-keys-under-one-account/)
  * [Binance Trading Fees](https://www.antrade.io/guide/docs/en/binance-trading-fees/)
  * [Binance Fee Calculator: How To Calculate Binance Fees?](https://www.antrade.io/guide/docs/en/binance-fee-calculator-how-to-calculate-binance-fees/)
  * [Can One Crypto Run Multiple Bots at the Same Time?](https://www.antrade.io/guide/docs/en/one-crypto-run-multiple-bots/)
  * [Which Robot Should a Novice Choose to Start and Which Crypto to Choose?](https://www.antrade.io/guide/docs/en/novice-choose-bot-and-crypto/)
  * [Why Is the Profit of AI Grid Different From the Profit of the Exchange?](https://www.antrade.io/guide/docs/en/the-profit-difference-in-ai-grid-and-exchange/)
  * [Why AntBot Doesn’t Get My Assets on the Exchange?](https://www.antrade.io/guide/docs/en/why-doesnt-get-assets/)
  * [Will AntBot Sell the Funds I Bought Manually on the Exchange?](https://www.antrade.io/guide/docs/en/will-antbot-sell-funds-i-bought/)
  * [What Should I Do About the Position Limit of the Exchange Account?](https://www.antrade.io/guide/docs/en/position-limit-of-exchange-account/)
  * [Why Is the Position not Added After the Price Has Reached the Position Increase Price?](https://www.antrade.io/guide/docs/en/why-is-position-not-added/)
  * [Can Energy Be Exchanged for USDT?](https://www.antrade.io/guide/docs/en/energy-exchange-usdt/)
  * [How Many Funds Do I Need to Start a Bot?](https://www.antrade.io/guide/docs/en/funds-to-start-bot/)

## What is the Trailing Take-Profit

5 months ago[AntBot](https://www.antrade.io/guide/docs/en/author/antbot/)1 minute

#### What is the Trailing Take-Profit? <a href="#b9lq0j" id="b9lq0j"></a>

Here we take the spot position as an example. In order to expand the profit when the market price rises, the take-profit is not executed according to the pre-set take-profit ratio, but market price is continuously monitored, and the take profit is not executed until the price retraces.

The Trailing Take-Profit mechanism can help you not miss the unilateral rise and capture more profits.

Both the DAC and Grid strategies of AntBot have the option of setting the Trailing Take-Profit. You can enable the Trailing Take-Profit function by opening and filling the ratio of the “Trailing Profit(%)” option.

To execute a complete Trailing Take-Profit, 2 conditions must be met:

1. When the market falls from the highest point to the current price, the retrace ratio must be greater than the pre-set ratio of “Trailing Profit(%)”.
2. Since the last time the position was opened, the market price has increased more than the “Take Profit(%)”

The following figure is a schematic diagram of Trailing Take-profit.

<figure><img src="https://antrade.io/guide/docs/en/wp-content/uploads/2022/10/What-is-the-Trailing-Take-Profit.png" alt=""><figcaption></figcaption></figure>

[#AntBot](https://www.antrade.io/guide/docs/en/tag/antbot/)@AntBot free trading bot\
