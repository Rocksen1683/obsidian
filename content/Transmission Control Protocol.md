*TCP* is a *point-to-point* protocol with a reliable, in-order byte stream. It uses *cumulative ACK's* and *pipelining*.

![[Pasted image 20241204170641.png]]

## Segment Structure
![[Pasted image 20241204170721.png]]
The [[Transmission Control Protocol]]'s header has variable length due to some optional fields which is why it's necessary to have a header length. 

### TCP Sequence Numbers 
Byte stream "number" of first byte in segment's data. 
### TCP ACKs
Sequence number of next byte expected from the other side and is cumulative ACK. 

![[Pasted image 20241204171430.png]]

### TCP Round Trip Time, Timeout 
If the *timeout* value is too short then we will have a premature timeout and unnecessary retransmissions. if it's too long then we'll have a slow reaction to segment loss. An ideal *timeout* value would be longer than the  *round trip time* or *RTT*.

To estimate *RTT*, we can measure the time from segment transmission until the ACK Receipt and this process is known as `SampleRTT`.  However we would want our estimate to be smoother with less change but `SampleRTT` varies a lot. 

Instead we can compute something called the `EstimatedRTT` which would be 
![[Pasted image 20241204172033.png]]

Now with `EstimatedRTT`, we can calculate the `TimeoutInterval` by adding some `safety margin` to the `EstimatedRTT`.

![[Pasted image 20241204172138.png]]

## TCP Sender 
![[Pasted image 20241204172330.png]]

## TCP Receiver 
![[Pasted image 20241204172749.png]]

![[Pasted image 20241204172821.png]]
![[Pasted image 20241204174503.png]]
![[Pasted image 20241204174509.png]]

## [[TCP Flow Control]]
## [[TCP Connection Maagement]]