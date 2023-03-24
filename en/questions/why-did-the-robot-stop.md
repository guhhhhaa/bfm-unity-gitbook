# Why did the Robot Stop?

[Skip to content](https://www.antrade.io/guide/docs/en/why-did-the-robot-stop/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/en/)[Free AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/en)
* [Questions](https://www.antrade.io/guide/docs/en/en-questions/)
* [Why did the Robot Stop?](https://www.antrade.io/guide/docs/en/why-did-the-robot-stop/)

Search for:

QUESTIONS

*
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
  * [Frequently Asked Questions and Answers](https://www.antrade.io/guide/docs/en/frequently-asked-questions/)
  * [How to Change the Margin Mode of Binance to Cross Margin Mode?](https://www.antrade.io/guide/docs/en/binance-to-cross-margin-mode/)
  * [How to Change Okx’s Margin Mode to Cross Margin Mode?](https://www.antrade.io/guide/docs/en/okx-to-cross-margin-mode/)
  * [Why is My Position Liquidated Even Though My Margin is Sufficient?](https://www.antrade.io/guide/docs/en/position-liquidated-though-sufficient-margin/)
  * [How to Change Binance’s Position Mode to Hedge Mode?](https://www.antrade.io/guide/docs/en/binance-to-hedge-mode/)

## Why did the Robot Stop?

5 months ago[AntBot](https://www.antrade.io/guide/docs/en/author/antbot/)2 minutes

#### Why did the robot stop? <a href="#cvpyee" id="cvpyee"></a>

* **Running Once**\
  You have set a single run for the robot, and the robot has closed the position and stopped running after reaching the take profit condition.\

* **Take Profit**\
  You have set a take-profit for the robot, and the robot has closed the position and stopped running after reaching the total take-profit condition.\

* **Stop Loss**\
  You have set a stop-loss for the robot, and the robot has closed the position and stopped running after reaching the total stop-loss condition.\

* **Close\&Stop**\
  You have manually forcibly ended the robot from running, and the robot has closed the position and stopped running.\

* **Insufficient positions, can not be closing**\
  Your positions on the broker are smaller than the positions recorded by a robot, so the robot cannot close the positions according to the positions recorded by it.\

* **Order not exist**\
  Your positions on the broker have been closed, there are no positions left, and the robot cannot complete the trading for you.\

* **The order’s position side doesn’t match the user’s setting**\
  It usually appears when the AntBot is used for the first time. The reason is that if you have positions of futures account on the broker, the robot cannot help you switch to the Hedge Mode. Please close the positions manually on the broker first, and then try to start the robot again. If the robot still does not work properly, you need to go to the broker to manually set the Hedge Mode of the futures account, and then try to start the robot again.\

* **Crypto has been delisted**\
  The crypto pair has been delisted by the broker, and the robot cannot trade normally.\

* **Unpositioned Error**\
  Unknown reasons cause the robot to fail to trade normally. Please check your trading permissions of the API key on the broker and try restarting the robot again.

[#AntBot](https://www.antrade.io/guide/docs/en/tag/antbot/)@AntBot free trading bot\
