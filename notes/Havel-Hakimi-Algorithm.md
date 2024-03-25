## Havel-Hakimi Algorithm
Let degree sequence $d$ be separated into sections: $(S, T, D)$ and $d\prime$ be $(T\prime, D)$.

The theorem states: $d$ is a graphic IFF $d\prime$ is a graphic.

### $\leftarrow$
Given $d\prime$ is graphic, the graph of $d\prime$, $A\prime$, can be defined as the following:
$$d\prime(t_1-1, ..., t_s-1, D)$$
Then simply by adding a new vertex $v$ adjacent to the $s$ vertices of $T$ would prove if $d\prime$ is graphic, then $d$ is graphic.

### $\rightarrow$
First, divide the proof into two separate cases: (1) $S$ is adjacent to $T$ and (2) $S$ is not adjacent to $T$ for $1 \leq i \leq s$.

Case 1 is trivial. Removing $S$ from $d$ would be equivalent to $d\prime$.

Case 2 is again split into two parts: (1) when $t_i = d_j$ or (2) $t_i \gt d_j$.<br>
This is because: $d(S, T, D)$ is in a non-increasing order $S$ has at least the degree of $s$ so $S$ must be adjacent to some $d_j \in D$ for $1 \leq j \leq n$. Also, we know $t_i \geq d_j$.

Case 2-Part 1 is also trivial. Switch $t_i$ and $d_j$, then connect $S$ to $d_j$ instead of $t_j$. This creates the same structure as `Case 1`.

Case 2-Part 2 requires some thinking. Let $W \in T_i$ but $W \notin D_j$. Then, remove $\\{S, D_j\\}$ and $\\{T_i, W\\}$, and replace them with $\\{S, T_i\\}$ and $\\{W, D_j\\}$. Similarly to `Case 2-Part 1`, this creates the same structure as `Case 1`.
* This method effectively preserves the degree sequence as well.

$\therefore$ $d$ is graphic IFF $d\prime$ is graphic.
