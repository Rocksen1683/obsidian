*Cache* is small and fast-memory that exploits [[Locality of Reference]] to ensure that memory that gets accessed a lot is really fast.

## Cache and Main Memory 

![[Pasted image 20240128180949.png]]

The *cache* contains a small portion of the main memory and whenever the processor is looking for something, it performs a check if it exists in the cache or not. If it *does not* exist in the cache, then data is transferred from main memory to cache and is delivered to the processor as shown above.  

Due to [[Locality of Reference]], it is likely that many of near-future memory references will be to other bytes in the block (spatial locality)

![[Pasted image 20240128182057.png]]

## [[Cache Design]]
