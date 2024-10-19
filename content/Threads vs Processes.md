## Processes vs Threads 
So far we have talked about processes having the following characteristics:
- **Resource Ownership:** Owns a process image which has PCB, stack etc 
- **Scheduling:** Process has an execution status (ready, running etc) and maybe interleaved with other processes 
To distinguish processes vs threads, we can have the following definition: 
- **Process/Task:** Unit of resource ownership that schedules things to run 
- **Thread:** Unit of dispatching that actually does the work 

In a  [[Multithreading]] environment, we have the following definitions 
#### Processes:
- Unit of resource allocation and ownership 
- Virtual address space that holds the process image 
- Protected access to processors, other processes (for inter process communication), files, and I/O resources (devices and channels)
#### Threads:
Within a process, there may be one or more threads, each with the following: 
- Thread execution state -> Running, Ready, etc 
- Saved thread context when dormant
- Execution stack 
- Static storage for local variables 
- Access to memory and resource of its processes, shared with all other threads in that process

![[Pasted image 20240210163951.png]]
