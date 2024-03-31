## 9.1.1 (1)
Let $G = (V, E)$ be a graph, where $|E| = 25$ and the minimum degree of a vertex $v$, $v \in V$, is $4$.

What is the maximum $|V|$, $G$ can have?

### Solution
By the degree-sum formula which states that $2|E| = deg(v)$, $\forall v \in V$, the sum of the degrees of $V$ is at least $4n$, where $n$ is $|V|$.
$$2|E| \geq 4n$$
$$2\times25 \geq 4n$$
As the $n$ is answer we are trying to find, $|V|$, further solving the equation for $n$ gives us the answer.
$$50 \geq 4n$$
$$12.5 \geq n$$
The number of vertices must be an integer.
$$12 \geq n$$

$\therefore$ The maximum $|V|$, graph $G$ can have is $12$.

## 9.1.1 (2)
Let $G = (V, E)$ be a simple graph, where $|E| = 50$.

What is the minimum $|V|$, $G$ can have?

### Solution
For a simple graph to have the minimum number of vertices, $|V|$, each vertex have as much edges as possible. A graph that has this characteristic is the complete graph.

By definition, a complete graph is where for every vertex, there is one and only one edge to all other vertices.

Based on the definition of a complete graph, every vertex of $G$ has the degree of $n - 1$ where $n$ is the number of vertices.

By the degree-sum formula,
$$2|E| = n(n - 1)$$
$$|E| = \frac{n(n - 1)}{2}$$
Substituting our problem gives,
$$50 = \frac{n(n - 1)}{2}$$
Solving for $n$,
$$100 = n(n - 1)$$
$n$ must be an integer. $\lceil n \rceil$

$\therefore$ The minimum $|V|$, graph $G$ can have is $11$.

## 9.1.5
Let a group of $20$ shake hands as a group $71$ times, prove there exists a person who shaked hands at least $8$ times.

### Proof
> This proof uses the pigeonhole principle

Using proof by contradiction, assume there does not exist a person who shaked at least $8$ times among the $71$ handshakes.

To shake hands, two distinct (distinguishable) people need to participate so the group can be spilt into pairs of two of a total $10$ pairs.

By our assumption, every person can shake the others' hand at most $7$ times. Hence, at most $70$ handshakes can occur.

However, our assumption also states there were $71$ handshakes. This contradicts our assumption.

$\therefore$ There exists a person who shaked at least $8$ times.

## 9.1.9 (1)
Let $G$ be a graph, where the min-degree is $\delta$.

Prove there exists a path that has a length of at least $\delta$.

### Proof
Using proof by contradiction, assume there is no path of length at least $\delta$ in $G$.

The longest path in $G$ has length less than $\delta$.

Let $v_0, v_1, \ldots, v_k$ be the longest path in $G$, where $k < \delta$.

Since $v_0$ has degree at least $\delta$ because either it is the min-degree vertex or not, there must be at least $\delta$ distinct vertices adjacent to $v_0$.

However, since the path $v_0, v_1, \ldots, v_k$ has length less than $\delta$, not all of these adjacent vertices are included in the path.

Hence, there must be at least one vertex adjacent to $v_0$ that is not in the path.

This step is can be repeated until the length of the path is $\delta$ because each vertex has at least $\delta$ adjacent vertices.

By adding these vertices to the path, we obtain a path of at least length $\delta$, contradicting the assumption that the length of the longest path was less than $\delta$.

$\therefore$ There exists a path of length at least $\delta$.

## 9.1.9 (2)
Let $G$ be a graph, where the min-degree is $\delta$.

Prove there exists a cycle that has a length of at least $\delta + 1$.

### Proof
Let path $P = (v_0, v_1, ..., v_k)$ be the longest path in $G$.

The degree of $v_k$ is at least $\delta$. This is proven from Section `9.1.9 (1)`.

Let an arbituary $v_i$ be the neighboring vertex to $v_k$ that creates the longest path.

This creates the longest cycle because $v_iv_k \in E$, which a cycle following the path.

The length of this cycle is $k + 1 - i$. $k$ vertices subtracted by $0 ~ i$ and $1$ added because it is a cycle.

Also, it follows that the length of the path from $v_i$ to $v_{k-1}$ is $k - i \ge \delta$. Simply, subtracting $v_k$ and $v_i$ (the looping vertex) gives $k - i$. $k - i$ is greater or equal to $\delta$ because by the definition of $P$, $deg(v_k) \ge \delta$ and $v_i$ is the neighboring vertex that creates the longest path, which is at leat $\delta$.

Adding $1$ to each side of the equation gives, $k + 1 -i \ge \delta$. The left side of the equation is equivalent to the length of the cycle.

$\therefore$ There exists a cycle of length $\ge \delta$ for a graph with a minimum degree of $\delta$.

## 9.1.14 (1)
Prove whether the following degree sequence, $D$, is graphic: $5, 5, 4, 4, 3, 2, 2, 1, 1$. If it is draw a simple graph of the graphic.

### Proof
By the degree-sum formula, the sum of the degrees should be even ($2|E|$).

$\sum_{d_i \in D} d_i$ is odd, $27$.

$\therefore$ The degree sequence is not graphic, and cannot be drawn as a simple graph.

