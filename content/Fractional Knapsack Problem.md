## Problem Definition 
#### Input 
- $n$: number of objects 
- $m:$ weight that your *knapsack* can hold
- $o:$  $n$ objects 
- $p:$ each object has a price $p$
- $w:$ each object has a weight $w$

The main Difference between this and the [[0 1 Knapsack Problem]] is that we are allowed to take objects *fractionally* which is why we use [[Greedy Algorithms]] instead of [[Dynamic Programming]].
## Pseudocode 

```
#calculate price/weight for each object 
pw = []
knapsack_prof = 0

def getMax(arr): 
	# remove max element every time
	max = arr.remove(max(arr))
	maxIdx = #index 
	return max, maxIdx

while m > 0: 
	max, maxIdx = getMax(pw)

	#greedy decision 
	if m - w[maxIdx] > 0: 
		knapsack_prof += p[max]
		m -= w[maxIdx]
	else:
		knapsack_prof += p[maxIdx]/m
		m -= w[maxIdx]/m 

return knapsack_prof
```
