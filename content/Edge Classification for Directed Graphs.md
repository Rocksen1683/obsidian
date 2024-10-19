![[Pasted image 20240215164040.png]]

We can have the following classification of edges in a [[Directed Graph]]

#### Tree Edges 
Regular Edges that get visited in [[Depth First Search for Undirected Graph]]

#### Back Edges 
From a *descendant* to *ancestor*

If we are going from $v \rightsquigarrow w$ and $w$ is not finished, then $(v, w)$ is a **back edge**



#### Forward Edges 
From *ancestor to descendant* but not a tree edge 

A forward edge is when we start from a vertex $v$, reach vertex $w$ indirectly and $w$ is finished. Now if there exists a direct edge $(v, w)$ it means it's a forward edge

$$start[v] < start[w] < finish[w]$$

#### Cross Edges 
Edges that are not *forward* or *back* and basically connect one tree to another 

A cross edge is when we reach a vertex $v$, and we realize that there exists an edge $(v, w)$, where $w$ has already been visited then $(v, w)$ is a *cross edge* 
$$start[w] < finish[w] < start[v]$$
