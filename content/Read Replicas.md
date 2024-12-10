*Read Replicas* are a *full copy* of all the dataa and they can handle *read* requests (SELECT). 

Data changes are pushed to read replicas, although the replicas might be slightly behind the primary database. So any read requests that are *sensitive to consistency* should use the primary database. 

We shouldn't have too many read replicas though as it would make the data push process a bottleneck in the primary. 

![[Pasted image 20241207223029.png]]
![[Pasted image 20241207223527.png]]

### Replication Shortcomings
While [[Read Replicas]] makes *reads* scalable, it does not do the same with *writes* as they are still all handled in one database machine (primary). 

*Capacity* is also not scalable as all the data must fit on each database machine. 

