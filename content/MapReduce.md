Google framework :)

Two functions:
- *Map*: Maps a $1:n$ relation  
- *Reduce*: aggregates a bunch of results together   

If the input is a text file, *key* would be the position of a line and *value* would be the text of a line.

The *Reduce* step aggregates the values that have the same key.

```
map: (k1, v1) -> List[(k2, v2)]
reduce: (k2, List[v2]) -> List[(k3, v3)]
```

### Example
If we're counting the word `Waterloo` in two paragraphs:
```
MAP:
P0: {'Waterloo' : 4}
P1: {'Waterloo' : 5}

REDUCE:
{'Waterloo' : [4, 5]}  -> {'Waterloo' : 9}
```

![[Pasted image 20240910131839.png]]


### How much memory will this use?
It would be `O(n)` where n describes the number of unique words. 

### WordCount MapReduce Implementation

```Python
def map(key, value):
	counts = Counter()
	
	for word in tokenize(value):
		counts[word] += 1
		
	return counts.items()


def reduce(key, values):
	sum = 0 
	for v in values:
		sum += v 
	emit(key, sum)
```

### WordCount MapReduce Alternative Implementation
```Python 
def map(line):
	for word in line:
		emit(word, 1)

def reduce(key, values):
	sum = 0 
	for v in values:
		sum += v 
	emit(key, sum)
```

Problem with this approach:
The *Reduce* server is getting too much data :( If the file was 10TB, the server will be getting more than 10TB of data. 

Solution? **Use Multiple Reducers**

### Multiple Reducers

```
map: (k1, v1) -> List[(k2, v2)]
reduce: (k2, List[v2]) -> List[(k3, v3)]
partition: (k2, v2, n in N) -> [0, n)
```

**Partition** will default to a hash function that results in a particular reducer that deals with some word. 

```Python 
def map(line):
	for word in line:
		emit(word, 1)

def reduce(key, values):
	sum = 0 
	for v in values:
		sum += v 
	emit(key, sum)

def partition(key, reducer_count):
	return hashcode(key) % reducer_count
```

What if we did one value per key per mapper?
### Combine

```
map: (k1, v1) -> List[(k2, v2)]
combine: (k2, List[v2]) -> List[(k2, v2)]
reduce: (k2, List[v2]) -> List[(k3, v3)]
partition: (k2, N) -> N
```

```Python
def combine(key, values):
	sum = 0 
	for v in values:
		sum += v 
	emit(key, sum)
```

Combine is an **optional** optimization step that will be framework dependent. 

Combine *might* be the same as reduce if $k_{2} = k_{3}, v_{2} = v_{3}$

### [[Averages in MapReduce]]

## [[Physical View of MapReduce]]
### [[Hadoop]]

## [[Distributed File System]]

### [[Combiners in MapReduce]]
