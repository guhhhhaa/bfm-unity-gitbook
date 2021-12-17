# 【软件】行动手册 🚩

{% hint style="success" %}
恭喜有品位的你翻到了这一页！请**仔细阅读**！

你现在是在 BFM Unity Doc **最重要的一页** 上！
{% endhint %}

![我们终于迎来了黎明的曙光](../../.gitbook/assets/u=3153260481,2815876954\&fm=26\&gp=0.jpg)

{% embed url="https://medium.com/@anilpai/currency-arbitrage-using-bellman-ford-algorithm-8938dcea56ea" %}

[https://gist.github.com/anilpai/fe4e11b5c59d8c02813900813396400b](https://gist.github.com/anilpai/fe4e11b5c59d8c02813900813396400b)

[https://gist.github.com/anilpai/dd00a9671c062390c848952eaddbbe1e](https://gist.github.com/anilpai/dd00a9671c062390c848952eaddbbe1e)

> How do we solve this?

### Graph data structure <a href="#297a" id="297a"></a>

Weighted directed graphs can be represented as an **adjacency matrix**. For a graph with _|V| X |V|_ vertices, an **adjacency matrix** is a |V| times |V| matrix of values, where the entry in row _i_ & column _j_ is a non-zero integer if and only if the edge _(i, j)_ is in the graph. If you want to indicate an edge weight, put it in the row _i_, column _j_ entry, and reserve a special value (perhaps `None`) to indicate an absent edge.

### Finding arbitrage <a href="#b951" id="b951"></a>

Arbitrage opportunities arise when a cycle is determined such that the edge weights satisfy the following expression

> _**w1 \* w2 \* w3 \* … \* wn > 1**_

The above constraint of finding the cycles is harder in graphs. Instead we must transform the edge weights of the graph such that the standard graph algorithms can be applied.

Let’s take the logarithm on both sides, such that

> _**log(w1) + log(w2) + log(w3) + … + log(wn) > 0**_

Taking the negative log, this becomes

> _**(-log(w1)) + (-log(w2)) + (-log(w3)) + … + (-log(wn)) < 0**_

Therefore we can conclude that if we can find a cycle of vertices such that the sum of their weights if negative, then we can conclude there exists an opportunity for currency arbitrage. Luckily, Bellman-Ford algorithm is a standard graph algorithm that can be used to easily detect negative weight cycles in O(|V\*E|) time.

### Bellman Ford Algorithm <a href="#fe14" id="fe14"></a>

Let _G(V, E)_ be a graph with vertices, _V_, and edges, _E_.

Let _w(x)_ denote the weight of vertex _x_.

Let _w(i, j)_ denote the weight of the edge from source vertex _i_ to destination vertex _j_.

Let _p(j)_ denote the predecessor of vertex _j_.

The Bellman-Ford algorithm seeks to solve the single-source shortest path problem. It is used in situations where a source vertex is selected and the shortest paths to every other vertex in the graph need to be determined. After applying Bellman-Ford algorithm on a graph, each vertex maintains the weight of the shortest path from the source vertex to itself and the vertex which precedes it in the shortest path. In each iteration, all edges are relaxed if _**\[w(i) + w(i, j) < w(j)]**_ and the weight of each vertex is updated accordingly. After the i-th iteration, the algorithm finds all shortest paths consisting of at most _i_ edges.

Once all shortest paths have been identified, the algorithm loops through all of the edges and looks for edges that can further decrease the value of the shortest path. If we can still relax the edges, then _**a negative weight cycle has been found**_ since a path can have at most |V-1| edges.

Printing a negative weight cycle is done to show the arbitrage opportunity. `We use the predecessor chain to print the cycle.` Now that we have an edge which can be further relaxed, we have found the source & destination vertex of such an edge. `Let’s`` `_**`start from the source vertex and go backwards until you see the source vertex again or any other vertex that predecessor chain has already shown us while printing the negative weighted cycle.`**_

```python
打印"负权环"以显示套利机会。
我们使用"前驱链"打印周期。
现在我们有了可以进一步放松的边缘，我们已经找到了该边缘的源顶点和目标顶点。 
让我们从源顶点开始，然后返回，
直到您再次看到源顶点或在打印"负权环"时"前驱链"已经向我们显示的任何其他顶点。
```

## 我们发现了一个术语叫 predecessor chain，这很重要。

![](<../../.gitbook/assets/屏幕快照 2020-03-25 下午5.59.12.png>)

{% embed url="http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.86.1981&rep=rep1&type=pdf" %}

```python
from typing import Tuple, List
from math import log

rates = [
    [1, 0.23, 0.25, 16.43, 18.21, 4.94],
    [4.34, 1, 1.11, 71.40, 79.09, 21.44],
    [3.93, 0.90, 1, 64.52, 71.48, 19.37],
    [0.061, 0.014, 0.015, 1, 1.11, 0.30],
    [0.055, 0.013, 0.014, 0.90, 1, 0.27],
    [0.20, 0.047, 0.052, 3.33, 3.69, 1],
]

currencies = ('PLN', 'EUR', 'USD', 'RUB', 'INR', 'MXN')


def negate_logarithm_convertor(graph: Tuple[Tuple[float]]) -> List[List[float]]:
    ''' log of each rate in graph and negate it'''
    result = [[-log(edge) for edge in row] for row in graph]
    return result


def arbitrage(currency_tuple: tuple, rates_matrix: Tuple[Tuple[float, ...]]):
    ''' Calculates arbitrage situations and prints out the details of this calculations'''

    trans_graph = negate_logarithm_convertor(rates_matrix)

    # Pick any source vertex -- we can run Bellman-Ford from any vertex and get the right result

    source = 0
    n = len(trans_graph)
    min_dist = [float('inf')] * n

    pre = [-1] * n
    
    min_dist[source] = source

    # 'Relax edges |V-1| times'
    for _ in range(n-1):
        for source_curr in range(n):
            for dest_curr in range(n):
                if min_dist[dest_curr] > min_dist[source_curr] + trans_graph[source_curr][dest_curr]:
                    min_dist[dest_curr] = min_dist[source_curr] + trans_graph[source_curr][dest_curr]
                    pre[dest_curr] = source_curr

    # if we can still relax edges, then we have a negative cycle
    for source_curr in range(n):
        for dest_curr in range(n):
            if min_dist[dest_curr] > min_dist[source_curr] + trans_graph[source_curr][dest_curr]:
                # negative cycle exists, and use the predecessor chain to print the cycle
                print_cycle = [dest_curr, source_curr]
                # Start from the source and go backwards until you see the source vertex again or any vertex that already exists in print_cycle array
                while pre[source_curr] not in  print_cycle:
                    print_cycle.append(pre[source_curr])
                    source_curr = pre[source_curr]
                print_cycle.append(pre[source_curr])
                print("Arbitrage Opportunity: \n")
                print(" --> ".join([currencies[p] for p in print_cycle[::-1]]))


if __name__ == "__main__":
    arbitrage(currencies, rates)

# Time Complexity: O(N^3)
# Space Complexity: O(N^2)
```

## 运行结果：

{% embed url="https://nbviewer.jupyter.org/github/guhhhhaa/TensorAct-of-Stars/blob/main/BFM.ipynb" %}

{% hint style="info" %}
看完之后如果有帮助，请 [**打赏**](https://guhhhhaa.gitbook.io/bfm/juan-zeng) **** 我。
{% endhint %}

{% embed url="https://gist.githubusercontent.com/anilpai/dd00a9671c062390c848952eaddbbe1e/raw/0a65b53371470d7565988e3ec12c0d46f594895e/currency_arbitrage.py" %}

{% hint style="info" %}
现在你能回答以下这几个问题了吗？\
\
1，BFM-find 和 BFM-detect 步骤有什么不同？ \
2，BFM-find 和 BFM-detect 的时间复杂度有什么不同？\
3，BFM-find 里面的步骤涉及前驱链，什么是前驱链? 涉及前驱链的步骤到底做了什么？ \
4，为什么算法运行前要对汇率取-ln？ \
5，为什么汇率在取-ln之前要移动小数点再乘以几百？ \
6，BFM 算法基于图的邻接矩阵表示。什么是图的邻接矩阵表示？BFM 算法的步骤中如何使用图的邻接矩阵表示？&#x20;
{% endhint %}

依然不能？回去，重看：

{% content-ref url="../../bfm-rins.-bi-fang-meng-ke-xue-yan-jiu-yuan/suan-fa-yan-jiu-yuan/what-is-bfm-al/" %}
[what-is-bfm-al](../../bfm-rins.-bi-fang-meng-ke-xue-yan-jiu-yuan/suan-fa-yan-jiu-yuan/what-is-bfm-al/)
{% endcontent-ref %}
