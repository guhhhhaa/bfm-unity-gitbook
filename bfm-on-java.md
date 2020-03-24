# BFM On Java

## 未完成

{% api-method method="get" host="https://api.cakes.com" path="/v1/cakes/:id" %}
{% api-method-summary %}
Get Cakes
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" %}
ID of the cake to get, for free of course.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication token to track down who is emptying our stocks.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="recipe" type="string" %}
The API will do its best to find a cake matching the provided recipe.
{% endapi-method-parameter %}

{% api-method-parameter name="gluten" type="boolean" %}
Whether the cake should be gluten-free or not.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```text
{    "name": "Cake's name",    "recipe": "Cake's recipe name",    "cake": "Binary cake"}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```text
{    "message": "Ain't no cake like that."}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

```java
private void relax(EdgeWeightedDigraph G, int v)

{

for (DirectedEdge e : G.adj(v)

{

int w = e.to(); if (distTo[w] > distTo[v] + e.weight()) {

distTo[w] = distTo[v] + e.weight(); edgeTo[w] = e; if (!onQ[w]) {

q.enqueue(w);

onQ[w] = true; }

} if (cost++ % G.V() == 0) findNegativeCycle();

}

}
```

Relaxation for Bellman-Ford，Algorithhms 4th Edition by Robert Sedgewick, Kevin Wayne，P673

> ALGORITHM 4.11
>
> Bellman-Ford algorithm \(queue-based\)

```java
public class BellmanFordSP {

private double[] distTo; private DirectedEdge[] edgeTo; private boolean[] onQ; private Queue<Integer> queue; private int cost; private Iterable<DirectedEdge> cycle;

// length of path to v // last edge on path to v // Is this vertex on the queue? // vertices being relaxed // number of calls to relax() // negative cycle in edgeTo[]?

public BellmanFordSP(EdgeWeightedDigraph G, int s) {

distTo = new double[G.V()]; edgeTo = new DirectedEdge[G.V()]; onQ = new boolean[G.V()]; queue = new Queue<Integer>(); for (int v = 0; v < G.V(); v++)

distTo[v] = Double.POSITIVE_INFINITY; distTo[s] = 0.0; queue.enqueue(s); onQ[s] = true; while (!queue.isEmpty() && !this.hasNegativeCycle()) {

int v = queue.dequeue();

onQ[v] = false;

relax(v); }

}

private void relax(int v) // See page 673.

public double distTo(int v) public boolean hasPathTo(int v) public Iterable<Edge> pathTo(int v)

// standard client query methods // for SPT implementatations // (See page 649.)

private void findNegativeCycle() public boolean hasNegativeCycle() public Iterable<Edge> negativeCycle() // See page 677.

}
```

This implementation of the Bellman-Ford algorithm uses a version of relax\(\) that puts vertices pointed to by edges that successfully relax on a FIFO queue \(avoiding duplicates\) and periodically checks for a negative cycle in edgeTo\[\] \(see text\).

> Arbitrage in currency exchange

```java
public class Arbitrage {

public static void main(String[] args) { int V = StdIn.readInt(); String[] name = new String[V]; EdgeWeightedDigraph G = new EdgeWeightedDigraph(V); for (int v = 0; v < V; v++) { name[v] = StdIn.readString(); for (int w = 0; w < V; w++) { double rate = StdIn.readDouble(); DirectedEdge e = new DirectedEdge(v, w, -Math.log(rate)); G.addEdge(e); }

}

BellmanFordSP spt = new BellmanFordSP(G, 0); if (spt.hasNegativeCycle()) {

double stake = 1000.0; for (DirectedEdge e : spt.negativeCycle()) {

StdOut.printf("%10.5f %s ", stake, name[e.from()]);

stake *= Math.exp(-e.weight());

StdOut.printf("= %10.5f %s\n", stake, name[e.to()]); }

} else StdOut.println("No arbitrage opportunity");

}

}
```

This BellmanFordSP client ﬁnds an arbitrage opportunity in a currency exchange table by construct- ing a complete-graph representation of the exchange table and then using the Bellman-Ford algo- rithm to ﬁnd a negative cycle in the graph.

```java
% java Arbitrage < rates.txt 
1000.00000 USD = 741.00000 EUR 
741.00000 EUR = 1012.20600 CAD 
1012.20600 CAD = 1007.14497 USD
```

