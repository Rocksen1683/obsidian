The [[Network Layer]] passes a *datagram* to the link layer, which prepares to send a *frame* containing this datagram. 

The header and footer of the frame carry the link layer information. 

### Frame Read Approaches 
- Byte-Oriented Protocols: BISYNC, IMP-IMP, PPP
- Bit-Oriented protocols: HDLC 
- Counter-based approach: DDCMP
- Clock-based approach: SONET 

### Common Approach 
Delineate frame with a special pattern called a *flag*, ex `01111110`

The problem with this approach is if the flag variable `01111110` is part of the payload. 

To fix this, we can introduce *stuffing* but this could head to high overhead in processing. 

### Bit-Oriented Protocols
This approach would treat the link as a bit stream and will have special bit patterns:
- *flag*: `01111110`
- *idle*: `01111110`
- 