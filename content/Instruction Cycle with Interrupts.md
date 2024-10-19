To accommodate interrupts, we add a new stage called the *interrupt stage* to the instruction cycle specified in [[Instruction Execution]]. 

![[Pasted image 20240128164324.png]]
### What happens in the Interrupt Stage 
- In the interrupt stage, the processor checks to see if any interrupts have occurred, indicated by the presence of an interrupt signal. 
- If no interrupts are pending, the processor proceeds to the fetch stage and fetches the next instruction of the current program.
- If there are interrupts pending, processor switches to the *interrupt handler* routine which checks the type of interrupt and appropriately executes 