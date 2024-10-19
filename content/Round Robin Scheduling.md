To help mitigate issues with *short processes* in [[First Come First Served (FCFS)]], we can define a *time-slice* which would be some time period after which the current running process pre-emptively (using a *clock interrupt*) is moved into ready and the next process in the queue will start executing for the next time slice. 

A huge design consideration with this would be to choose the *time-slice* as if it is too short, short processes will move quickly but the overhead for the clock interrupt would increase. If the *time-slice* is small, the throughput would also be relatively low. 

It still has issues with I/O processes as usually a I/O process would need resources from I/O device which usually cannot be acquired in a single time-slice. 

To avoid this unfairness, we can make an improvement to *Round Robin* called *Virtual Round Robin* which uses an auxiliary queue  that is based on the [[First Come First Served (FCFS)]]  policy which increases throughput. 

![[Pasted image 20240326164050.png]]
