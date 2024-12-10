*Subnets* are parts of a sub-part of a network and is a set of interfaces that have IP Addresses with the same *prefix* and subnet portion. They can physically reach each other *without passing* through an intervening router, 

![[Pasted image 20241203134441.png]]

## Getting a subnet address 

When a device gets an IP Address, it is given `a.b.c.d/x`, i.e an address and a prefix `x` where `x < 32`. [[Subnet Mask]]

Now to get the actual subnet address, we would need to do a *bit-wise AND* between the IP Address and the [[Subnet Mask]].

![[Pasted image 20241203135137.png]]
![[Pasted image 20241203135146.png]]
