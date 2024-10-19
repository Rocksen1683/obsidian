## Recursive 

Data Structure used: **Hash Set**

**Hash Set** is used to track whether we have visited a vertex or not 
### Implementation 

``` python 
def DFS_Helper(G, v, visited):
	#visit the vertex 
	visited.add(v)
	print(v) 

	#iterate through the neighbors 
	for i in G[v]:
		if i not in visited: 
			#this will recursively go depth first
			DFS_Helper(G, i, visited)


def DFS(G, v):
	#G is a graph, v is a source vertex 
	visited = set() #keep track of whether we visit a vertex or not 
	DFS_Helper(G, v, visited)
```

