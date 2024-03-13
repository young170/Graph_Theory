## Introduction
This note consists of fundamental definitions of graph theory

## What is a graph?
### Graph
Let $G = (V, E, R)$ where:
- $V$ is the set of `vertices` (nodes) in the graph.
- $E$ is the set of `edges` (connections) between the vertices.
- $R$ is a `relation` that maps each edge to a pair of vertices it connects.

The relation associates each edge with two vertices. These vertices of an edge are called the `end points` of the edge.
* A vertex can have multiple edges
* When $v_1$ and $v_2$ are the same, $v_1 = v_2$, $(v_1, v_2)$ is called a `loop`.<br>

### Degree
Let $d(v)$ where:
- $v$ is a vertex of the set of vertices
  -  $v \in V$
- $d(v)$ is the # of edges with v as the endpoint
  - An interesting point is that loops count as two `degrees`
  - Simply, drawing a loops one can see there are two entries to/from the vertex

### Degree-sum formula
Let $G = (V, E)$
- Graphs are usually denoted using only $V$ and $E$

Let $|E|$ be the # of edges of graph $G$<br>
Then by the *degree-sum formula*, $2|E| = \sum_{v \in V}d(v)$
- This can be easily determined because each edge has two vertices

## How are graphs traversed?