Also, using the Havel-Hakimi algorithm, the degree sequence, $D$, can be proven to be non-graphic.
$$D = (5, 5, 4, 4, 3, 2, 2, 1, 1), k = 5, D\prime = (4, 3, 3, 2, 1, 2, 1, 1) = (4, 3, 3, 2, 2, 1, 1, 1)$$
$$D\prime = (4, 3, 3, 2, 2, 1, 1, 1), k = 4, D\prime\prime = (2, 2, 1, 1, 1, 1, 1)$$
$$D\prime\prime = (2, 2, 1, 1, 1, 1, 1), k = 2, D\prime\prime\prime = (1, 0, 1, 1, 1, 1)$$
$$D\prime\prime\prime = (1, 0, 1, 1, 1, 1), k = 1, D\prime\prime\prime\prime = (-1, 1, 1, 1, 1)$$
As in the algorithm, a negative value in the reduced degree sequence denotes that it is not graphic.

## 9.2.4 (1)
Solve the **incident matrix** and the **adjacent matrix** for the following graph, $G$:

<img src="https://github.com/young170/Graph_Theory/blob/main/assets/images/graph-9_2_4.png" alt="prob-graph" width="300"/>

<img src="https://github.com/young170/Graph_Theory/blob/main/assets/images/graph-9_2_4-hand.jpeg" alt="hand-graph" width="300"/>

### Incident matrix
$$
I(G) = 
\begin{bmatrix}
1 & 0 & 0 & 0 & 0 & 1 & 1 & 0 & 1 \\
1 & 1 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\
0 & 1 & 1 & 0 & 0 & 0 & 1 & 1 & 0 \\
0 & 0 & 1 & 1 & 0 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 1 & 1 & 0 & 0 & 1 & 1 \\
0 & 0 & 0 & 0 & 1 & 1 & 0 & 0 & 0
\end{bmatrix}
$$

### Adjacent matrix
$$
A(G) = 
\begin{bmatrix}
0 & 1 & 1 & 0 & 1 & 1 \\
1 & 0 & 1 & 0 & 0 & 0 \\
1 & 1 & 0 & 1 & 1 & 0 \\
0 & 0 & 1 & 0 & 1 & 0 \\
1 & 0 & 1 & 1 & 0 & 1 \\
1 & 0 & 0 & 0 & 1 & 0
\end{bmatrix}
$$

## 9.2.9
Given the adjacency matrix $A(G)$ of a graph, $G = (V, E)$.
1. Solve for the the minimum and maximum degree of $G$.
2. Solve for the number of edges of $G$.
3. Solve for the number of cycles that have the length of $3$ in $G$.

$$
A(G) = 
\begin{bmatrix}
0 & 1 & 1 & 1 & 1 \\
1 & 0 & 1 & 0 & 0 \\
1 & 1 & 0 & 1 & 1 \\
1 & 0 & 1 & 0 & 1 \\
1 & 0 & 1 & 1 & 0
\end{bmatrix}
$$

### 1
The vertex with the minimum degree is the row|column that has the least entries. This is because each entry counts for an edge starting/ending on that vertex. Hence, counting as a degree.

Inversely, the vertex with the maximum degree is the row|column that has the most entries.

$\therefore$ The minimum degree is $v_2 = 2$ and the maximum degree is $v_1, v_3 = 4$.

### 2
Each edge is recorded twice in the adjacency matrix.

$\therefore$ The number of edges is $8$.

### 3
By theorem 9.2.2 (2), for an arbituary natural number $m$, $A^m_{i,j}$ represents the number of paths of length $m$ from vertex $v_i$ to vertex $v_j$.

To find the number of cycles of length $3$ in graph $G$, let $A^3_{i,j}$ be the adjacency matrix $A(G)$ raised to the power of $m$, $3$.

$$
A^3(G) = 
\begin{bmatrix}
8 & 7 & 9 & 9 & 9 \\
7 & 2 & 7 & 4 & 4 \\
9 & 7 & 8 & 9 & 9 \\
9 & 4 & 9 & 6 & 7 \\
9 & 4 & 9 & 7 & 6
\end{bmatrix}
$$

## 9.3.3
Solve for all complete graphs, $K_n$, and complete-bipartite graphs, $K_{m,n}$, that contain a Euler cycle.

### Solution - Complete Graphs
Using the theorem on the existence of Euler cycles, this problem can be solved.

The theorem states, the necessary and sufficient condition for a connected graph, $G$, to have a Euler cycle is when all vertices of $G$ have an even degree.

For all the vertices in a complete graph to have an even degree, the total number of vertices, $|V|$, must be an odd number.

By the definition of a complete graph, all vertices are connected to $n - 1$ distinct vertices, when $n = |V|$.

$\therefore$ All complete graphs, $K_n$, with $n \ge 3$, contain a Euler cycle **IFF** $n$ is an odd number.

### Solution - Complete-Bipartite Graphs
By the definition of complete-bipartite graphs, the set of vertices, $V$, of a complete-bipartite graph, $G$, can be divided into two disjoint sets, $U$ and $W$.

Also, by definition, $\forall u \in U$, $u_i$ has an even degree **IFF** $|W|$ is even.

Similarly, $\forall w \in W$ can be proved.

$\therefore$ A complete-bipartite graph, $K_{m,n}$ has a Euler cycle **IFF** $m$, $|U|$, and $n$, $|W|$ are even.

## TODO
9.3.8
