#### Prerequisite Knowledge
[[Decision Problem]]

A [[Decision Problem]] $A$ is a polynomial time reducible to a decision problem $B$, if there is a polynomial time algorithm $F$ that transforms any instance $I_A$ of $A$ to an instance $I_B$ of $B$ such that 
$I_A$ is a **YES** instance of $A$ $\iff F(I_{A})= I_B$ is a **YES** instance of $B$

We write $A < _{P} B$ if such a *reduction* exists. 
We write $A = _{P}B$ if $A < _{P}B$ and $B <_{P}A$

#### [[Transitivity of Polynomial Time Reductions]]



