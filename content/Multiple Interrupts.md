What happens when we have Multiple Interrupts? Earlier in [[Interrupt Processing]], we talked about how the processor *chooses* which interrupt handler to run. Let's see how it actually works. 

## Sequential Approach 
One approach to handle multiple interrupts, is to *disable interrupts* when dealing with one of them and *re-enable* them after the [[Interrupt Processing]]. This means that if an interrupt occurs when something is processing, it is *disabled* until it's completed. 

![[Pasted image 20240128171102.png]]
### Drawbacks of Sequential Interrupts 
**Main Issue:** No way of measuring *relative priority* or taking into account *time-sensitive* interrupts
## Transfer of Control Approach 
A better approach would be to define priorities for interrupts and allow a *high-priority* interrupt to interrupt a  *low-priority* one. 

![[Pasted image 20240128171627.png]]

![[Pasted image 20240128171642.png]]