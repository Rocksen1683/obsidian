A *DMA* module controls the exchange of data between main memory and the I/O Module. So with this the I/O module can request a block of data from main memory without interrupting the processor (except at the beginning and the ending of the transaction).
![[Pasted image 20240408225353.png]]

When the processor sends a request to the *DMA module*, it sends the following information 
- Read or write operation 
- Address of the device involved 
- Starting location in memory to read or write 
- Number of words to be read or written 
After the *DMA* finishes it's business with the data, it sends an interrupt to the processor. 

[[DMA Configurations]]