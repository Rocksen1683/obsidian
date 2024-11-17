Would it be possible to run [[Dijkstra's Algorithms]] on a  [[MapReduce]] job. 

![[Pasted image 20241107132723.png]]

## Pseudocode (Unweighted Edges)
```
def map(id, node):
	emit(id, node)
	for m in node.adjList:
		emit(m, node.d + 1)
```

```
def reduce(id, values):
	d = infinituy 
	node = None 
	for o in values:
		if isNode(o):
			node = o 
		else:
			d = min(d, o)

		node.d = min(node.d, d)
		emit(id, node)
```

## Pseudocode (Weighted Edges)
```
def map (id, node): 
	emit(id, node) 
	for m in node.adjList: 
		emit(m.id, node.d + m.w))
```

```
def reduce (id, values):
	d = infinity
	node = None
	for o in values: 
		if isNode(o):
			node = o
		else:
			d = min(d, o)
		node.d = min(node.d, d)
		emit(id, node)
```


