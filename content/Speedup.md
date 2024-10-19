Program *speedup* is defined as $S_{C} = \frac{T_{I}}{T_{C}}$ where $C$ is the number of CPUs and $T_{I}$ is the sequential execution.
![[Pasted image 20241001130812.png]]

An algorithm/program is composed of *sequential* and *concurrent* sections.

### [[Amdahl's Law]]

With [[Amdahl's Law]], we can prove that concurrent programming aims to minimize the sequential section of code $(1-P)$.