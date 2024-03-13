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

### Corollary - degree-sum formula
$\forall g$ the number of `odd points` is even<br>
How is this possible? And what is a `corollary`?<br>
First, a corollary is a kind of "side theorem". A theorem that is not essential, but helpful in other ways.<br>

First step is **reduction** (one of my favourite concepts!). Split $\sum_{v \in V}d(v)$ into two. Vertices with even degrees and odd degrees. $\sum_{v \in V}d(v_o) + \sum{v \in V}d(v_e)$.
* $v_o$ represents vertices with odd degrees
* $v_e$ represents vertices with even degrees

We know the sum of the degrees of even vertices must be even, and $2|e|$ is even. Also, for a sum of an even number and an arbituary number to be even, the arbituary number has to be an even number.<br>
$\therefore \sum_{v \in V}d(v_o)$ is even.

## How are graphs traversed?
There are many ways a graph can be traversed. The point to note while reading along is that all (most of them) of them are extensions of each other. Simply, the previous traversal method with an additional condition to make it a proper subset.

### Walk & closed-walk
Imagine taking a walk in the park, if you were to draw a line on the ground while walking it would form a continous line.<br>
Using this idea, a walk is:
- A `sequence` of `adjacent` edges
- Because every "walk" has a starting point and an end point, these points are called: `initial` & `terminal` points.<br>
Now after your (hopefully) daily walk, you would normally check the distance you've covered (and either feel proud! or...). This is called the `length` of walk.<br>
It is calculated just as your health app would, no limits and no removal of overlaps.<br>
When your inital point and terminal points are the same it is termed a `closed` walk. Simple as that!

### Trail
In the introduction of this chapter I meantioned each traversal method is just the extension of the one before.<br>
A `trail` is just a `walk` with `distinct` edges.

### Path
Continuing from `trails`, a `path` is just a `trail` with `distinct` vectices. Remember the difference between trails and paths (distinct edges vs vertices).

### In a nutshell
![graph traversal method circle](https://github.com/young170/Graph_Theory/main/assets/images/graph_traversal_method_circle.png)
This diagram shows the relationship between the 3 introduced methods.<br>
$path \subset trail \subset walk$

### Cycle
Now this is where things start to get interesting.<br>

```
Notice cycles are not formally a subset of paths because by definition, paths must have distinct vertices.
```

## Notations to remember

