Is a high speed cache for page table look-up and contains page table entries that have been *most recently used*. 

Given a virtual address, the processor will first examine the TLB. If the desired page table entry is present (TLB hit), then the frame number is retrieved and the real address is formed.

If not desired page table entry is not found (TLB miss) so we go through it normally. 

![[Pasted image 20240311004646.png]]

![[Pasted image 20240310231619.png]]