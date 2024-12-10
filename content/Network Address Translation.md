*NAT* is used to limit the number of addresses given to a home or an office networks and tries to reuse IP addresses in a smart way. 

![[Pasted image 20241203145953.png]]

![[Pasted image 20241203150306.png]]

## Implementation 
The *NAT Router* must do the following: 
-  *Replace* the Source IP, address, port number of every outgoing datagrams to NAT IP, new port number
- *Remember* in the NAT Translation Table, every source IP, address, port number to NAT IP, new port number translation pair 
- *Replace* incoming datagrams in destination fields of every incoming datagram with the corresponding source IP, address, port number stored in the NAT Table

![[Pasted image 20241203154435.png]]
![[Pasted image 20241203154500.png]]

### NAT Load Balancer
![[Pasted image 20241208150224.png]]
