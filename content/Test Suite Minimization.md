Reduce the number of tests to get an adequate amount of coverage and tests while minimizing the number of tests executed. 

*Essential Test Case:* If a test requirement $r_{i}$ is only satisfied by a particular test case $t_{j}$ then it is an essential test case

#### GE Heuristic 
- Start with all *essential* test cases 
- Using [[Greedy Algorithms]], select the the test case that satisfies the maximum number of unsatisfied test requirements 
#### GRE Heuristic 
- Remove all redundant test cases which might lead to additional essential test cases
- Run *GE Heuristic* on the new input set 

