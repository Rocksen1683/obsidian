- most common way of organizing files 
- fixed format used for records 
- all records of same length, and have same number of fields 
- *Key Field :* First field of a record used to uniquely identify it 
- Only structure to be easily stored on tape as well as disk 
- Physical organization of file on tape or disk directly matches the local organization
#### Issues 
 -  Access requires *sequential search* of the file for a key match 
 - Pretty big processing delay in accessing a record in a large sequential file
 - Additions also present problems 

#### Overcoming Issues 
- Organize a sequential file physically as a linked list