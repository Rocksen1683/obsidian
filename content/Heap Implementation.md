To implement a heap in Python, you would need the following:
### Min-Heap
```python 
import heapq

heap = [2, 3, 4]
heapq.heapify(heap)

heapq.heappush(heap, 1)

minElement = heapq.heappop(heap) #returns 1
```

### Max-Heap
```python 
import heapq 

heap = [2, 3, 4]
maxHeap = [-1 * x for x in heap]

heapq.heapify(maxHeap)

heapq.heappush(maxHeap, -5)

maxElement = -1 * heapq.heappop(maxHeap) #returns 5
```
