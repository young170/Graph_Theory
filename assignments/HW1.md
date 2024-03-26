## 9.1.1
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

## 9.1.5
Let a group of $20$ shake hands as a group $71$ times, prove there exists a person who shaked hands at least $8$ times.

### Proof
> This proof uses the pigeonhole principle

Using proof by contradiction, assume there does not exist a person who shaked at least $8$ times among the $71$ handshakes.

To shake hands, two distinct (distinguishable) people need to participate so the group can be spilt into pairs of two of a total $10$ pairs.

By our assumption, every person can shake the others' hand at most $7$ times. Hence, at most $70$ handshakes can occur.

However, our assumption also states there were $71$ handshakes. This contradicts our assumption.

$\therefore$ There exists a person who shaked at least $8$ times.

## 9.1.9
Let $G$ be a graph, where the min-degree is $\delta$.
1. Prove there exists a path that has a length of at least $\delta$.
2. Prove there exists a cycle that has a length of at least $\delta + 1$.

### Proof
#### Proof 1
Using proof by contradiction, assume there is no path of length at least $\delta$ in $G$.

The longest path in $G$ has length less than $\delta$.

Let $v_0, v_1, \ldots, v_k$ be the longest path in $G$, where $k < \delta$.

Since $v_0$ has degree at least $\delta$, there must be at least $\delta$ distinct vertices adjacent to $v_0$.

However, since the path $v_0, v_1, \ldots, v_k$ has length less than $\delta$, not all of these adjacent vertices can be included in the path.

Hence, there must be at least one vertex adjacent to $v_0$ that is not in the path.

By adding this vertex to the path, we obtain a longer path, contradicting the assumption that $v_0, v_1, \ldots, v_k$ was the longest path.

$\therefore$ There exists a path of length at least $\delta$.

#### Proof 2
Using the proof from part 1, let P be the path $v_0, v_1, \ldots, v_\delta$ of length $\delta$.

Let $v_0$ be the vertex that has the min-degree of $\delta$, meaning it has at least $\delta$ adjacent vertices.

At least one of the adjacent vertices, $v_j$, must be also adjacent to some $v_i$ for $0 \leq i \leq \delta$.

If $v_j$ is adjacent to $v_0$, then we found a cycle of length $\delta + 1$ and have proven the statement.

Else, $v_j$ is adjacent to some $v_i$ for $0 \lt i \lt \delta$.

Hence, a different cycle is created by taking the subset of the original path.
$$v_i, v_{i+1}, \ldots, v_j, v_{j+1}, v_i$$
This cycle has the length of $\delta + 1$.

$\therefore$ There exists a cycle of length at least $\delta$

## 9.1.14 (1)
Prove whether the following degree sequence is graphic or not: $5, 5, 4, 4, 3, 2, 2, 1, 1$

### Proof
Using the Havel-Hakimi theorem, the degree sequence, $d$, can be broken down into a simpler degree sequence.
$$d = (5, 5, 4, 4, 3, 2, 2, 1, 1), d\prime = ()$$

## TODO
9.2.4 (1)
9.2.9
9.3.3
9.3.8
