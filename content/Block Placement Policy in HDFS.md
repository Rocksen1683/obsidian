[[Hadoop Distributed File System]] maintains $3$ replicas that will be stores on *at least* $2$ racks 
- One replica on local node
- Second replica on a remote rack
- Third replica on the same remote rack

Clients read from the *nearest* replica. 

This is the *default* policy and can be changed if necessary. 