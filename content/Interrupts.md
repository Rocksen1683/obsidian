Interrupts are provided mainly to improve processor utilization. 

### Why do we need interrupts? 
Usually other devices are slower than your computer and if we were just following the *instruction cycle*  in [[Instruction Execution]] , the processor would have to wait a long time until the I/O device catches up to move to the next cycle. To reduce this wait and time-wastage, we have interrupts. 

### Classes of Interrupts 

![[Pasted image 20240128161652.png]]

### Interrupts and Instruction Cycle 
This is how the *instruction cycle* works with interrupts 
- Program reaches a point where it can make a ***WRITE*** call 
- I/O program is invoked with preparation code and actual command. After few instructions, control is returned back to main 
- While main is running the next set of instructions, the I/O device accepts data from memory concurrently 
- When the I/O device is ready with it's preparation and data transfer, it sends an *interrupt request* to the processor 
- Processor suspends running of current instruction and branches of to a routine called the *interrupt handler*
- The *interrupt handler* executes the I/O code and branches back to the processor to execute the original code 

## Detailed Information
### [[Instruction Cycle with Interrupts]]

### [[Interrupt Processing]]

### [[Multiple Interrupts]]
