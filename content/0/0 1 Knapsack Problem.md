### Input 
- Items $1,..., n$ with *weights* $w_{1}, w_{2}, ..., w_{n}$ and *values* $v_{1}, ..., v_{n}$
- a *capacity* $W$
![[Pasted image 20240305130506.png]]

## Solution
### Approach 
Either we choose the item or not. 
The *max value* with items $1$ to $n$ is: 
- If item $n$ is *not chosen*:
	- max value that we can get with weight $w$ and items $1$ to $n-1$ 
- if item $n$ is *chosen*:
	- $v_{n}+$ max value that we can get with weight $w - w_{n}$ and items $1$ to $n-1$

Using an array of $i = 1...$n and $w = 1,...W$
We want to find the *max value* achievable using a knapsack of capacity $w$ and item $1,...,i$

### Pseudocode 
```
01Knapsack(v_1, ..., v_n, w_1, ..., w_n, W):
initialize an array O[0..n, 0..W]
with all O(0, j) = 0 and all O(w, 0) = 0
for i = 1, ..., n:
	for w = 1,... W: 
		if w_i > w:
			O[w, o] = O[w, i-1]
		else:
			O[w,i] = max(v_i + O[w-w_i, i-1], O[w,i-1])
```

**Runtime:** Time complexity would be $\Theta(nW)$
**Note:** green arrow means *don't include*, red arrow means *include*

This is still a sad 😔 approach 😭 and is expensive.
![[Pasted image 20240305135905.png]]
