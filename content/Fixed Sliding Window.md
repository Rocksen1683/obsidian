Our sliding window will have a fixed *length*. 

Example: Max sum subarray of size $k$.

## Template

```Python

nums = [] #some array 
# let k be the size of the array 
globalVal = #global return value 
windowVal = #value that window is calculating

for i in range(len(nums)):
	windowVal += nums[i]

	if (i >= k-1): #maintaining length k for window
		windowVal -= nums[i-k-1]

	globalVal = max(globalVal, windowVal)

return globalVal
```

