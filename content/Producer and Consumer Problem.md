### Input 
- Buffer of $n$ slots, each capable of storing one unit of data
- Two processes running, *Producer* and *Consumer*
![[Pasted image 20240411145240.png]]

- Producer *inserts* data into an empty and Consumer *removes* data from a filled slot
- Producer and Consumer *should not* insert and remove data simultaneously 
### Solution using [[Semaphores]]
- $n$ : a [[Counting Semaphore]] which is the number of items in the buffer 
- $s$: a [[Binary Semaphore]] 
- $delay$: a [[Binary Semaphore]]
#### Producer Implementation 
``` c
void producer(){
	while(true){
		 //
		 produce()
		 semWaitB(s)
		 append()
		 n++
		 if (n==1){
		 semSignalB(delay)
		 }
		 semSignalB(s)
	}
}
```

#### Consumer Implementation 
``` c
void producer(){
	int m; //local variable 
	semWaitB(delay);
	while(true){
		 //
		 semWaitB(s)
		 take()
		 n--
		 m - n;
		 semSignalB(s)
		 consume();
		 if (m==0){
		 semWaitB(delay)
		 }
	}
}
```