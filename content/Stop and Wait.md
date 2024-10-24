Is a *simple* mechanism where the sender sends one packet (encapsulated in a frame) and then *waits* for the receiver's response. The sender won't send the next packet until it gets an acknowledgement from the receiver.

To ensure this works, we would need the following structure:
- *Acknowledgements (ACK)*: receiver explicitly tells the sender that the packet has been received without any issues 
- *Negative Acknowledgements (NAK)*: receiver explicitly tells the sender that the packet had errors which leads the sender to *retransmit* the packet. 

![[Pasted image 20241024140155.png]]

## Problems 
### Data Loss 

In the case of a *data loss*, the sender keeps waiting for an acknowledgement from the receiver for an infinite amount of time. After the system has gone through a *timeout*, the sender then resends the same packet 

![[Pasted image 20241024140259.png]]

### Acknowledgement Loss 
In the case where the *acknowledgement* gets lost, the sender *waits* for an infinite amount of time for an acknowledgement from the receiver. 

![[Pasted image 20241024140502.png]]

### Delayed Acknowledgement 
![[Pasted image 20241024140922.png]]

### ACK Loss with SN's 
![[Pasted image 20241024140951.png]]

## Performance 

![[Pasted image 20241024142137.png]]
![[Pasted image 20241024142207.png]]
![[Pasted image 20241024142223.png]]
