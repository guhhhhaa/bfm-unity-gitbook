# MVRV-被折叠

#### [原始策略](https://share.weiyun.com/a0QaKX11)（[介绍视频](https://www.bilibili.com/video/BV1uA411g7Sn)）

![](../.gitbook/assets/mvrv-jian-ban-.png)

![](../.gitbook/assets/mvrv-jian-ban-.png)

![](../.gitbook/assets/mvrv.png)

MVRV 由两部分组成，市值（MV）和实现市值（RV），是二者的比率。市值好理解，理解实现市值是理解这个指标的关键。

实现市值是指市场中比特币 UTXO （产生时）的价格的总和，大体体现了市场参与者的持币成本——交易所的交易不完全体现为 UTXO 的变动，因此这里只能是"大体体现"。

MVRV 可以简单地理解为目前的市场价格和成本的比率。

| MVRV | 1 | 3 | 4 | x |
| :--- | :--- | :--- | :--- | :--- |
|  | 0 | 2 | 3 | x-1 |
|  | 4 | 2 | 1 | 4-x+1 |
|  | 2 | 1 | 0 | LOG\(4-x+1,2\) |
|  | 0 | 1 | 2 | 2-LOG\(4-x+1,2\) |
|  | 0 | 1 | 4 | POWER\(2-LOG\(4-x+1,2\)\) |
|  | 0 | 0.25 | 1 | 1-y=\(POWER\(2-LOG\(4-x+1,2\),2\)/4\) |
| 仓位牛 | **1** | 0.75 | 0 | y\_BULL=1-\(POWER\(2-LOG\(4-x+1,2\),2\)/4\) |
|  |  |  |  |  |
|  | 1 | 2 | 4 | x |
|  | 0 | 1 | 2 | LOG\(x,2\) |
|  | 2 | 1 | 0 | 2-LOG\(x,2\) |
|  | 4 | 1 | 0 | 4\*y=POWER\(2-LOG\(x,2\),2\) |
| 仓位1 | 1 | 0.25 | 0 | y1=POWER\(2-LOG\(x,2\),2\)/4 |
|  |  |  |  |  |
| MVRV | 1 | 1.5 | 4 | x |
|  | 6 | 5 | 0 | 8-2\*x |
|  | 4096 | 1024 | 1 | POWER\(8-2\*x,4\) |
| 仓位2 | 1 | 0.25 | ≈0 | y2=POWER\(8-2\*x,4\)/4096 |
|  |  |  |  |  |
| 仓位熊 |  |  |  | y\_BEAR=\(3\*y1+2\*y2\)/5 |

## BFM Unity 的 MVRV 评级：（以四分之一为准）

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#x65F6;&#x95F4;</th>
      <th style="text-align:left">2021.
        <br />1.11</th>
      <th style="text-align:left">2021.
        <br />1.11</th>
      <th style="text-align:left">
        <p>2021.</p>
        <p>1.21</p>
      </th>
      <th style="text-align:left">
        <p>2021.</p>
        <p>1.27</p>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">&#x8BC4;&#x7EA7;</td>
      <td style="text-align:left">B</td>
      <td style="text-align:left">C</td>
      <td style="text-align:left">C</td>
      <td style="text-align:left">C</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">&#x4ED3;&#x4F4D;</td>
      <td style="text-align:left">25%</td>
      <td style="text-align:left">0</td>
      <td style="text-align:left">2.53%</td>
      <td style="text-align:left">4.36%</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

