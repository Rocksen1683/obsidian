Changing software system such that it does not *alter* external behavior but still *improves* internal structure 
#### Process
- Identify code smells 
- Determine what refactoring should be applied 
- Guarantee that the applied refactoring preserves behavior 
- Apply the refactoring 
- Assess the effect of the refactoring on design quality 
- Maintain consistency between refactored code and other software artifacts 

- *Floss Refactoring:* frequent refactoring *interleaved* with other kinds of program changes. Do this to maintain *healthy* code.
- *Root Canal Refactoring:* infrequent, protracted periods of refactoring during which programmers perform other kinds of program changes. Do this to correct *unhealthy* code

#### Martin Fowler Refactoring 
If you see the same code structure un more than one place, find a way to unify them 

#### Frank Simon Metrics based Refactoring 
- Uses *Jaccard Distance* to quantify the cohesion between attributes and methods 
$$ $$
$$distance(A,B) = 1 - similarity(A,B)$$

 - Calculated distances are visualized in a three-dimensional perspective using VRML
 - Developer manually identifies refactoring opportunities
#### Radu Marinescu Detection Strategy 
- Detection Strategy: composition of various metric rules combined with AND/OR operators into a single rule 
- Metric rules: metrics that should comply with proper threshold values 

#### Naouoel Moha DECOR
- *DECOR:* method for specification and detection of code and design smells based on DSL 
- *DETEX:* detection technique that instantiates DECOR

#### [[Slicing Based Cohesion]]

#### God Class 
A class having multiple responsibilities and violates the Single Responsibility Principle

[[Duplicate Code]]