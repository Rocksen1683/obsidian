### Clone Detection 
Defined $4$ types of clones. 
#### Type 1 Clones 
- Code fragments are identical except for variations in white space, layout
#### Type 2 Clones 
- Code fragments are structurally all and syntactically identical except for variations in identifiers, literals, types
- Refactorable Type 2 Clines 
	- Generalize Type 
	- Parameterize Object Creation 
	- Parameterize Number Literal 
#### Type 3 Clones 
- Code fragments are copied with further modifications
- Refactorable by abstracting behavior
#### Type 4 Clones 
Two or more code fragments perform the same computation, but are implemented through different syntactic variants 