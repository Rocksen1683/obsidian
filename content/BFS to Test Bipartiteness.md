## Algorithm 
Suppose $G$ connected, run [[Breadth First Search for Undirected Graph]] from and $s$, and set 
- $V_{1}:$ vertices with odd level 
- $V_{2}:$ vertices with even level 
Then $G$ is bipartite *if and only if* all edges have one end in $V_{1}$ and one end in $V_{2}$ (this is testable in $O(m)$)

