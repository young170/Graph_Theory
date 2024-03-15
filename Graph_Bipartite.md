## Introduction
This note consists of proofs related to [bipartite](https://github.com/young170/Graph_Theory/blob/main/Graph_Fundamentals.md#bipartite) graphs.

The proof is a two part proof. This is because the theorem states an *if and only if* (IFF) statement.

## Theorem
Let $G = (V, E)$ be an undirected graph.<br>
Then, $G$ is a bipartite graph **IFF** it has no odd [cycles](https://github.com/young170/Graph_Theory/blob/main/Graph_Fundamentals.md#cycle).

## Proof
### If a Graph is Bipartite $\Rightarrow$ It Has no Odd Cycles
Let $G = (V, E)$ be bipartite.<br>
Then by definition, let $V = A \cup B$ such that, $A \cap B = \emptyset$, and that all edges $e \in E$ are in the form, ${a, b}$ where $a \in A$ and $b \in B$.

Using **proof by contradiction**, suppose $G$ has (at least) one cycle $C$ with odd length.<br>
Let the length of $C$ be $n$.<br>
Let $C = (v_1, v_2, ..., v_n, v_1)$.
$w.l.g.$ let $v_1 \in A$. It follows that $v_2 \in B$ and hence $v_3 \in A$, and so on.<br>
Hence, we see that $\forall \, x \in {1, 2, ...n}$, we have:
$$
v_k=
\begin{cases}
A & k \text{is odd}\\
B & k \text{is even}
\end{cases}
$$
By definition, $n$ is odd, $v_n \in A$.<br>
But $v_1 \in A$, and $(v_n, v_1) \in C_n$.<br>
So, $(v_n, v_1) \in E$ contradicts the assumption that $G$ is bipartite.<br>
$\therefore$ If $G$ is bipartite, then it has no odd cycles.

## If a Graph Has no Odd Cycles $\Rightarrow$ It is a Bipartite Graph


