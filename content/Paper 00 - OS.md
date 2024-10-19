#### Question 2
1) Routine 1m -> good as it's reliable 

#### Question 3 
Refer to 7 State Process Diagram in [[Processes]]

#### Question 4 
- *User Level Threads:* these are threads that are controlled by an *application* which is programmed by users of the operating system. The kernel doesn't know about these threads and treat the application as a process
- *Kernel Level Threads*: These are threads that are controlled by the kernel and it has knowledge of each dispatchable unit of work. 
- *Advantages of User level:* 
	1) as they are programmed within an application, the processor doesn't need to do any thread management as that would be the responsibility of the application. 
	2) As they are within the application, you don't have to switch between kernel mode and user mode 

#### Question 5 
occurs when multiple processes or threads read and write data at the same time 
``` c
int a = 0

void proc1(){
	a = 2
}

void proc2(){
	a = 3
}
```

#### Question 6 
```
C = exec time 
T = period

ProcA: 
C = 6 
T = 11

ProcB: 
C = 4
T = 15

ProcC:
C = 7 
T = 20 
```
#### Question 7 
A *buffer overflow attack* is when you pass in too much data to the buffer 
#### Question 11 
If there are tasks 
