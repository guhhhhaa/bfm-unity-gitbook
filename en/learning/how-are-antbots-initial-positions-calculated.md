# How are AntBot’s Initial Positions Calculated?

[Skip to content](https://www.antrade.io/guide/docs/en/antbots-initial-positions-calculated/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/en/)[Free AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/en)
* [Beginner](https://www.antrade.io/guide/docs/en/en-beginner/)
* [Learning](https://www.antrade.io/guide/docs/en/en-learning/)
* [Questions](https://www.antrade.io/guide/docs/en/en-questions/)
* [How are AntBot’s Initial Positions Calculated?](https://www.antrade.io/guide/docs/en/antbots-initial-positions-calculated/)

Search for:

BEGINNER

*
  * [How to Create Bitget API Key?](https://www.antrade.io/guide/docs/en/binding\_bitget/)
  * [How to Create Gate.io API Key?](https://www.antrade.io/guide/docs/en/binding\_gateio/)
  * [How to Create Kucoin API Key?](https://www.antrade.io/guide/docs/en/binding\_kucoin/)
  * [Insufficient API Key Trading Permissions: How to Modify API Key Trading Permissions?](https://www.antrade.io/guide/docs/en/insufficient-api-trading-permissions/)
  * [How Do I Fill in an IP Address in Binance?](https://www.antrade.io/guide/docs/en/ip-address-of-binance/)
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
  * [How to Reduce Fee on Exchange?](https://www.antrade.io/guide/docs/en/reduce-fee-on-exchange/)

## How are AntBot’s Initial Positions Calculated?

3 months ago[AntBot](https://www.antrade.io/guide/docs/en/author/antbot/)1 minute

The position management in AntBot is based on the **ATR** indicator.

**What is ATR？**

&#x20;Average True Range (ATR) is a moving average of the price fluctuation range within a certain period of time.

**How is it calculated?**

The ATR calculation formula is as follows:

**1. True Range (TR):**

TR = MAX (∣highest price – lowest price∣, ∣highest price – yesterday’s closing price∣, ∣yesterday’s closing price – lowest price∣)

**2. Average True Range (ATR):**

ATR = N-day simple moving average of TR

**ATR determines position size.**

It is generally believed that the greater the average volatility ATR of the trading variety, the greater the risk. Therefore, the position ratio should be smaller for varieties with greater volatility.

**Initial Positions = 1% of M\*total fund/ATR**

The variable M in the previous formula depends on the strategy type.

[#AntBot](https://www.antrade.io/guide/docs/en/tag/antbot/)[#Calculate](https://www.antrade.io/guide/docs/en/tag/calculate/)[#Initial Positions](https://www.antrade.io/guide/docs/en/tag/initial-positions/)@AntBot free trading bot\
