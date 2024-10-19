The *optimal* replacement algorithm replaces the page for which the time to the next reference is the longest. This method cannot actually be implemented as you never know which page will have the longest time till the next call but is usually used as a *benchmark* to test other algorithms. This algorithm also gives us the least amount of *page faults*.

### Example 
![[Pasted image 20240311011018.png]]

where $F$ is a *page fault*.