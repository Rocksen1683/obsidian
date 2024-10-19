$DFS(G)$ gives us a partition of $G$ into vertex-disjointed rooted trees $T_{1}..., T_{k}$ which is known as the [[DFS Forest]]. 

## Ancestor and Descendants
> $u$ is an **ancestor** of $v$ if they are on the same tree $T_{i}$ and $u$ is on the path $root \rightsquigarrow v$

This means that 
> v is a **descendant** of $u$

### Claim 
> All edges in $G$ connect to a vertex to one of its descendants or ancestors 

#### Proof
Let {$v, w$} be an edge, and suppose we visit $v$ first. 

Then when we visit $v$, ($v, w$) is an unvisited path between $v$ and $w$, so $w$ will become a *descendant* of $v$ $[$ using [[White Path Lemma]] $]$



