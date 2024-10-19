Uses a *power schedule* which chooses which seeds to pick for fuzzing 

- Maximize the time spent fuzzing seeds which lead to higher coverage in shorter time 

### Directed Greybox Fuzzing 
- We assume that we know a spot in the code that is more dangerous and we can change the *power schedule* to find more seeds within that part 
- 