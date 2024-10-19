## What do we need?
### Framing 
- Is ***compulsory***.
- We would need to encapsulate the datagram into *frame*,adding header, trailer. 
- MAC addresses in frame headers to identify source, destination 
### Error Detection
- Not necessarily compulsory
- Detection for errors caused by signal attenuation and noise 
- Receiver detects errors, signal retransmission
### Error Correction 
Receiver *identifies* and *corrects* bit errors without retransmission. 

### Reliable delivery between adj nodes
Always used for links with *high error rates*, but is not as useful for links with *low error rates*.


