A *disk cache* is a small portion in main memory reserved for disk sectors. Contains copies of some sectors on the disk. 
- When a I/O request is made to the disk: 
	- Check whether requested sector in *disk cache* $\implies$ request satisfied by cache 
	- If not, requested sector $\to$ read into *disk cache* from disk