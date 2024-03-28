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
Using the proof from part 1, let $P$ be the path $v_0, v_1, \ldots, v_\delta$ of length $\delta$.

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

![graph-9_2_4](https://github.com/young170/Graph_Theory/blob/main/assets/images/graph-9_2_4.png)

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

## TODO
9.2.9
9.3.3
9.3.8
