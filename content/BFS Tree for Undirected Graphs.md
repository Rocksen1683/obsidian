## Definition 
The BFS Tree $T$ is the subgraph made of: 
- all $w$ such that parent$[w] \neq NIL$
- all edges $\{w,$parent$[w]\} \neq NIL$ for some $w$ as above (except $w = s$)
### Claim 
The BFS tree $T$ is a tree (no cycles and fully connected)
### Proof 
We can prove it by induction on the vertices for which parent$[v]$ is not $NIL$. 
![[Pasted image 20240125133840.png]]

## Shortest paths from the BFS Tree
### Claim 1
 The levels in the queue are *non-decreasing*. 
### Proof 
 The levels in the queue are *non-decreasing* because we start with the source vertex at level $0$ and increment by $1$ as we assign it's children. As we are going [[Breadth First Search for Undirected Graph]], we go through a *level-order* traversal which means we visit all nodes of same level first making the queue *non-decreasing*. 

### Claim 2
For all vertices $u, v$, if there is an edge {$u, v$}, then level$[v]$ $\leq$ level$[u] + 1$
### Proof 
If we dequeue $v$ before $u$, then
$$level[v] \leq level[u]$$


