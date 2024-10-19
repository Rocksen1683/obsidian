In *FCFS* scheduling, the next process is chosen based on the amount of time it's been present in the *ready queue*.

![[Pasted image 20240326161855.png]]

This type of scheduling favors *lengthy processes* as shown above faces the following issues: 
- Does not have a good turnaround ratio when you have *short processes*
- Favors *processor-bound* processes over *I/O-bound* processes which could cause issues as usually I/O bound processes are not in the ready queue for as long as the processor bound processes. 

Not recommended to use on it's own but when combined with other [[Scheduling Policies]], could be effective. 