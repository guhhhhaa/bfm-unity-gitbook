# 卓尔金升级A2——参数读取

{% hint style="info" %}
### 参数读取由 [CryptoSheets](https://app.cryptosheets.com/) 和 [GlassNode](https://studio.glassnode.com/settings/api) 支持

未来考虑增加 [https://sheets.santiment.net/](https://sheets.santiment.net/) 的支持
{% endhint %}

【链接】HowtopullCCXTdataintoExcelandGoogleSheets [https://docs.cryptosheets.com/providers/ccxt/](https://docs.cryptosheets.com/providers/ccxt/)

[https://store.office.com/addinsinstallpage.aspx%3Frs=en-US\&assetid=WA104381695\&ui=en-US\&ad=US](https://store.office.com/addinsinstallpage.aspx%3Frs=en-US\&assetid=WA104381695\&ui=en-US\&ad=US)

[https://docs.cryptosheets.com/cryptosheets-concepts/beginner-tutorial/](https://docs.cryptosheets.com/cryptosheets-concepts/beginner-tutorial/)

[https://docs.cryptosheets.com/functions/querya/](https://docs.cryptosheets.com/functions/querya/)

[https://docs.cryptosheets.com/providers/glassnode/mvrv-z-score/](https://docs.cryptosheets.com/providers/glassnode/mvrv-z-score/)

[https://docs.cryptosheets.com/providers/cryptoquant/btc-mvrv/](https://docs.cryptosheets.com/providers/cryptoquant/btc-mvrv/)

[https://docs.cryptosheets.com/providers/glassnode/stock-to-flow-ratio/](https://docs.cryptosheets.com/providers/glassnode/stock-to-flow-ratio/)

[https://docs.cryptosheets.com/providers/glassnode/stock-to-flow-deflection/](https://docs.cryptosheets.com/providers/glassnode/stock-to-flow-deflection/)

[http://help.cryptosheets.com/en/articles/3499319-troubleshooting-cannot-log-in-or-you-are-not-logged-in-and-other-login-errors](http://help.cryptosheets.com/en/articles/3499319-troubleshooting-cannot-log-in-or-you-are-not-logged-in-and-other-login-errors)

{% hint style="info" %}
准备发起一个新活动，

目标是对接CryptoSheets。

1，练手：通过CryptoSheets读取各个币种对美元，人民币，比特币和以太坊的价格（群主已完成）

[http://help.cryptosheets.com/en/articles/4448907-what-s-the-difference-between-cs-exrate-vs-cs-price-vs-cs-pricea](http://help.cryptosheets.com/en/articles/4448907-what-s-the-difference-between-cs-exrate-vs-cs-price-vs-cs-pricea)

2，市值：通过CryptoSheets读取各个币种的美元市值（实时），输出到Excel表格。（通过[https://app.cryptosheets.com/#/templates/133](https://app.cryptosheets.com/#/templates/133)已完成）

[https://cryptosheets.com/templates](https://cryptosheets.com/templates)

[https://app.cryptosheets.com/#/browse/templates](https://app.cryptosheets.com/#/browse/templates)

3，MVRV：通过CryptoSheets读取BTC的MVRV（当日），输出到Excel表格。(已完成)

[https://docs.cryptosheets.com/scenarios/marketcap-metrics---realized,-mvrv-and-basic-historical-marketcap/](https://docs.cryptosheets.com/scenarios/marketcap-metrics---realized,-mvrv-and-basic-historical-marketcap/)

4，S2F：通过CryptoSheets读取BTC的S2F（当日），输出到Excel表格。

5，增加交易所排名支持

[https://app.cryptosheets.com/#/templates/428](https://app.cryptosheets.com/#/templates/428)
{% endhint %}

* [Unix时间与Excel时间转换](https://blog.csdn.net/flora\_zhl/article/details/73920260)
* [通过Excel将Unix时间转换为日期时间](https://www.it1352.com/2037257.html)

| ![](https://ci3.googleusercontent.com/proxy/mIahoxuhPjkwSlmSzsvmRrjoiF85TWP8\_HExCs5vLImyD0oAkHw9-8oy\_fyRI4VXzxF2MD8vrl3QvVnaxn6XqpySq1Sx6rrrg6eYK6901klaUQobxjZ3LP3Bf5-Gz440z6dQLNAj\_h1Va-e1t9vuU8XN=s0-d-e1-ft#https://cryptosheets.intercom-mail.com/i/o/163477801/e3239dd408a0f426c81e40be/File1573823790483) |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

|

Hi there,

## Refreshing Crypto API Data in Cryptosheets

\
![👉](https://fonts.gstatic.com/s/e/notoemoji/14.0/1f449/72.png) It's easy to refresh data with Cryptosheets and there are a number of different methods for both [Excel](https://cryptosheets.intercom-clicks.com/via/e?ob=dpNFJpA05C1%2BKysb%2Fo1pR18Yi5tfaM2nMFyRNYlmmLOoc82brdXNDa6vfEAzEHeHMDAh%2BTXQexalwHMA3W9WmBKiPFG2ikAjCr0e09k1%2FAtZZCL2URqUQzu8ZgRirvb7ygAUugzu6xlf0oRO2%2BBc1xT1RnKaFicQtOykHwv1l65UxwDihvDzwflehTRkX7ZG\&h=9123addc1eac27a678e297770eb0008262102047-w1ppxcjb\_98178001422580\&l=cea91ab435d7b2e567051fba18d22d53ad7f6473-10924630) & [Googlesheets](https://cryptosheets.intercom-clicks.com/via/e?ob=vqJYWGSOSCthykQzXu6JvhJ0m%2BN4iq%2BPoPyBKkE48yDcyHe77%2ByRokFcgW9V15U0VsiM5FAhZNKAUFj2nE0ReSs77KOImgVvV6tpuApg6EIgjQ5ulxq1nUmF%2FW9RcK6OV7C9N2HkG0lMlSY39KGtj6BCp5l0oyPHGTPMdIF%2Fk9wCq1LiBrRG46VtL3i57fK2\&h=484961ee63b0f5137eeba1966a18ab46a4b3bc6e-w1ppxcjb\_98178001422580\&l=5ffe088f06ec14104154cf671383ad4c972bf760-10924631).

We have several resources to help you understand and learn how to choose which method to use

* **Docs portal:** [Data refresh concepts](https://cryptosheets.intercom-clicks.com/via/e?ob=kKdxjVB4gYnhMEq7Zlnt1laBQ7W8tC%2FFDnFXaI4kYywzhYpzJ0eg9rr5CL20TBdpY8RCKDe%2B7pLz4e%2FJG2cZdzYxovWnSbt3aCMCqAiVxuE%3D\&h=2ccabdc34f23a7d428e7dc89eb15cc80958b0b7a-w1ppxcjb\_98178001422580\&l=4770d824d7e9b778f49e4f092901c9338471f79c-10924632)
* **YouTube:** [Refreshing Crypto API Data playlist channel](https://cryptosheets.intercom-clicks.com/via/e?ob=ext542A0w%2BFEejiKaDnA3n4Inlczal0iZ%2BnK2TgCzWnQbqIhd%2B0%2F%2BEpl%2B1d5s1Bpl0nWU79PnfL5eB3HQUP%2ByHwxDOkGqglDResAQhQilX0%3D\&h=c7d209bdb4a3569821667602e61651d92d5d5902-w1ppxcjb\_98178001422580\&l=bc7bc5061006db0d90dfbd823e8b5c2a5cb513ca-10924633)\
  _Make sure to subscribe to our YouTube channel to receive the latest examples and tutorials for how to refresh data_
* **Medium Blog**: [Focus articles on refreshing data](https://cryptosheets.intercom-clicks.com/via/e?ob=HHCGwsFeUzdyBfOUyJNBFc8%2FcYuaUNufyhzsAov4riEgn7BdkLejg3tywkvza3Hfdpdl41PUe6Cy47%2F%2FprqlPHSbpduENod9ArFiuXJwwZs0vepkpWuQGkveXkwvPPq8CJaHLhNsjWuFg9FPdP9bwy1VdTCFZj6NVOfhA83btbY0CiAUYuG6noQvQOv92Jv2\&h=706ca5267296c8fb2cbda18ca2848547e263112d-w1ppxcjb\_98178001422580\&l=a207748c530ea8b58e9e36e32072161c9599f366-10924634) & [tutorials for real time dashboards](https://cryptosheets.intercom-clicks.com/via/e?ob=h02zjA6VYVfvkYffTfFeXKSYSrfzVcIe8CqjC9uELc2JLU2gOLSPbmE7VZTW05X6fg4ITTz%2Bj5fzcfhWr%2B6OIEPdfAImDS4Lg%2B2IevfIyC%2BgJkLTGGahjEqApig10lL7qA81aK%2BpUjvqBiWpK1ziUO%2BmeBLCV0CNdJlYKlhp3SE%3D\&h=02d3abc879d9fde87fb25adbafd6830246c06a5d-w1ppxcjb\_98178001422580\&l=a931ed836a51cb1a887e9db6a936840e381124a9-10924635)

## Try some quick data refresh examples

_Excel & Google Sheets refresh capabilities are slightly different so checkout examples for both with Google Sheets examples at the bottom of this email._

### [Excel](https://cryptosheets.intercom-clicks.com/via/e?ob=dpNFJpA05C1%2BKysb%2Fo1pR18Yi5tfaM2nMFyRNYlmmLOoc82brdXNDa6vfEAzEHeHMDAh%2BTXQexalwHMA3W9WmBKiPFG2ikAjCr0e09k1%2FAtZZCL2URqUQzu8ZgRirvb7ygAUugzu6xlf0oRO2%2BBc1xT1RnKaFicQtOykHwv1l65UxwDihvDzwflehTRkX7ZG\&h=9123addc1eac27a678e297770eb0008262102047-w1ppxcjb\_98178001422580\&l=cea91ab435d7b2e567051fba18d22d53ad7f6473-10924630)

![✅](https://fonts.gstatic.com/s/e/notoemoji/14.0/2705/72.png) _Paste or type these formulas into any cell_\


### EXAMPLE 1

```
 =CS.EXRATE("BTC","USD",1)
```

[![](https://ci3.googleusercontent.com/proxy/BEBVs-iG1IE3Fs2ohdwVPCJgusgm3zR3pS3347coHmcmxwngn7MhD4DmnIk3Wi40TlYr3G8MuqJXnnoKrYlmojiYGW93sXH36EuSG3afZ9M9aLUVvWEgU5LUf4gK7Po-mWSpCPinyIQmyxM2GXCrGVX5OpZnwH4MADbsY6569uB5LHy1FerTIMZurg99ghQwzo3qZA7ylImz5Y8ZlwdcVg=s0-d-e1-ft#https://cryptosheets.intercom-mail.com/i/o/246207473/5359446bf38be6e50bbe465b/cryptosheets-docs\_excel\_functions\_csEXRATE-example5%5B1%5D.gif)](https://cryptosheets.intercom-clicks.com/via/e?ob=dpNFJpA05C1%2BKysb%2Fo1pR18Yi5tfaM2nMFyRNYlmmLOoc82brdXNDa6vfEAzEHeHMDAh%2BTXQexalwHMA3W9WmBKiPFG2ikAjCr0e09k1%2FAtZZCL2URqUQzu8ZgRirvb7ygAUugzu6xlf0oRO2%2BBc1xT1RnKaFicQtOykHwv1l65UxwDihvDzwflehTRkX7ZG\&h=9123addc1eac27a678e297770eb0008262102047-w1ppxcjb\_98178001422580\&l=25dc78d22b54724fc7213ede45dcdb961d625dbb-10924636)

### EXAMPLE 2

```
 =CS.PRICEA("base","BTC","quote","USD",A1,B1)
```

[![](https://ci4.googleusercontent.com/proxy/yPcyK7VIIYGQtXsBZQmOPm3yt1TUwnoNGr1j1ChhfmmdPG\_CvASE8LlPSi1rlrW\_oYOhMxVcHW94VfeiTLP45lOjYoyFiPRzyiTyXCEZBK6d0UJ\_Wbbz8YOq-yNyJogtMR4kmh7bruqqdnsFsNS4mondI\_hyzlAFm1Sv79AHPbScZ9Wt8MNP2VCdN32PpnoDAdz8a\_hTsCiYgaOzpip9qaZLDw9fjKnqd2ah\_Ww7DcORAXnVeAmpvDVrgT8=s0-d-e1-ft#https://cryptosheets.intercom-mail.com/i/o/260279717/39bbb3fcab5724a29f95aaea/YT-1355-3873\_cryptosheets-docs\_providers\_cryptosheets\_console\_csPRICEA-example6%5B1%5D.gif)](https://cryptosheets.intercom-clicks.com/via/e?ob=ext542A0w%2BFEejiKaDnA3n4Inlczal0iZ%2BnK2TgCzWnQbqIhd%2B0%2F%2BEpl%2B1d5s1Bpl0nWU79PnfL5eB3HQUP%2ByHwxDOkGqglDResAQhQilX0%3D\&h=c7d209bdb4a3569821667602e61651d92d5d5902-w1ppxcjb\_98178001422580\&l=1ef294789cc426d360384e70e8d6e9e2912f50da-10924637)

### EXAMPLE 3

```
 =CS.OHLCVA("base","BTC","quote","USD","refresh",CS.TIME(10))
```

![](https://ci3.googleusercontent.com/proxy/qPaq6jjUAmpfNxYoGjvygRq3I1IgmXkhJ7f03SwWUgL70RDtie5\_3p1hq15WVmFM15Ypua86QCp-h\_n5mm2wDTfyIH7Gf7HLAooWpXEzWJU9J-aWkZuP8yIoHjl7j6Q5KzMf8XPfdU6SOoSreWtpOYGDg8pQtaGQ9Bmwx8UgLGT1ytl5pnZwiHHkhLWN135F-r16-LVRg5P3=s0-d-e1-ft#https://cryptosheets.intercom-mail.com/i/o/246216883/546e1044e001261bca970af6/cryptosheets-docs\_excel\_functions\_csOHLCVA-example2.gif)

_\*_[_CS.TIME_](https://cryptosheets.intercom-clicks.com/via/e?ob=jBWl7I74XD9EF%2FyKqAjyXWg%2BqDx8taFJ0VsK5IdKRK7TpFXWwKdl9stJ80jYTzaP\&h=3d0fcfeba9020a97c31668c3b9a3defb8f8750bb-w1ppxcjb\_98178001422580\&l=516b2f38b0eecab0c5695bebdc620c2cd16c6ec2-10924638) _is only available for_ [_paid subscriptions - upgrade today!_](https://cryptosheets.com/pricing)\


### [Googlesheets](https://cryptosheets.intercom-clicks.com/via/e?ob=vqJYWGSOSCthykQzXu6JvhJ0m%2BN4iq%2BPoPyBKkE48yDcyHe77%2ByRokFcgW9V15U0VsiM5FAhZNKAUFj2nE0ReSs77KOImgVvV6tpuApg6EIgjQ5ulxq1nUmF%2FW9RcK6OV7C9N2HkG0lMlSY39KGtj6BCp5l0oyPHGTPMdIF%2Fk9wCq1LiBrRG46VtL3i57fK2\&h=484961ee63b0f5137eeba1966a18ab46a4b3bc6e-w1ppxcjb\_98178001422580\&l=5ffe088f06ec14104154cf671383ad4c972bf760-10924631)

![✅](https://fonts.gstatic.com/s/e/notoemoji/14.0/2705/72.png) _Paste or type these formulas into any cell_

### EXAMPLE 4

```
 =CSPRICE("BTC","USD",,"Coinbase","ask",GOOGLEFINANCE("CURRENCY:USDEUR"))
```

[![](https://ci3.googleusercontent.com/proxy/GPqFjLR33wPQwK8vrEpFiRkDUquMPoZNUuh60YKyUkSIgFkgUb3fnz97c1eodsRD8w9w-JpBbgdIo\_nvkc9X-onI4CQ5sICZOinsa\_dSKDpFl\_V8s\_Hzwwn4W586FHjmgMCCs44DLNwcAg=s0-d-e1-ft#https://cryptosheets.intercom-mail.com/i/o/246206395/2b52e9967491a70de99f8e18/image.png)](https://cryptosheets.intercom-clicks.com/via/e?ob=vqJYWGSOSCthykQzXu6JvhJ0m%2BN4iq%2BPoPyBKkE48yDcyHe77%2ByRokFcgW9V15U0VsiM5FAhZNKAUFj2nE0ReSs77KOImgVvV6tpuApg6EIgjQ5ulxq1nUmF%2FW9RcK6OV7C9N2HkG0lMlSY39KGtj6BCp5l0oyPHGTPMdIF%2Fk9wCq1LiBrRG46VtL3i57fK2\&h=484961ee63b0f5137eeba1966a18ab46a4b3bc6e-w1ppxcjb\_98178001422580\&l=b1fcf70edbb8b7137237de913f3754758ea81f66-10924640)

_\*Fastest refresh interval_ [_using this method_](https://cryptosheets.intercom-clicks.com/via/e?ob=HHCGwsFeUzdyBfOUyJNBFc8%2FcYuaUNufyhzsAov4riEgn7BdkLejg3tywkvza3Hfdpdl41PUe6Cy47%2F%2FprqlPHSbpduENod9ArFiuXJwwZs0vepkpWuQGkveXkwvPPq8CJaHLhNsjWuFg9FPdP9bwy1VdTCFZj6NVOfhA83btbY0CiAUYuG6noQvQOv92Jv2\&h=706ca5267296c8fb2cbda18ca2848547e263112d-w1ppxcjb\_98178001422580\&l=a207748c530ea8b58e9e36e32072161c9599f366-10924634) _is \~2 minutes_

### EXAMPLE 5

```
 =CSPRICEA("base","BTC","quote","USD","refresh",A1)











```
