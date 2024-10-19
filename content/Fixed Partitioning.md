Not used as much now but used to be. 

Technique where main memory would be split into *fixed partitions*
It is easy to implement. 
#### Weaknesses
- inefficient use of memory 
- would only be able to handle a *fixed* maximum amount of processes. 
### Partition Sizes 
- **Equal Sizes** - This would be very easy to implement but would be **very** inefficient as we would sometimes have to allocate big blocks of memory for little data 
	- This would be called *Internal Fragmentation*
- **Unequal Sizes** -  Much more efficient compared to equal sizes 
	- Way to assign process would be to assign each process to the smallest partition within which it will fit 
