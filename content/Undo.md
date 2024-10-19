***Granularity:*** How much should be undone at one time? A *chunk* is a conceptual change from one state to another. Undo reverses one chunk. 

#### Granularity Suggestions 
- Delimit chunks on discrete "input breaks" 
- Chunk all changes resulting from a single interface event 

***Change Record:*** Defines a single transformation to the state of the *model*
## [[Forward Undo]]

## [[Reverse Undo]]

We would implement this with *two stacks* 
- *Undo Stack* - all change records 
- *Redo Stack* - change records that have been *undone*

It's common to have multiple undo-redo stacks 
  