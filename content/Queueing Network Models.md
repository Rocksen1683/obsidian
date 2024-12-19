*Queuing Network Models* characterize the software's performance in the presence of *dynamic factors*, such as work loads or multiple users. 

It gives us a precise metrics that account for *resource contention* and sensitivity of performance metrics to variations in workload composition. 

Also helps in identification of *bottleneck* resources and comparative data on *performance improvement options*. 

[[Queueing Network Models]] represents the key computer system resources as queues and servers. 
- A *server* represents a component of the environment that provides some service to the software (like a processor, disk, etc)
- A *queue* represents jobs waiting for service 

### Queues
![[Pasted image 20241209210954.png]]

Follows [[Kendall Notation]].

## Performance Metrics 
*Performance Metrics* of interest of each server are: 
- *Residence Time* ($RT$): the average time jobs spend in the server, in service and waiting
- *Utilization* ($U$): the average percentage of the time the server is busy 
- *Throughput* ($X$): the average rate at which jobs complete service
- *Queue Length* ($N$): the average number of jobs at the server (receiving service and waiting)

### Execution Profile
![[Pasted image 20241212153052.png]]
### Calculation of Performance Metrics 
![[Pasted image 20241212153116.png]]

### [[Utilization Law]]
### [[Little's Law]]

## [[Queue Analysis]]

## [[Types of Queuing Network Models]]