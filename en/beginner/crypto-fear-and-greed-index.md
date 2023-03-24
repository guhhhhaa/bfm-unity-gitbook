# Crypto Fear & Greed Index

[Skip to content](https://www.antrade.io/guide/docs/en/fear-and-greed-index/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/en/)[Free AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/en)
* [Beginner](https://www.antrade.io/guide/docs/en/en-beginner/)
* [Function](https://www.antrade.io/guide/docs/en/en-function/)
* [Crypto Fear & Greed Index](https://www.antrade.io/guide/docs/en/fear-and-greed-index/)

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

## Crypto Fear & Greed Index

4 months ago[AntBot](https://www.antrade.io/guide/docs/en/author/antbot/)4 minutes

This is a plot of the Fear & Greed Index over time, where a value of 0 means “Extreme Fear” while a value of 100 represents “Extreme Greed”.

<figure><img src="https://www.antrade.io/guide/docs/en/wp-content/uploads/2023/02/1675845194517.png" alt=""><figcaption></figcaption></figure>

### Why Measure Fear and Greed?

The crypto market behaviour is very emotional. People tend to get greedy when the market is rising which results in FOMO (Fear of missing out). Also, people often sell their coins in irrational reaction of seeing red numbers. With our Fear and Greed Index, we try to save you from your own emotional overreactions. There are two simple assumptions:

* **Extreme fear** can be a sign that investors are too worried. That could be a **buying opportunity**.
* When Investors are getting **too greedy**, that means the market is **due for a correction**.

Therefore, we analyze the current sentiment of the Bitcoin market and crunch the numbers into a simple meter from 0 to 100. Zero means “Extreme Fear”, while 100 means “Extreme Greed”. See below for further information on our data sources.

### Data Sources

We are gathering data from the five following sources. Each data point is valued the same as the day before in order to visualize a meaningful progress in sentiment change of the crypto market.

First of all, the current index is for bitcoin only (we offer separate indices for large alt coins soon), because a big part of it is the volatility of the coin price.

But let’s list all the different factors we’re including in the current index:

#### Volatility (25 %)

We’re measuring the current volatility and max. drawdowns of bitcoin and compare it with the corresponding average values of the last 30 days and 90 days. We argue that an unusual rise in volatility is a sign of a fearful market.

#### Market Momentum/Volume (25%)

Also, we’re measuring the current volume and market momentum (again in comparison with the last 30/90 day average values) and put those two values together. Generally, when we see high buying volumes in a positive market on a daily basis, we conclude that the market acts overly greedy / too bullish.

#### Social Media (15%)

While our reddit sentiment analysis is still not in the live index (we’re still experimenting some market-related key words in the text processing algorithm), our twitter analysis is running. There, we gather and count posts on various hashtags for each coin (publicly, we show only those for Bitcoin) and check how fast and how many interactions they receive in certain time frames). A unusual high interaction rate results in a grown public interest in the coin and in our eyes, corresponds to a greedy market behaviour.

#### Surveys (15%) currently paused

Together with strawpoll.com (disclaimer: we own this site, too), quite a large public polling platform, we’re conducting weekly crypto polls and ask people how they see the market. Usually, we’re seeing 2,000 – 3,000 votes on each poll, so we do get a picture of the sentiment of a group of crypto investors. We don’t give those results too much attention, but it was quite useful in the beginning of our studies. You can see some recent results here.

#### Dominance (10%)

The dominance of a coin resembles the market cap share of the whole crypto market. Especially for Bitcoin, we think that a rise in Bitcoin dominance is caused by a fear of (and thus a reduction of) too speculative alt-coin investments, since Bitcoin is becoming more and more the safe haven of crypto. On the other side, when Bitcoin dominance shrinks, people are getting more greedy by investing in more risky alt-coins, dreaming of their chance in next big bull run. Anyhow, analyzing the dominance for a coin other than Bitcoin, you could argue the other way round, since more interest in an alt-coin may conclude a bullish/greedy behaviour for that specific coin.

#### Trends (10%)

We pull Google Trends data for various Bitcoin related search queries and crunch those numbers, especially the change of search volumes as well as recommended other currently popular searches. For example, if you check Google Trends for “Bitcoin”, you can’t get much information from the search volume. But currently, you can see that there is currently a **+1,550%** rise of the query **“bitcoin price manipulation**”  in the box of related search queries (as of 05/29/2018). This is clearly a sign of fear in the market, and we use that for our index.

[#Fear Greed Index](https://www.antrade.io/guide/docs/en/tag/fear-greed-index/)[#market sentiment index](https://www.antrade.io/guide/docs/en/tag/market-sentiment-index/)[#MSI](https://www.antrade.io/guide/docs/en/tag/msi/)@AntBot free trading bot\
