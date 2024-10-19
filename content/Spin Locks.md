A *spin lock* is implemented using *busy waiting*, WHICH LOOPS CHECKING FOR AN EVENT TO occur. 


When a task is busy waiting, it loops till:
- [[Critical Section]] becomes unlocked or an event happens 
- Waiting task is preempted and put back into ready queue

### Adaptive Spin Lock
Some spin-locks allow adjustment of spin duration, called *adaptive spin-lock*.


### Non-Yielding Spin Lock 
```
class uSpinLock { 
	public: 
		uSpinLock(); // open void
		acquire(); bool tryacquire(); 
		void release(); 
};
```


### Yielding Spin Lock 
```
class uLock { 
	public: uLock( 
		unsigned int value = 1 ); 
		void acquire(); 
		bool tryacquire(); 
		void release(); 
	};
```

- Lock starts closed (0) or opened (1); waiting tasks compete to acquire lock after release.
- `tryacquire` makes one attempt to acquire the lock, i.e., it does not wait.

### Synchronization
![[Pasted image 20241017190239.png]]

### Mutual Exclusion
![[Pasted image 20241017190312.png]]
