Instruction execution is a *two-step* process: 
1. **fetch**: processor reads instructions from memory 
2. **execution**: processor executes each instruction 

The processing required for a *single instruction* is called **instruction cycle**.

### Overview of How it works: 
- At the beginning of an instruction cycle, processor *fetches* address of instruction from **PC**
- It then increments the **PC** so that the next instruction can be fetched 
- The fetched instruction is loaded into the *instruction register (IR)* 
- Processor *executes* the instruction in IR
### Types of Execution Instructions 
- **Processor-memory** - data transfer b/w processor and memory or vice versa
- **Processor-I/O** - data transfer b/w processor and I/O or vice versa
- **Data Processing** - perform arithmetic or logic operation 
- **Control** - Controls next instruction to be fetched. 
	- *Example:* Say you fetch instruction $192$ and it tells you to fetch instruction $180$ instead of the next instruction, so processor fetches instruction $180$.

![[Pasted image 20240128154407.png]]

![[Pasted image 20240128154450.png]]

The processor contains a single data register, called the **accumulator (AC)**. Both instructions and data are $16$ bits long, and memory is organized as a sequence of $16$-bit words. The instruction format provides 4 bits for the opcode, allowing as many as $2^{4}= 16$ different opcodes (represented by a single hexadecimal $1$ digit). The opcode defines the operation the processor is to perform. With the remaining $12$ bits of the instruction format, up to $2^{12}= 4096$ (4K) words of memory (denoted by three hexadecimal digits) can be directly addressed.