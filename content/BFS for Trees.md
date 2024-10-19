It means *level-order* traversal of a BST.
Data Structures Used: **Queue**
## Implementation 
```python 
def BFS(root):
	#empty queue 
	Q = []
	Q.append(root)

	#checking if we have visited or not 
	order = []
	
	while Q:
		#pop left 
		node = Q.pop(0)
		order.append(node.val)
		if node.left:
			Q.append(node.left)
		if node.right:
			Q.append(node.right)

	#order of values 
	return order
	
```

