Let us start from a *rooted DFS Tree* $T$, knowing parent and levels. 
**Assumption:** $G$ is connected 

#### Claim 
> The root $s$ is a cut vertex if and only if it has more than one child 
#### Proof 

$[\implies]$ If $s$ has one child, removing $s$ leaves $T$ connected, so not a cut vertex 

$[\impliedby]$ If $s$ has subtrees $S_{1}, ..., S_{k}, k > 1$. We know that there is no edge connecting $S_{i}$ to $S_{j}$ for $i \neq j$. This means that removing $s$ gives us $k$ connected components. 

![[Pasted image 20240215161101.png]]

