These are the set of requirements that a [[Memory Management]] system *should have*.
## Relocation 
In order to move to maximize process utilization by providing a large pool of processes to execute, we would often have to *relocate* processes to different areas of memory.
## Protection 
- Programs in other processes should not be able to read or write the address of another process without permission 
- Therefore the memory management should ensure the protection of data and processes 
- Mostly done with hardware 
## Sharing 
- Protection mechanisms should also allow processes to access (*share*) the same portion of main memory 
- Memory management should allow controlled access to shared areas without compromising protection 
## Logical Organization 
An efficient ways to organize data in memory would be to use *modules*. These *modules* would: 
- Contain independent programs that could run 
- Have access features that would define what data they can access 
- Have other *modules* references be compiled at run-time 
- Introduce *sharing* between modules
## Physical Organization 
As discussed in [[Memory Hierarchy in an OS]], we would have *main memory* which is high speed high cost, and *secondary memory* which has low speed low cost. Memory Management should have a system that would handle moving information between these levels.