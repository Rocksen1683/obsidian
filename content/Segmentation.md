Same as [[Paging]] but instead of *fixed-partitions*, we do *variable-partitions*. This eliminates *internal fragmentation* but has *external fragmentation* like [[Dynamic Partitioning]]. 

We use a **segment table** to keep track of which segment of the process is mapped to which frame. 

An issue with segmentation is that there is no direct relationship between logical addresses and physical addresses. 

### [[Segment Table]]