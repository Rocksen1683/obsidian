An *in-order* [[DFS for Trees]] is a traversal where we go depth first and in-order. 

![[Pasted image 20240213150642.png]]

For the above example [[Binary Search Tree]], the *in-order* traversal would be:
$$4 \rightarrow 2 \rightarrow 5 \rightarrow 1 \rightarrow 3$$
**Order of Traversal:** left $\rightarrow$ root $\rightarrow$ right
## Implementation 

```python 
def inOrder(node):
	#visiting the left 
	inOrder(node.left)

	#visiting the current node 
	print(node.val)

	#visiting the right node 
	inOrder(node.right)

def DFS(root):
	inOrder(root)

```

**Time Complexity:** $O(n)$ as we visit every node once 
**Space Complexity:** $O(\log n)$ for [[Binary Search Tree]]

## Iterative Implementation 

``` python 
s = [] #stack 

def inOrder(node):
	current = node
	 while current or s: 

		#go left most 
		if current is not None: 
			s.append(current) #add to stack 
			current = current.left  

		else: 
		#we are at left most and stack still exists 
			#pop top element of stack 
			current = s.pop()
			print(current) #in-order 
			current.pop

			current = current.right 


```
