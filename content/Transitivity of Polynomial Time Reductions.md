#### Lemma 
If $A<_{P}B$ and $B < _{P}C$ then $A < _{P}C$

#### Proof 
If  $A<_{P}B$, then there exists a algorithm $F$ which maps instances of $A$ to $B$

Similarly, If  $B<_{P}C$, then there exists a algorithm $G$ which maps instances of $B$ to $C$

Now, the composition of the algorithms $F$ and $G$, which is $G \circ F$
will map instances of $A$ to $C$ in polynomial time.
![[Pasted image 20240329141027.png]]

Therefore the algorithm $G \circ F$ will map instances $A$ to $C$ which means that $A <_{P} C$
