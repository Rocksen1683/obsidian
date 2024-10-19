- Save complete *current* document state $S$ 
- Save *reverse change records* to return to previous state $\{c^{-1}, b^{-1}, a^{-1}\}$
- To undo last action, apply last *reverse change record* $S = undo(S) = c^{-1}(S)$


It uses the *Command Pattern*
- Execute user *command* to create new document state 
- Push *reverse command* onto undo stack 
- Clear redo stack 

Another option to implement this would be to use the *Memento Pattern*
- Save snapshots of each document state 
- Could be complete state or *difference* from last state