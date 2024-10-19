The simplest type of buffer, when a user process issues an I/O request, the OS assigns a *buffer* in the main memory to the operation., 

### Block Oriented Devices 
Buffering scheme can be described as 
- Input transfers are made to system buffers 
- When the transfer is complete, the process moves the block into user space and immediately requests another block. This is called *reading ahead*, or anticipated input; it is done in the expectation that the block will eventually be needed

This leads to a speedup as we would be processing one block data while the next block is being read in. This also complicates the implementation of *swapping*.

Similarly for block-oriented output, data moves from user space into system buffer -> written out 

### Stream Oriented Devices 
The single buffering scheme can be used in a line at-a-time fashion or a byte-at-a-time fashion. 
#### Line at a time Operation 
- Line-at-a-time operation is appropriate for scroll-mode terminals (sometimes called dumb terminals)
- User process is suspended during input, waiting for the arrival of the entire line 
#### Byte at a time Operation
- Byte-at-a time operation is used on forms-mode terminals and peripherals like controllers 
- Interaction between OS and user process -> [[Producer and Consumer Problem]]
-
