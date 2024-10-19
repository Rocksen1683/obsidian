### Definition and Notation
A graph $G$ is a pair$(V, E)$ such that: 
- $V$ is a finite set, whose elements are called **vertices**
- $E$ is a finite set, whose elements are *unordered pairs of distinct vertices*, and are called **edges**
**Convention:** $n$ is the number of vertices and $m$ is the number of edges 
### Data Structures for Undirected Graphs
- **Adjacency List:** an array $A[1_{..}n]$  such that $A[v]$ is the *linked list* of all edges connected to $v$. 
	- $2m$ list cells, total size $\Theta(n+m)$, but testing if an edge exists is not $O(1)$
- **Adjacency Matrix:** a $(0, 1)$ matrix $M$ of size $n \times n$ , with $M[v, w] = 1$ iff $\{v, w\}$ is an edge

### Graph Terminology 
- **Path:** A sequence $v_1...,v_{k}$ of vertices with {$v_{i}, v_{i+1}$} in $E$ for all $i$
- **connected graph:** $G = (V, E)$ such that for all $u, w$ in $V$, there exists a path from $u\rightsquigarrow w$
- **cycle:** a path $v_{i}, ..., v_{k}, v_{i}$ where the length of path $> 3$
- **tree:** a connected graph with no cycles 
- **rooted tree:** a *tree* with a special vertex called *root*. 
- **subgraph:** A graph $G' = (V', E')$ is a subgraph if $V' \subset V$, $E' \subset E$ and if all edges in $E'$ are between vertices in $V'$

