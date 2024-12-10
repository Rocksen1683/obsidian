![[Pasted image 20241204175044.png]]

In the case that the [[Network Layer]] sends information at a rate faster than the [[Application Layer]] clears it's buffers, then it won't be handle the *flow* of the incoming data. 

*Flow Control* is the mechanism where the receiver controls the sender so that the sender won't overflow the receiver's bugger by transmitting too much, too fast. 

[[TCP Flow Control]] works in the following way: 
- *TCP Receiver* "advertises" the free buffer space in the `rwnd` field in the *TCP Header*. `RcvBuffer` size is set via socket options 
- *TCP Sender* limits the amount of `unACKed` data to received `rwnd`
With this mechanism, the receive buffer will not overflow

![[Pasted image 20241204175520.png]]