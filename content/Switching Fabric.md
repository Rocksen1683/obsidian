The *switching fabric* is the MOST Important part of the [[Router Architecture]] and is responsible for transferring the packet from the input link to the respective output link. 

*Switching Rate* is the rate at which packets can be transferred from inputs to outputs. 
- measured as the multiple of input/output line rate
- $N$ inputs: switching rate $N$ times line rate desirable 
![[Pasted image 20241203160056.png]]

### Switching via Memory 
Used in first-generation routers where the packet is copied to system''s memory. Due to the memory copying, this method had a lot of speed limitations.

![[Pasted image 20241203160706.png]]

### Switching via bus
Datagram from input port memory to output port memory via a shared bus. Here the switching speed is limited by the *bus bandwidth*.
![[Pasted image 20241203160941.png]]

### Switching via Interconnection Network 
![[Pasted image 20241203161303.png]]
![[Pasted image 20241203161311.png]]
