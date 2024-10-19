A group of instructions on an associated object (data) that must be performed atomically is called a ***critical section***

One way to handle this is to detect any sharing and serialize all access; wasteful if threads are only reading. 

Improve by differentiating between reading and writing 
- allow multiple readers or a single writer; still wasteful as a writer may only write at the end of its usage.