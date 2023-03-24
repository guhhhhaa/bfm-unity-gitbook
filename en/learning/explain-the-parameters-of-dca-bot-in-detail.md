# Explain the Parameters of DCA Bot in Detail

[Skip to content](https://www.antrade.io/guide/docs/en/parameters\_dca/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/en/)[Free AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/en)
* [Learning](https://www.antrade.io/guide/docs/en/en-learning/)
* [Explain the Parameters of DCA Bot in Detail](https://www.antrade.io/guide/docs/en/parameters\_dca/)

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

## Explain the Parameters of DCA Bot in Detail

5 months ago[AntBot](https://www.antrade.io/guide/docs/en/author/antbot/)5 minutes

<figure><img src="https://antrade.io/guide/docs/en/wp-content/uploads/2022/11/4498dc5bed674b3d13637e08c59430d.jpg" alt=""><figcaption></figcaption></figure>

**Long**

Robots that run long positions.

**Short**

Robots that run short positions.

**Shock**

Robots that run **long** and **short** positions at the same time.

**Leverage**

Using leverage can be regarded as borrowing funds from the exchange to hold positions. The multiple of this position funds relative to the principal is the leverage, and increasing leverage will magnify profits and losses. It is recommended to keep the default value of 5x leverage for beginners.

**Initial Positions**

The size of the initial positions opened by the bot from the state of unopened position. It is recommended to keep the default value for beginners .

**Max Positions**

That is, the total position amount after completing the “Max Order”.

**Cycle**

The positions will be opened repeatedly after closing positions to take profits each time.Only after reaching the take-profit or stop-loss in “Optional” setting  will the bot stop.

**Single**

The bot will automatically stop after taking profits on all positions.

**Risk**

The greater the risk, the greater the price gap and take-profit percentage, and the risk level is radical > steady > conserv.&#x20;

**Max Order**

It is the max number that bots are allowed to increase positions consecutively from the state of unopened position.

**Multiples**

The next opening amount is a certain multiple of the current opening amount.It means: the next opening amount = the current opening amount X “Multiples”.

**Price Gap (%)**

Taking a long bot as an example,the positions will be increased if the market price falls by this preset percentage referring to the last opening price,otherwise,for short bots,the positions will be increased if the market price rises by this preset value. (It can be used in conjunction with “Trailing Stop”)

**Trailing Stop(%)**

Take the long bot as an example,The positions will be increased when the market price retraces from the newly lowest price with the retracement percentage reaching the preset value and the market price meets the price gap percentage at the same time; For the short bot, the short positions will be increased when the market price retraces from the newly highest price  with the retracement percentage reaching the preset value and the market price meets the price gap percentage at the same time.

**Take-Profit(%)**

When the returns of the bot’s positions reach the preset value, the positions will be closed to take profits, and the bot will enter the next cycle. (Can be used in conjunction with “Trailing Profit”)

**Trailing Profit (%)**

Take the long bot as an example,The positions will be closed when the market price retraces from the newly highest price with the retracement percentage reaching the preset value and the market price meets the take-profit percentage at the same time; For short bot, the short positions will be closed when the market price retraces from the newly lowest price with the retracement percentage reaching the preset value and the market price meets the take-profit percentage at the same time.

**Price Ceiling**

When the market price is higher than this preset price, the long and short bots will not open a position, but will only close a position, and the bot will not open positions until the price falls back to the preset price.

**Price Floor**

When the market price falls below this preset price, the long and short bots will not open positions, but will only close positions, and the bot will not open positions until the price rises back to the preset price.

**Double Opening**

Each time the bot will open a position at double the amount of the initial position in preset from the state of unopened position.It should be noted that increasing positions subsequently is also calculated by original initial position,which can obviously increase returns in the weak oscillation market.

**Smart  Increase**

If the current positions exceeds 25% of the expected investment and even if the market price reaches the condition for increasing the positions, the AI system will not increase the positions immediately.It is necessary to wait for the MACD indicator (4 hours) to see a stalemate or reversal of long/short power before increasing positions.

**Take-Profit by Percent**

The bot will automatically close the positions to take profits and stop if the market price is higher than the preset price for a long position bot or if the market price is lower than the preset price for a short position bot.

**Stop-Loss by Percent**

The bot will automatically close the positions to stop loss and stop if the market price is lower than the preset price for a long position bot or if the market price is higher than the preset price for  a short position bot.

**Take-Profit by Amount**

Realized PnL + floating PnL > the  preset amount, the bot that meets above conditions will automatically close the positions and stop.

**Stop-Loss by Amount**

Floating PnL < negative value of this preset amount, the robot  that  meets  above conditions  will automatically close the positions to stop loss and  stop.

[#AntBot](https://www.antrade.io/guide/docs/en/tag/antbot/)[#bot](https://www.antrade.io/guide/docs/en/tag/bot/)[#DCA](https://www.antrade.io/guide/docs/en/tag/dca/)[#Martingale](https://www.antrade.io/guide/docs/en/tag/martingale/)[#Stop-Loss](https://www.antrade.io/guide/docs/en/tag/stop-loss/)[#strategy](https://www.antrade.io/guide/docs/en/tag/strategy/)[#Take-Profit](https://www.antrade.io/guide/docs/en/tag/take-profit/)@AntBot free trading bot\
