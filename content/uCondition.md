A *condition* is an external synchronization lock and is a queue of waiting tasks. 

It has the following methods 
- `empty()`: returns *false* if there are tasks blocked on the queue and *true* otherwise
- `front()`: returns an integer value stored with the waiting task at the front of the condition queue
- `wait()`: a task blocks itself using wait
- `signal()`: unblocks the thread at the front of the condition queue after the signaller thread blocks or exits
- `signalBlock()`: unblocks the thread at the front of the condition queue and then *blocks* the signaller thread

NOTE: Signaller does not block, so the signalled task must continue waiting until the signaller exits or waits.

![[Pasted image 20241208121931.png]]
