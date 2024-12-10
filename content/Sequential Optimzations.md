Most programs are sequential; even concurrent programs are
- (large) sections of sequential code per thread connected by
- small sections of concurrent code where threads interact (protected by synchronization and [[Mutual Exclusion]] (SME))

## Data Dependency 

![[Pasted image 20241202171324.png]]
where $R \implies$ *read* operations and $W \implies$ *write* operations

## Control Dependency
