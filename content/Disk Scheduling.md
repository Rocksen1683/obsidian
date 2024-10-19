### Quick Definitions 
- ***Seek Time:*** Time taken to position the *head* at the track 
	- consists of initial startup time and track traversal time 
	- track traversal time is *not linear* and includes a *settling time*
- ***Rotational Delay:*** Time taken for the beginning of the sector to reach the head 
	- basically time required for addressed area of disk to rotate into accessible position 
- ***Access Time:*** Sum of seek time and rotational delay 
- ***Transfer Time:*** The time taken for data transfer during the read/write operation
- ***Rotational Positional Sensing (RPS):*** seek command issued $\to$ channel released to handle other I/O operations. Seek completed $\to$ device determines when data will *rotate* under the head 

## [[Disk Scheduling Policies]]