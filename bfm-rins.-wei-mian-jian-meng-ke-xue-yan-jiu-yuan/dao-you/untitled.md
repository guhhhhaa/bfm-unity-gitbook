# 【软件】Graph algorithms and currency arbitrage

{% embed url="https://reasonabledeviations.com/2019/03/02/currency-arbitrage-graphs/" %}

{% embed url="https://reasonabledeviations.com/2019/04/21/currency-arbitrage-graphs-2/" %}

## Graph algorithms and currency arbitrage, part 1

02 Mar 2019 · 6 min read   \[ [quant-finance](https://reasonabledeviations.com/category/quant-finance) ]\\

Arbitrage is the holy grail for traders and the bedrock of financial academia. Let’s say you are in an open marketplace with Alice selling oranges for $1 each and Bob buying them for $2. As a cunning trader, you realise you can buy an orange from Alice and immediately sell it to Bob for $1 of “risk-free” profit. However, as you keep reaping this $1 profit by buying up Alice’s oranges, she raises her prices. Eventually, Alice would be charging $2 per orange and the arbitrage would be shut. In other words, acting on arbitrage opportunities causes the market to become more efficient, with everything as close to its fair price as possible. Because of this, the only way to profit from true arbitrage is to find and execute opportunities faster than everybody else.

Currency exchange is a natural place to search for arbitrage because there are many different pairs that we can trade. For example, assume we are able to convert GBP to USD, then USD to EUR, then EUR to AUD for an effective rate of 1:2 GBP:AUD. If we were then able to directly swap AUD back to GBP in the ratio 2:1.1, this would be an arbitrage opportunity because we end up with more GBP than we started with while taking zero risk.

Our goal is to develop a systematic method for detecting arbitrage opportunities by framing the problem in the language of graphs. This is a reasonably large topic, so we’ll split it into two parts. Part 1 (this post) will lay the theoretical groundwork, introducing graph algorithms and giving an overview of their application to currency arbitrage. In [Part 2](https://reasonabledeviations.com/2019/04/21/currency-arbitrage-graphs-2/) we will present an actual implementation of these ideas in python, applied to cryptocurrencies.

### Graphs <a href="#graphs" id="graphs"></a>

Formally, we define a graph as a set of vertices (also called nodes) and edges. These edges can be _directed_ (i.e have little arrows on them) and may have _weights_. It is completely up to us to decide what the vertices, edges, and weights represent. For example, if we are trying to model a road network we might say that the vertices are cities (or junctions), the edges are the roads themselves, and the weights are the length of the roads. The diagram below shows how a weighted directed graph is typically depicted.![](https://reasonabledeviations.com/assets/images/weighted\_digraph.png)

It is useful to formulate real-world problems in terms of graphs because we have about three centuries worth of relevant theory – they were first investigated by Euler in 1736. In particular, there exist many efficient algorithms related to finding the shortest path along a graph, which have widespread applications e.g in mapping.

The [Bellman-Ford algorithm](https://en.wikipedia.org/wiki/Bellman%E2%80%93Ford\_algorithm) finds the minimum weight path from a single source vertex to all other vertices on a weighted directed graph. For the purposes of this post, we don’t need to know anything other than the fact that once the algorithm terminates, each vertex is labelled with the total weight of the minimum weight path from the source to that vertex.

Actually, the above statement has an incredibly important caveat. What happens if we try to find the minimum weight path from vertices C to D in the above graph? The obvious guess would be that it is the direct path along the CD edge, which has total weight 2.1. However, notice that we can in fact reduce this further by following the path CDECD, which would have a total weight of -1. But why stop there? If we go around the loop again, we can reduce it stil further. In fact, each time we traverse the loop, our minimum total weight will reduce by 1. Hence this is called a **negative-weight cycle**, the existence of which means that the shortest path between C and D is not defined.![](https://reasonabledeviations.com/assets/images/neg\_weight\_cycle.png)

This is actually the main reason why we are choosing to use Bellman-Ford over another shortest path algorithm like Dijkstra, despite the latter being asymptotically more efficient. Bellman-Ford is able to detect if there is a negative-weight cycle and as will be seen shortly, this will be the key to detecting arbitrage opportunities.

### Graphs for currency arbitrage <a href="#graphs-for-currency-arbitrage" id="graphs-for-currency-arbitrage"></a>

How can graphs be used to model currency markets? At a very high level, we will assign currencies to different vertices, and let the edge weight represent the exchange rate. A simple example is presented below: in this market, we can convert 1 GBP to 1.27 USD, 1 USD to 1.43 AUD, etc.![](https://reasonabledeviations.com/assets/images/currency\_graph.png)

To find the exchange rate between two currencies that do not share an edge, we simply find a path between the two currency vertices and walk along it, multiplying by each successive edge weight (exchange rate). If there are multiple possible paths, choose the path that has the greatest weight product, which corresponds to the most favourable rate.

What would happen if we start with 1 GBP and convert it along GBP →→ USD →→ AUD →→ GBP? Well, multiplying out the edges we see that our initial 1 GBP becomes 1.27×1.43×0.55≈0.9991.27×1.43×0.55≈0.999 GBP. That is to say, we lose a tenth of a penny on the round trip. However, if this number were greater than 1, it would mean that by following this path we end up with _more_ GBP than we started with – this is textbook arbitrage.

So the problem of finding arbitrage can thus be formally posed as follows: find a cycle in the graph such that multiplying all the edge weights along that cycle results in a value greater than 1. In fact we have already described an algorithm that can find such a path – the problem is equivalent to finding a negative-weight cycle, provided we do some preprocessing on the edges.

Firstly, we note that Bellman-Ford computes the path weight by adding the individual edge weights. To make this work for exchange rates, which are multiplicative, an elegant fix is to first take the logs of all the edge weights. Thus when we sum edge weights along a path we are actually multiplying exchange rates – we can recover the multiplied quantity by exponentiating the sum. Secondly, Bellman-Ford attempts to find _minimum_ weight paths and _negative_ edge cycles, whereas our arbitrage problem is about maximising the amount of currency received. Thus as a simple modification, we must also make our log weights negative.

With these two tricks in hand, we are able to apply Bellman-Ford. The minimal weight between two currency vertices corresponds to the optimal exchange rate, the value of which can be found by by exponentiating the negative sum of weights along the path. As a corollary, we have the wonderful insight that: **a negative-weight cycle on the negative-log graph corresponds to an arbitrage opportunity**.

### Conclusion <a href="#conclusion" id="conclusion"></a>

We have seen that graphs provide an elegant framework for thinking about currency exchange. Concretely, by representing different currencies as vertices and using the negative log of the exchange rate as the edge weight we can apply shortest-path algorithms to find negative-weight cycles if they exist, which correspond to arbitrage opportunities. In the [next post](https://reasonabledeviations.com/2019/04/21/currency-arbitrage-graphs-2/), we code up the methodology presented in this post and apply it to some real-world data. Should be fun!\\

## Graph algorithms and currency arbitrage, part 2

21 Apr 2019 · 17 min read   \[ [quant-finance](https://reasonabledeviations.com/category/quant-finance) ]\\

In the [previous post](https://reasonabledeviations.com/2019/03/02/currency-arbitrage-graphs/) (which should definitely be read first!) we explored how graphs can be used to represent a currency market, and how we might use shortest-path algorithms to discover arbitrage opportunities. Today, we will apply this to real-world data. It should be noted that we are not attempting to build a functional arbitrage bot, but rather to explore how graphs could potentially be used to tackle the problem. Later on we’ll discuss why our methodology is unlikely to result in actionable arbitrage.

Rather than using fiat currencies as presented in the previous post, we will examine a market of cryptocurrencies because it is much easier to acquire crypto order book data. We’ll narrow down the problem further by making two more simplifications. Firstly, we will focus on arbitrage within a single exchange. That is, we’ll look to see if there are pathways between different coins on an exchange which leave us with more of a coin than we started with. Secondly, we will only be considering a single snapshot of data from the exchange. Obviously markets are highly dynamic, with thousands of new bids and asks coming in each second. A proper arbitrage system needs to constantly be scanning for opportunities, but that’s out of the scope of this post.

With all this in mind, the overall implementation strategy was as follows:

1. For a given exchange, acquire the list of pairs that will form the vertices.
2. For each of these pairs, download a snapshot of the bid/ask.
3. Process these values accordingly, assigning them to directed edges on the graph.
4. Using Bellman-Ford, find and return negative-weight cycles if they exist.
5. Calculate the arbitrage that these negative-weight cycles correspond to.

_The full code for this project can be found in this_ [_GitHub repo_](https://github.com/robertmartin8/CryptoGraphArb/tree/master)_. If you find this post interesting, don’t forget to leave a star!_

[Star](https://github.com/robertmartin8/CryptoGraphArb)

### Raw data <a href="#raw-data" id="raw-data"></a>

For the raw data, I decided to use the [CryptoCompare API](https://min-api.cryptocompare.com/documentation) which has a load of free data compiled across multiple exchanges. To get started, you’ll need to register to get a free API key.

As mentioned previously, we will only look at data from Binance. I chose Binance not because it has a large selection of altcoins, but because most altcoins can trade directly with multiple pairs (e.g BTC, ETH, USDT, BNB). Some exchanges have many altcoins but you can only buy them with BTC – this is not well suited for arbitrage.

Firstly, we need to find out which pairs Binance offers. This is done with a simple call (`AUTH` is your API key string):

```
import requests
import json 

def top_exchange_pairs():
    url = (
        "https://min-api.cryptocompare.com/data/v3/all/" + 
        "exchanges?topTier=true&api_key=" + AUTH
    )
    r = requests.get(url)
    with open("pairs_list.json", "w") as f:
        json.dump(r.json(), f)
```

This is an excerpt from the resulting JSON file – for each exchange, the `pairs` field lists all other coins that the key coin can be traded with:

```
"Data":{  
   "Binance":{  
      "isActive":true,
      "isTopTier":true,
      "pairs":{  
         "ETH":["PAX", "TUSD", "USDT", "USDC", "BTC"],
         "ONGAS":["BTC", "BNB", "USDT"],
         "PHX":["ETH","BNB","BTC"]
      }
   },
   "Coinbase":{  
      "isActive":true,
      "isTopTier":true,
      "pairs":{  
         "ETH":["DAI", "USD", "USDC", "EUR", "GBP", "BTC"],
         "BCH":["BTC", "GBP", "EUR", "USD"]
      }
   }
}
```

I then filtered out coins with fewer than three tradable pairs. These coins are unlikely to participate in arbitrage – we would rather have a graph that is more connected.

```
def binance_connected_pairs():
    with open("pairs_list.json", "r") as f:
        data = json.load(f)
    pairs = data["Data"]["Binance"]["pairs"]
    return {k: v for k, v in pairs.items() if len(v) > 3}
```

We are now ready to download a snapshot of the available exchange rates for each of these coins.

```
import os
import tqdm  # progress bar

def download_snapshot(pair_dict, outfolder):
    if not os.path.exists(outfolder):
        os.makedirs(outfolder)

    # Download data and write to files
    for p1, p2s in tqdm(pair_dict.items()):
        url = (
            "https://min-api.cryptocompare.com/data/" 
            + f"ob/l1/top?fsyms={p1}&tsyms={','.join(p2s)}"
            + "&e=Binance&api_key=" + AUTH
        )
        r = requests.get(url)
        with open(f"{outfolder}/{p1}_pairs_snapshot.json", "w") as f:
            json.dump(r.json(), f)
```

We can then run all of the above functions to produce a directory full of the exchange rate data for the listed pairs.

```
top_exchange_pairs()
connected = binance_connected_pairs()
download_snapshot(connected, "binance_data")
```

```
"EOS": {
    "BNB": {
        "BID": ".2073",
        "ASK": ".2077"
    },
    "BTC": {
        "BID": ".0007632",
        "ASK": ".0007633"
    },
    "ETH": {
        "BID": ".02594",
        "ASK": ".025964"
    },
    "USDT": {
        "BID": "7.0441",
        "ASK": "7.046"
    },
    "PAX": {
        "BID": "7.0535",
        "ASK": "7.07"
    }
}
```

This excerpt reveals something that we glossed over completely in the previous post. As anyone who has tried to exchange currency on holiday will know, there are actually two exchange rates for a given currency pair depending on whether you are buying or selling the currency. In trading, these two prices are called the **bid** (the current highest price someone will buy for) and the **ask** (the current lowest price someone will sell for). As it happens, this is very easy to deal with in the context of graphs.

### Preparing the data <a href="#preparing-the-data" id="preparing-the-data"></a>

Having downloaded the raw data, we must now prepare it so that it can be put into a graph. This effectively means parsing it from the raw JSON and putting it into a pandas dataframe. We will arrange it in the dataframe such that it constitutes an adjacency matrix:

* Column ETH row BTC is the bid:
  * i.e someone will pay _x_ BTC to buy my 1 ETH
  * this is then the weight of the ETH →→ BTC edge.
* Column BTC row ETH is the ask:
  * i.e I have to pay _y_ BTC to buy someone’s 1 ETH
  * the reciprocal of this is the weight of the BTC →→ ETH edge.

I chose this particular row-column scheme because it results in intuitive indexing: `df.X.Y` is the amount of Y gained by selling 1 unit of X, and `df.A.B * df.B.C * df.C.D` is the total amount of D gained by trading 1 unit of A when trading via A→B→C→DA→B→C→D.

The column headers will be the same as the row headers, consisting of all the coins we are considering. The function that creates the adjacency matrix is shown here:

```
def create_adj_matrix(pair_dict, folder, outfile="snapshot.csv"):
    # Union of 'from' and 'to' pairs
    flatten = lambda l: [item for sublist in l for item in sublist]
    keys, vals = pair_dict.items()
    all_pairs = list(set(keys).union(flatten(values)))

    # Create empty df
    df = pd.DataFrame(columns=all_pairs, index=all_pairs)

    for p1 in pair_dict.keys():
        with open(f"{folder}/{p1}_pairs_snapshot.json", "r") as f:
            res = json.load(f)
        quotes = res["Data"]["RAW"][p1]
        for p2 in quotes:
            try:
                df[p1][p2] = float(quotes[p2]["BID"])
                df[p2][p1] = 1 / float(quotes[p2]["ASK"])
            except KeyError:
                print(f"Error for {p1}/{p2}")
                continue
    df.to_csv(outfile)
```

### Putting the data into a graph <a href="#putting-the-data-into-a-graph" id="putting-the-data-into-a-graph"></a>

We will be using the [NetworkX](https://networkx.github.io/documentation/stable/) package, an intuitive yet extremely well documented library for dealing with all things graph-related in python.

In particular, we will be using `nx.DiGraph`, which is just a (weighted) directed graph. I was initially concerned that it’d be difficult to get the data in: python libraries often adopt their own weird conventions and you have to modify your data so that is in the correct format. This was not really the case with NetworkX, it turns out that we already did most of the hard work when we put the data into our pandas adjacency matrix.

Firstly, we take negative logs as discussed in the [previous post](https://reasonabledeviations.com/2019/03/02/currency-arbitrage-graphs/). Secondly, in our dataframe we currently have `NaN` whenever there is no edge between two vertices. To make a valid `nx.DiGraph`, we need to set these to zero. Lastly, we transpose the dataframe because NetworkX uses a different row/column convention. We then pass this processed dataframe into the `nx.Digraph` constructor. Summarised in one line:

```
g = nx.DiGraph(-np.log(df).fillna(0).T)
```

### Bellman-Ford <a href="#bellman-ford" id="bellman-ford"></a>

To implement Bellman-Ford, we make use of the funky `defaultdict` data structure. As the name suggests, it works exactly like a python dict, except that if you query a key that is not present you get a certain default value back. The first part of our implementation is quite standard, as we are just doing the n−1n−1 edge-relaxations where _n_ is the number of vertices.

But because the ‘classic’ Bellman-Ford does not actually return negative-weight cycles, the second part of our implementation is a bit more complicated. The key idea is that if after n−1n−1 relaxations, there is an edge that can be relaxed further then that edge must be on a negative weight cycle. So to find this cycle we walk back along the predecessors until a cycle is detected, then return the cyclic portion of that walk. In order to prevent subsequent redundancy, we mark these vertices as ‘seen’ via another `defaultdict`. This procedure adds a linear cost to Bellman-Ford since we have to iterate over all the edges, but the asymptotic complexity overall remains O(VE)O(VE).

```
def bellman_ford_return_cycle(g, s):
    n = len(g.nodes())
    d = defaultdict(lambda: math.inf)  # distances dict
    p = defaultdict(lambda: -1)  # predecessor dict
    d[s] = 0

    for _ in range(n - 1):
        for u, v in g.edges():
            # Bellman-Ford relaxation
            weight = g[u][v]["weight"]
            if d[u] + weight < d[v]:
                d[v] = d[u] + weight
                p[v] = u  # update pred

        # Find cycles if they exist
        all_cycles = []
        seen = defaultdict(lambda: False)

        for u, v in g.edges():
            if seen[v]:
                continue
            # If we can relax further there must be a neg-weight cycle
            weight = g[u][v]["weight"]
            if d[u] + weight < d[v]:
                cycle = []
                x = v
                while True:
                    # Walk back along preds until a cycle is found
                    seen[x] = True
                    cycle.append(x)
                    x = p[x]
                    if x == v or x in cycle:
                        break
                # Slice to get the cyclic portion
                idx = cycle.index(x)
                cycle.append(x)
                all_cycles.append(cycle[idx:][::-1])
        return all_cycles
```

As a reminder, this function returns all negative-weight cycles reachable from a given source vertex (returning the empty list if there are none). To find all negative-weight cycles, we can simply call the above procedure on every vertex then eliminate duplicates.

```
def all_negative_cycles(g):
    all_paths = []
    for v in g.nodes():
        all_paths.append(bellman_ford_negative_cycles(g, v))
    flattened = [item for sublist in all_paths for item in sublist]
    return [list(i) for i in set(tuple(j) for j in flattened)]
```

### Tying it all together <a href="#tying-it-all-together" id="tying-it-all-together"></a>

The last thing we need is a function that calculates the value of an arbitrage opportunity given a negative-weight cycle on a graph. This is easy to implement: we just find the total weight along the path then exponentiate the negative total (because our weights are the negative log of the exchange rates).

```
def calculate_arb(cycle, g, verbose=True):
    total = 0
    for (p1, p2) in zip(cycle, cycle[1:]):
        total += g[p1][p2]["weight"]
    arb = np.exp(-total) - 1
    if verbose:
        print("Path:", cycle)
        print(f"{arb*100:.2g}%\n")
    return arb


def find_arbitrage(filename="snapshot.csv"):
    df = pd.read_csv(filename, header=0, index_col=0)
    g = nx.DiGraph(-np.log(df).fillna(0).T)

    if nx.negative_edge_cycle(g):
        print("ARBITRAGE FOUND\n" + "=" * 15 + "\n")
        for p in all_negative_cycles(g):
            calculate_arb(p, g)
    else:
        print("No arbitrage opportunities")
```

Running this function gives the following output:

```
ARBITRAGE FOUND
===============

Path: ['USDT', 'BAT', 'BTC', 'BNB', 'ZEC', 'USDT']
0.087%

Path: ['BTC', 'XRP', 'USDT', 'BAT', 'BTC']
0.05%

Path: ['BTC', 'BNB', 'ZEC', 'USDT', 'BAT', 'BTC']
0.087%

Path: ['BNB', 'ZEC', 'USDT', 'BAT', 'BTC', 'BNB']
0.087%

Path: ['USDT', 'BAT', 'BTC', 'XRP', 'USDT']
0.05%
```

0.09% is not exactly a huge amount of money, but it is still risk-free profit, right?

### Why wouldn’t this work? <a href="#why-wouldnt-this-work" id="why-wouldnt-this-work"></a>

Notice that we haven’t mentioned exchange fees at any point. In fact, Binance charges a standard 0.1% commission on every trade. It is easy to modify our code to incorporate this: we just multiply each exchange rate by 0.999. But we don’t need to compute anything to see that we would certainly be losing much more money than gained from the arbitrage.

Secondly, it is likely that this whole analysis is flawed because of the way the data was collected. The function `download_snapshot` makes a request for each coin in sequence, taking a few seconds in total. But in these few seconds, prices may move – so really the above “arbitrage” may just be a result of our algorithm selecting some of the price movements. This could be fixed by using timestamps provided by the exchange to ensure that we are looking at the order book for each pair at the exact same moment in time.

Thirdly, we have assumed that you can trade an infinite quantity of the bid and ask. An order consists of a price and a quantity, so we will only be able to fill a limited quantity at the ask price. Thus in practice we would have to look at the top few levels of the order book and consider how much of it we’d eat into.

It is not difficult to extend our methodology to arb between different exchanges. We would just need to aggregate the top of the order book from each exchange, then put the best bid/ask onto the respective edges. Of course, to do run this strategy live would require us to manage our inventory not just on a currency level but per currency per exchange, and factors like the congestion of the bitcoin network would come into play.

Lastly, this analysis has only been for a single snapshot. A proper arbitrage bot would have to constantly look for opportunities simultaneously across multiple order books. I think this could be done by having a websocket stream which keeps the graph updated with the latest quotes, and using a more advanced method for finding negative-weight cycles that does not involve recomputing the shortest paths via Bellman-Ford.

### Conclusion <a href="#conclusion" id="conclusion"></a>

All this begs the question: why is it so hard to find arbitrage? The simple answer is that other people are doing it smarter, better, and (more importantly) faster. With highly optimised algorithms (probably implemented in C++), ‘virtual colocation’ of servers, and proper networking software/hardware, professional market makers are able to exploit these simple arbitrage opportunities extremely rapidly.

In any case, the point of this post was not to develop a functional arbitrage bot but rather to demonstrate the power of graph algorithms in a non-standard use case. Hope you found it as interesting as I did!
