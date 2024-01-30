# 如何获取数字货币数据

{% embed url="https://link.medium.com/acsgXWzBQlb" %}

{% embed url="https://zhuanlan.zhihu.com/p/109021998" %}

The cryptocurrency industry has experienced interest from developers, entrepreneurs, and enthusiasts from around the globe. When Ethereum ERC20 tokens became more popular, the hottest trend was to create a token to be auctioned off within an ICO and traded or used as a utility within projects. This newly discovered wealth creation mechanism helped jumpstart a multitudinous amount of projects, which ultimately led to the great bull run of 2017.

Today, development on the Ethereum blockchain continues to be popular; however, development using cryptocurrency market data is becoming the new crypto gold rush.

Regardless if you are a cryptocurrency trader, speculator, developer, or someone interested in conducting research within cryptocurrency, there are tons of APIs to choose from. Fortunately, I have tested nearly all of the top cryptocurrency APIs and the results are surprising. Whether you want to leverage real-time crypto data to assist with trades, build a trading bot, conduct academic research on cryptocurrency, or learn to code with crypto data, I plan to give you an honest opinion, in the view of your everyday developer, of the APIs I have developed projects with and what I believe will benefit you in the long-term.

Let’s discover the best crypto APIs in the market.

## [LunarCRUSH — Social Listening For Crypto](https://lunarcrush.com/developers/docs) <a href="#3600" id="3600"></a>

