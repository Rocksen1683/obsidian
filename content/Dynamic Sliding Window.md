Dynamic *length* for window.

Example: Smallest sum that is >= to some value $s$.


## Template 
```Python
nums = [] #array 
globalMin = #return value
windowStart = 0

for windowEnd in range(len(nums)):
	while(question condition):
		globalMin = min(globalMin, windowEnd - windowStart + 1)
		windowStart += 1


return globalMin
```