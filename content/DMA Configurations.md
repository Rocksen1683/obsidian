There are $3$ popular ways of configuring DMA 
### 1. Single-bus, detached DMA 

![[Pasted image 20240408230023.png]]
- Both DMA and I/O use same system bus
- Data transfer is *inexpensive*  but very *inefficient*

### 2. Single-bus, integrated DMA-I/O

![[Pasted image 20240408230151.png]]

- There is a path from DMA to I/O modules that does not use the system bus 
- *DMA* logic could be implemented within the modules or we could have a separate IO module that controls the other modules
### 3. I/O Bus
![[Pasted image 20240408230452.png]]
- Separate I/O bus that acts as a link for all I/O modules
- the system bus that the DMA module shares with the processor and main memory is used by the DMA module only to exchange data with memory and to exchange control signals with the processor.
- The exchange of data between the DMA and I/O modules takes place off the system bus.****