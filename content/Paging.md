We know that [[Fixed Partitioning]] creates a lot of *internal fragmentation* and that [[Dynamic Partitioning]] creates a lot of *external fragmentation*. 

To avoid this we can divide our main memory into pretty small  fixed-sized chunks of the same size called *frames*. We could also partition every process into chunks of the same size called *pages*. Now the *pages* would fit perfectly into *frames* with space for some very little *internal fragmentation* on the last page of every process. 

The OS also maintains a **page table** for each process which shows the frame location for each page of the process. The OS also maintains single free-frame list of all the frames in main memory that are currently unoccupied and available for pages.

### [[Page Tables]]

### [[Translation Lookaside Buffer]]

### [[Page Size]]