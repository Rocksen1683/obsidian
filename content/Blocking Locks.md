Blocking locks reduce busy waiting by having releasing task do additional work: cooperation.

Therefore, all blocking locks have 
- state to facilitate lock semantics 
- list of blocked acquirers

## Types of Blocking Locks
- [[Mutex Locks]]
- [[Stream Locks]]
- [[Synchronization Lock]]
- 