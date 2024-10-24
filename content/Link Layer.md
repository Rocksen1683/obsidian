## Role 
The link layer is responsible to act as a communication channel that *directly* connects physically adjacent nodes over a link. Also responsible for transferring a *datagram* from one node to another. 
## What do we need?
### Framing 
- Is ***compulsory***.
- We would need to encapsulate the datagram into *frame*,adding header, trailer. 
- MAC addresses in frame headers to identify source, destination 
- How it works? -> [[Link Layer Framing]]
### Error Detection
- Not necessarily compulsory
- Detection for errors caused by signal attenuation and noise 
- Receiver detects errors, signal retransmission
- How to deal with them? -> [[Link Layer Error Detection]]
### Error Correction 
Receiver *identifies* and *corrects* bit errors without retransmission. 
### Reliable delivery between adjacent nodes
Always used for links with *high error rates*, but is not as useful for links with *low error rates*.

### Flow Control 
Pacing between adjacent sending and receiving nodes. 

## Structure 
The link layer is mainly implemented on the *Network Interface Card (NIC)*
### Sending Side 
- encapsulates the *datagram* in a *frame* ([[Link Layer Framing]])
- Adds error checking bits ([[Parity Checking]]) , reliable data transfer, and flow control 

### Receiving Side 
- Looks for errors ([[Link Layer Error Detection]]), flow control, etc 
- Extracts datagram and passes it to the [[Network Layer]] 