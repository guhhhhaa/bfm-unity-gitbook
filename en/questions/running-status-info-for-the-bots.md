# Running Status Info for the Bots

[Skip to content](https://www.antrade.io/guide/docs/en/running-status/#content)[AntBot | Crypto Trading Bot](https://www.antrade.io/guide/docs/en/)[Free AntBot](https://antrade.io/)

* [Home](https://www.antrade.io/guide/docs/en)
* [Questions](https://www.antrade.io/guide/docs/en/en-questions/)
* [Running Status Info for the Bots](https://www.antrade.io/guide/docs/en/running-status/)

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

## Running Status Info for the Bots

5 months ago[AntBot](https://www.antrade.io/guide/docs/en/author/antbot/)3 minutes

#### Running Status Info for the Bots <a href="#8cy1sa" id="8cy1sa"></a>

* **Waiting to open**\
  The bot is in the monitoring state, and the position will be opened after a short while.
* **Running**\
  The robot runs everything fine.
* **Smaller Position**\
  The position size recorded by the bot is inconsistent with the actual position size of the exchange. The reason is that the user manually reduced or closed all positions from the exchange. In this case, it is recommended to restart the bot after performing the “Stop” operation on the bot.
* **Insufficient Margin**\
  When this status appears, it means that your margin balance in the exchange futures account is insufficient and the bot can no longer open positions. It is recommended that you go to the exchange to increase your margin to avoid the risk of liquidation.
* **Insufficient USDT**\
  When this status appears, it means that your USDT in the spot account of the exchange is insufficient, and the bot can no longer carry out buying operations. It is recommended to go to the exchange to recharge USDT, or wait for the position to decrease to free up the available funds.
* **Max Positions**\
  “Spot/Futures Position” is about to reach “Max pos of Spot/Futures”. Spots will no longer be bought and futures will no longer be opened. Note: When “Near’maximum allowed position’\nNo longer opens positions” is displayed, there may be a gap between “Spot/Futures Position” and “Max pos of Spot/Futures”. This is normal because of “If you fill it in, it will exceed “Max pos of Spot/Futures”.
* **Price Ceiling**\
  When the currency price breaks the “Price Ceiling”, the bot will no longer open or cover positions. When this state occurs, the bot that supports the AI strategy will automatically adjust the Price Ceiling.\
  Bots with non-AI strategies can manually modify the “Price Ceiling”.
* **Max Oders**\
  The number of orders has been used up, and there will be no more replenishment. Users are required to judge whether they need to increase the number of orders based on their available funds and market conditions.
* **Trading Limit**\
  When this state occurs, it is generally because the current position is close to the maximum position limit of the exchange, and the position can no longer be covered, but the position can only be closed. You can continue to wait for the automatic liquidation to be triggered after the take profit condition is reached, or you can contact AntBot online support for help.
* **Trading Error**\
  This status cannot be automatically repaired. Generally, the exchange has rejected the transaction request and the robot cannot trade normally. Please contact AntBot online support for help.
* **Price Floor**\
  When the currency falls below the “Price Floor”, the bot will no longer open or cover positions. When this state occurs, the bot that supports the AI strategy will automatically adjust the price floor.\
  Bots with non-AI strategies can manually modify the “Price Floor”.
* **Waiting Covering**\
  When this state occurs, the position replenishment will be suspended, and the position will be replenished after waiting for the general trend to change.

[#AntBot](https://www.antrade.io/guide/docs/en/tag/antbot/)@AntBot free trading bot\
