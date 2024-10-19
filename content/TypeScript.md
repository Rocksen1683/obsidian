## JS Concepts 
### Truthy and Falsy 
![[Pasted image 20240227225147.png]]
0 in general is **falsy**
### Logical Or
``||`` is logical OR 
- usually used to assign default val is var is undefined 
``` JavaScript 
let v; 
v = v || 456; //v is 456 

let v = 0; 
v = v || 456; //v is 456 since 0 is falsy 
```

### Nullish Coalescing 
`??` is the *nullish coalescing* operator. Only **false** when null or undefined
``` JavaScript 
let v = 0; 
v = v ?? 456; //v is 0 because not undefined or null
```

