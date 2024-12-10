Dynamic Host Configuration Protocol or *DHPC* is used to *dynamically* obtain IP Addresses from the network server when it joins the network. 

It's a *client server* protocol using [[User Datagram Protocol]]:
- hosts broadcasts DHCP *discover* message
- DHCP Sever responds with DHCP *offer* message 
- Host requests IP Address with DHCP *request* message
- DHCP Server then sends address with DHC *ack* message
![[Pasted image 20241203141852.png]]
![[Pasted image 20241203141901.png]]

DHCP will also return the following along with the IP Addresses: 
- address of the first-hop router for client 
- name and IP Address of DNS Server 
- Address and prefix 

DHCP is a network function implemented as an application protocol.

