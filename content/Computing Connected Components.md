## Algorithm 
```
#After BFS while loop, add the following 

for v in G(V):
	if visited[v] = false:
		#recursively call BFS on that vertex to enter new component
		BFS(v)
```

## Complexity 
The complexity will still be $O(n+ m)$ like [[Breadth First Search for Undirected Graph]] as we still visit each vertex and edge linearly and only once. 
