An improvement over [[Single Buffer]] can be had by assigning two system buffers to the operation. A process now transfers data to (or from) one buffer while the operating system empties (or fills) the other. This technique is known as *double buffering* or *buffer swapping* .
![[Pasted image 20240409002040.png]]

### Block-Oriented Transfer 
For *block-oriented* transfer, we would have an increase in speed over [[Single Buffer]]. This comes with increased complexity tho 😞
### Stream-Oriented Transfer 
#### Line at a time I/O 
User process *not suspended* unless the process runs ahead of the double buffers 
#### Byte at a time I/O 
- No particular advantage over single buffer of *twice the length*
- Still follows [[Producer and Consumer Problem]]