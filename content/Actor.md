*Actor* is a unit of work *without* a [[Threads]]. 
![[Pasted image 20241001133959.png]]

![[Pasted image 20241001134413.png]]
![[Pasted image 20241001134425.png]]

As we don't know how many threads we're creating, this would be a form of *implicit* [[Concurrency]]

Implements [[Thread Communication]] through a *polymorphic queue* of messages.  Messages are received in FIFO order from mailbox and executed sequentially. 

- Send messages with operator $|$
- Receive *derived message* through `msg_d`
- Start actor with `uActor::start()`
- (StartMsg) uActor::startMsg / (StopMsg) uActor::stopMsg persistent predefined messages
- Stop actor with `uActor::stop()`

Usually Actor systems use some sort of [[Garbage Collection]] but as `C++` does not have anything like that, actors use explicit storage-management and return some sort of *allocation status* for each message. 

`enum Allocation {Nodelete, Delete, Destroy, Finished}`

- `Nodelete` $\implies$ Is the *default* type. It's for when actor or message persists after an actor returns from receive. Use for multi-use actors or messages during their life time
- `Delete` $\implies$ Actor or message is deleted after an actor returns from receive. Use with dynamically allocated actors or messages at completion
- `Destroy` $\implies$ actor’s or message’s destructor is called after an actor returns from receive but storage is not deallocated
- `Finished` $\implies$ actor is marked finished after it returns from receive but neither the destructor is called nor storage deallocated.

### [[Sum Rows of Matrix with Actors]]