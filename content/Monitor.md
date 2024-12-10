A *monitor* is an abstract data type that combines shared data with serialization of its modification: 
```
_Monitor name{
	shared data
	members that see and modify the data
}
```


A *mutex member* is one that does not begin execution if there is another active mutex member. In a [[Monitor]], public member routines are implicitly *mutex* and other kinds of members can be made explicitly mutex with `_Mutex`. 

Destructor must be *mutex* so that deleting a dynamically allocated monitor blocks if the thread is still in the monitor. 

### [[Monitor Scheduling]]

An exception raised in a monitor member propagates to the caller's thread. 

### [[Lock Composition Problem]]

### [[Types of Monitors]]