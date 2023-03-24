# What Is the Rebalancing Trading Strategy?

[Skip to content](https://www.antrade.io/guide/docs/en/strategy\_rebalancing/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/en/)[Free AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/en)
* [Strategy](https://www.antrade.io/guide/docs/en/en-strategies/)
* [What Is the Rebalancing Trading Strategy?](https://www.antrade.io/guide/docs/en/strategy\_rebalancing/)

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

## What Is the Rebalancing Trading Strategy?

5 months ago[AntBot](https://www.antrade.io/guide/docs/en/author/antbot/)4 minutes

#### Why Rebalancing? <a href="#78c01n" id="78c01n"></a>

Rebalancing is holding multiple spot assets in a set ratio. When the value of the position exceeds the “Threshold”, the position is sold to a higher value cryptocurrency and the position is bought to a lower value cryptocurrency, returning the portfolio to the initial position.

Rebalancing has the characteristics of investment portfolio, risk diversification and long-term investment.

In the short term, selling high and buying low will make the number of some cryptocurrencys more and the number of some cryptocurrencys less. In view of the sharp rise and fall of the market, through the cryptocurrency portfolio to continuously adjust the position, so that the proportion of value between your multiple cryptocurrencys fluctuates within a certain range, which can effectively avoid the income from fluctuating sharply due to the market.

When the price of a certain cryptocurrency rises strongly, the overall value of the investment portfolio can rise relatively steadily by adjusting the positions to distribute the income to other cryptocurrency in the portfolio; when the price falls, the overall value of the investment portfolio can fall less than a certain cryptocurrency the decline; eventually a relatively stable income.

As market volatility is persistent, your total cryptocurrency holdings will grow.

<figure><img src="https://antrade.io/guide/docs/en/wp-content/uploads/2022/10/What-is-the-Rebalancing-Strategy-0001.png" alt=""><figcaption></figcaption></figure>

**How do I configure a cryptocurrency portfolio in Rebalancing?**

Choose cryptocurrencies that are bullish and hold for the long term.\
Choose cryptocurrencies with volatility.\
Choose cryptocurrencies that are price regressive.\
Choose cryptocurrencies with similar volatility.\
Choose cryptocurrencies that are not in the same field and have large differences in attributes.\
Holding a portfolio of evenly distributed cryptocurrency values.

**What is a reasonable Rebalancing period or “Threshold” setting?**

The setting of the Rebalancing period or “Threshold” needs to refer to the level of the transaction fee, and the higher the general fee, the larger the value of the setting.

AntBot’s Rebalancing bot is completely free, and the exchange’s spot trading fee is generally 0.1% (e.g Binance).

When Rebalancing reaches the condition, it will only sell high and buy low for the part of the portfolio that is out of value, so the trading volume caused by the rebalancing is generally a small part of the position.

The rebalancing ratio of traditional financial products is generally set at 5%-15%. The volatility of cryptocurrencies is relatively high. It is recommended to set it at 10%-20%. The rebalancing ratio must be set according to the properties of different cryptocurrencies.

**Rebalancing parameter configuration description**

AntBot’s rebalancing robot has two modes: creating positions and using original positions.\
We first introduce creating positions. When you choose this method to start the robot, different proportions will be allocated according to different cryptocurrencies, and then the position will be opened.

Allocation method, i.e. the value of each cryptocurrency as a percentage of the total expected investment after the user adds the cryptocurrency. AntBot offers the following 3 ways to allocate the share of each cryptocurrency:

1. Average: distributed equally according to the value of the currency, suitable for cryptocurrency combinations with similar volatility.
2. Market Cap：which refers to the ratio of the circulating market value of each cryptocurrency to the total circulating market value of the selected cryptocurrencies.
3. Volatility: It is the ratio of the true volatility (ATR) of each cryptocurrency to the sum of the true volatility of the selected cryptocurrencies.

Rebalancing Threshold: Reaching this preset value at the latest market price where the difference between the valuation ratio of at least one cryptocurrency and its initial proportion causes a rebalancing action to return to the initial proportional state. The default Rebalancing Threshold is 5%.

<figure><img src="https://antrade.io/guide/docs/en/wp-content/uploads/2022/10/What-is-the-Rebalancing-Strategy-0002.jpg" alt=""><figcaption></figcaption></figure>

In original position mode, the robot will actively read your spot assets on the exchange. The robot only reads assets with a value greater than 200 USDT and then displays the ratio based on the value share. When the robot is activated it will rebalance in the original cryptocurrency by a set percentage.

<figure><img src="https://antrade.io/guide/docs/en/wp-content/uploads/2022/10/What-is-the-Rebalancing-Strategy-0003.jpg" alt=""><figcaption></figcaption></figure>

**References**

[The Rebalancing Bonus— Bernstein](https://www.efficientfrontier.com/ef/996/rebal.htm)

[Diversification, Rebalancing, and the Geometric Mean Frontier — Bernstein](https://poseidon01.ssrn.com/delivery.php?ID=230074113006026025084070079088123026007073086004051025077104114087122066108077111067073126102023048093032025085064026007078125122011083025090094096028102090098028020031069075012078119\&EXT=pdf)

[Case Studies in Rebalancing — Bernstein](https://www.efficientfrontier.com/ef/100/rebal100.htm)

[Portfolio Rebalancing in Theory and Practice — Vanguard](https://personal.vanguard.com/pdf/flgprtp.pdf)

[Value of Rebalancing — Sigma Investing](https://www.sigmainvesting.com/advanced-investing-topics/value-of-rebalancing)

[The Art of Rebalancing — SmithBarney Consulting Group](https://www.retailinvestor.org/pdf/SmithBarney.pdf)

[There is a Rebalancing Bonus (False) — Retail Investor](https://www.retailinvestor.org/why.html#bonus)

[#AntBot](https://www.antrade.io/guide/docs/en/tag/antbot/)[#free](https://www.antrade.io/guide/docs/en/tag/free/)[#rebalancing](https://www.antrade.io/guide/docs/en/tag/rebalancing/)[#strategy](https://www.antrade.io/guide/docs/en/tag/strategy/)[#tradingbot](https://www.antrade.io/guide/docs/en/tag/tradingbot/)@AntBot free trading bot\