![](https://miro.medium.com/max/1400/1\*4BKsaiCby15k7xpcE1p19A.png)

[**LunarCRUSH**](http://lunarcrush.com/) **** provides API endpoints for thousands of crypto assets. This is the same API that drives their [web app](https://lunarcrush.com/developers/widgets). Access over 100 million collected social posts, all classified by coin using artificial intelligence and displayed alongside unique insights. The cryptocurrency focused company collects more than 100,000 social posts with 20,000 links per day and they support more than 2000 cryptocurrencies. LunarCRUSH is known as one the most reliable API for community and social insights.

LunarCRUSH collects data on influencers, social influencer activity and their engagement, frequency, and impact across over thousands of cryptocurrencies. This allows for some pretty awesome things such as how bullish something is vs. bearish. It also lets you know who is really influential vs. a bot. You can also integrate social metrics for over 2,000 coins into your [TradingView charts](https://lunarcrush.com/developers/tradingview). LunarCRUSH has real-time cryptocurrency alerts, LunarAlerts, for notifications on Cryptocurrency prices and social metrics which helps for automating trade decisions.

### LunarCRUSH API Usage <a href="#c517" id="c517"></a>

The LunarCRUSH API allows access to most of the data available on their public [website](http://lunarcrush.com/). Seeing as they provide the largest set of social data available for gathering cryptocurrency data, I will expand on this section with multiple examples.

The base URL Endpoint to use when developing with Python:

[`https://api.lunarcrush.com/v2`](https://lunarcrush.com/developers/docs)

**Assets Endpoint:** Details, overall metrics, and time series metrics for one or multiple assets. We refer to all supported cryptocurrencies as assets.

**Market Endpoint:** Summary information for all supported assets including 5 recent time series values for some metrics.

**Global Endpoint:** Overall aggregated metrics for all supported assets.

**Feeds:** Social posts, news, and shared links for one or multiple coins[.](https://lunarcrush.com/feeds)

**Alerts:** Historical timestamped records of changes in metrics that are notable beyond typical trends including periodical highs, lows, and sudden increases or decreases.

**Influencer:** Individual influencer details including actual posts.

**Influencers:** List of social accounts that have the most influence on different assets based on number of followers, engagements, and volume of posts.

### LunarCRUSH API Documentation <a href="#6574" id="6574"></a>



### Experience With LunarCRUSH <a href="#42dc" id="42dc"></a>

So far so great, right? After testing nearly every crypto data provider I was able to get my hands on, LunarCRUSH API was one of the last ones I tried actually. Sort of like a hidden gem, I found them while browsing tutorials online which ultimately lead to their Twitter, where they are actively posting about crypto data. While I had planned to brush them off as just another API, I decided to look deeper into what they offer. I was especially surprised they provide social metrics, such as bullish and bearish sentiment, along with lists of top [influencers](https://lunarcrush.com/influencers) from social sites.

My initial project was to use their API to gather as much social data as possible and feed the data into an aggregated model with [LunarCRUSH](https://lunarcrush.com/) and [Messari](https://messari.io/) and [Nomics](https://nomics.com/) [Pricing data](https://lunarcrush.com/developers/pricing). I am still currently working on this project which I hope to open source a some point in the future. Feel free to keep a lookout for the project. I expand on my experience with the other two APIs later in this article.

## [Messari](https://messari.io/api) <a href="#bb2e" id="bb2e"></a>

![](https://miro.medium.com/max/1400/1\*XRqWKw3WtOTCCW6qZM2a4g.png)

[Messari](https://messari.io/) provides API endpoints for thousands of crypto assets. These endpoints include trades, market data (VWAP), quantitative metrics, qualitative information. This is the same API that drives their [web app](https://messari.io/). Most of their endpoints are available without an API key, but they limit their rates. The free tier does not include redistribution rights and requires attribution and a link back to their site.

### Messari API Usage <a href="#0b62" id="0b62"></a>

The base URL for their is: `https://data.messari.io/api`, and the endpoints are versioned (v1, v2, etc.) whenever a breaking change is introduced.

### Messari API Documentation <a href="#8517" id="8517"></a>



### Experience With Messari <a href="#2b24" id="2b24"></a>

Generally, Messari is a good API for those looking to build custom solutions. While their site has good information for traders, developing with their API can be challenging. Having a positive spotlight within the crypto community , a few years back decided to try my luck following a Github repo named [‘](https://medium.com/@spenserhuang/exploring-messaris-crypto-api-a7aa2c03fde2)[messari-api-exploration](https://github.com/spenserhuang/messari-api-exploration)[’](https://medium.com/@spenserhuang/exploring-messaris-crypto-api-a7aa2c03fde2). The documentation was very easy to read and it was rather quick for me to figure out the basics of the API. Since then, I have been using their data as a form of validation with Nomics to build out an aggregated crypto data hub.

## [Nomics](https://p.nomics.com/cryptocurrency-bitcoin-api) <a href="#f9e0" id="f9e0"></a>

![](https://miro.medium.com/max/1400/1\*-0E6WlGJw72erxYxbRKF7A.png)

[Nomics ](https://nomics.com/)is a cryptocurrency data API focused on Price, [crypto market cap](https://nomics.com/), supply, and all-time high data. They offer Candle/OHLC data for [currencies](https://nomics.com/) & [exchanges](https://nomics.com/exchanges). Additionally, they supply historical aggregate cryptocurrency market cap since January of 2013.

Nomics API is a resource for all developers. Their prices can seem expensive to the typical developer who is searching for a cheap or free crypto API. Nonetheless, they are a well respected API within the crypto industry.

### Nomics API Usage <a href="#199c" id="199c"></a>

The Nomics API base url runs at `https://api.nomics.com/v1`. All requests should be prefixed by the server URL.

### Nomics API Documentation <a href="#33aa" id="33aa"></a>



### Experience With Nomics <a href="#ebb9" id="ebb9"></a>

An overall positive experience with Nomics lead me to discovering what it has to offer. Nomics API is decently simple to use but when I was starting to build out crypto apps a few years ago, their API was slightly challenging to me. If you want historical candle data for currencies & exchanges, gapless raw trade data, and or order book data then you will need to pay for those services. As discussed in previous sections, I am still using the Nomics API as a form of cryptocurrency market price validation for my aggregated crypto data hub which I hope to open-source in the future.

## [CoinMarketCap](https://coinmarketcap.com/api/) <a href="#3d71" id="3d71"></a>

![](https://miro.medium.com/max/1400/1\*OJihyf96CFB-IEEDQy8\_xg.png)

[CoinMarketCap ](https://coinmarketcap.com/)is commonly known for being the go-to place for checking cryptocurrency and token prices. CoinMarketCap was recently acquired by [Binance](https://binance.com/), an international cryptocurrency exchange founded by Changpeng Zhao in China in 2017.

CoinMarketCap provides API tiers for individual users and business users. The free plan has limitations to how many API calls you can make per month. The functionality is fine for testing but for those attempting to build applications for consumer use then I suggest using an API with [more options](https://lunarcrush.com/developers/docs).

### CoinMarketCap API Usage <a href="#5a72" id="5a72"></a>

Using their API with Python, all requests should target their base URL[`https://pro-api.coinmarketcap.com`](https://pro-api.coinmarketcap.com/)

### CoinMarketCap API Documentation <a href="#a468" id="a468"></a>



### Experience with CoinMarketCap <a href="#fe98" id="fe98"></a>

When initially discovering the power of crypto data, CMC was the first API I was exposed to. My initial attempt to use their data was with a price prediction model, using their free historical data. Unfortunately, after spending a few days working on my project, CMC updated their website so all of my code was no longer working and I did not have the patience to go through developing more code. As of today, my repo no longer works due to changes in their UI. You can view my project [here](https://github.com/nrese).

## [CoinGecko](https://www.coingecko.com/en/api) <a href="#9d1f" id="9d1f"></a>

![](https://miro.medium.com/max/1400/1\*LN4XPDVhNulYzJ5B8PTRSQ.png)

[CoinGecko](https://www.coingecko.com/) provides data for live pricing, trading volume, tickers, exchanges, historical data, coin info & images, developer & community stats, events, global markets, and CoinGecko Beam coins & exchanges status updates directly.

With only 21 endpoints, this may not be the best option for traders and enterprises. I would not recommend using for these purposes. Although CoinGecko is free, it most likely will not meet the needs of traders and exchanges.

### CoinGecko API Usage <a href="#942b" id="942b"></a>

When using the CoinGecko API with Python, you will need to use their base URL [`https://api.coingecko.com/api/v3`](https://api.coingecko.com/api/v3)

### CoinGecko Documentation <a href="#189e" id="189e"></a>



### Experience With CoinGecko <a href="#5f77" id="5f77"></a>

This API was the second API I began developing projects with. The challenges I found while using the CoinGecko was the lack of Python documentation available. I believe CoinGecko has potential being a free API; however, the community needs to step in and provide more documentation for projects. When I was doing initial research on which API I should use for my projects, simply searching ‘CoinGecko Python API’ does not return many results. Luckily, I was able to find a wrapper on Github which helped with implementing into my project. I attempted to follow an open-source project for A Discord bot with multiple features, which can viewed on my [Github](https://github.com/nrese).

## Conclusion <a href="#4686" id="4686"></a>

The cryptocurrency market continues to hit mainstream coverage, increasing exposure, and becoming widely used by the masses. I believe it is important to get a head start in developing applications and conducting analysis within the industry. Crypto data is a valuable asset which can be used to make trades, conduct research experiments, and leverage transparency for your organization. The future of crypto development depends on how many projects will continue to create innovative features within application programming interfaces in 2020.

There are tons of cryptocurrency data api to choose from, sometimes it can feel overwhelming. Picking the best cryptocurrency API all depends on your needs, especially depending on which programming language you plan to use. The majority of APIs provide cryptocurrency price API access, so maybe you want to find one with more than price, like social metrics.

I hope this post helps you decide which data provider is best for your project.

## Thanks For Reading <a href="#9e10" id="9e10"></a>

Questions, comments, and constructive criticism is welcomed. This is one of my first articles published.

Constructive criticism and feedback are welcomed. Nicholas Resendez can be reached on Instagram [@nirholas](http://instagram.com/nirholas?ref=hackernoon.com), on [LinkedIn](http://linkedin.com/in/nixholas?ref=hackernoon.com)**,** and Twitter [@nickresendez ](https://twitter.com/nickresendez)for updates on new articles.



I write on a variety of topics such as cryptocurrency, freelancing, and programming. [instagram.com/nirholas/](http://instagram.com/nirholas/) — [linkedin.com/in/nixholas](http://linkedin.com/in/nixholas) [twitter.com/nickresendez](http://twitter.com/nickresendez)[\
](https://towardsdatascience.com/exploring-the-trump-twitter-archive-6242e5100a74?readmore=1\&source=follow\_footer-----32475d2eb749----0-------------------------------)
