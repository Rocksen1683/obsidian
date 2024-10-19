![[Pasted image 20240912131257.png]]
In a *distributed file-system*, we break down large files into smaller *shards* which are then assigned to different servers for respective processing. 

This process is called [[Sharding]].

Now, it is quite common for a server to have some hardware failure which leads to some data loss. To avoid this, we can use something called [[Replication in DFS]]

Data Coherency 
	• Write-once-read-many access model 
	• Client can only append to existing files
 Files are broken up into blocks 
	 • Typically 64MB block size 
	 • Each block replicated on multiple DataNodes 
 Intelligent Client 
	 • Client can find location of blocks 
	 • Client accesses data directly from DataNode
### [[Hadoop Distributed File System]]
### [[Google File System]]