Single or multi-level page tables work by mapping the page location to frame location. An issue with page tables is that the space required by them is proportional. 
![[Pasted image 20240311132141.png]]
## Inverted Page Table 
Page number portion mapped into a hash value using a simple hashing function. 

- Hash value is to a pointer to the inverted page table which contains the page table entries 
There is one entry in the inverted page table for each real memory page frame rather than one per virtual page. Thus, a fixed proportion of real memory is required for the tables regardless of the number of processes or virtual pages supported

The page table’s structure is called *inverted* because it indexes page table entries by frame number rather than by virtual page number.

![[Pasted image 20240311004509.png]]
