The *fetch policy* determines when a page should be brought into main memory. 

### Demand Paging 
Page brought into main memory only when a reference is made to a location on that page . 

When a process starts in *demand paging*, it will have a lot of page faults (refer diagram in [[Translation Lookaside Buffer]]) because the pages demanded aren't in main memory yet but this will reduce as we go deeper and deeper. 

### Pre Paging
Along with the page that is demanded, we fetch pages that are contiguously close to it, avoiding more frequent *page faults*

