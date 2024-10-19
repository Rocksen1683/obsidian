This is what happens when an interrupt gets triggered 
1. Device issues an *interrupt signal* to the processor 
2. Processor finishes execution of current instruction then responds to interrupt 
3. Processor checks for interrupt signal, acknowledges it. Device removes signal post acknowledgement
4. Program stores information required to resume post interrupt on the *control stack*. This is called the *Program Status Word (PSW)*. The address to the next instruction can be found in the *PC*
5. Processor chooses an *interrupt handling* routine and loads it onto the *IR*
6. Interrupt Handler also saves the state of all of the registers in the original program before continuing 
7. Interrupt Handler starts it's instruction cycle where it *fetches* and *executes* the interrupt code
8. After execution of interrupt, saved register values are retrieved from stack and restored 
9. *PSW* and *PC* values are restored which resumes the execution of the program 