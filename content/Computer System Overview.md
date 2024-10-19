### What does an OS do? 
An OS exploits the hardware resources of one or more processors to provide services to users. It also manages memory and I/O devices on behalf of the user. 

## Basic Elements of a Computer 
### Processor 
Controls operation of the computer and performs its data processing functions. The main processor is referred to as **CPU**. 
### Main Memory 
Stores data and programs and is mostly *volatile* (lose contents and memory when shut down). Disk memory is retained even when system is shut down 
### I/O Modules 
Moves data between computer and external devices 
### System Bus
Provides communication between processor, I/O modules, and memory. 

![[Pasted image 20240128145558.png]]

### Memory and I/O Registers 
- **Memory Address Register (MAR):** Specifies the address in memory for the next read/write operation 
- **Memory Buffer Register (MBR):** Holds content of things to be written into memory or things acquired from memory (interaction b/w processor and memory)
- **I/O Address Register (I/O AR):** Same as **MAR** but specifies address in a particular I/O device 
- **I/O Buffer Register (I/O BR):** Same as **MBR** but holds content for interaction b/w processor and I/O device 
## Evolution of the Microprocessor 
Microprocessors started out with single cores and were very slow. Now they are super-fast due to improvements in the physics of how they're built. They are now **multiprocessors** with multiple chips (called *socket*) and multiple processors (called *cores*).
### Some Terminology 
- **GPU (Graphical Processing Units)** - mainly for rendering games and graphics but now used for numerical computation too 
- **SIMD (Single Instruction Multiple Data)** - techniques used by the **GPU** to provide efficient computation on arrays of data 
- **DSP (Digital Signal Processors)** - used in devices for handling streaming signals like audio and video 
- **SoC (System on a Chip)** - modern microprocessor with **CPU**, **DSP**, **GPU**, **I/O**, main memory all together. Mainly used by handheld devices 

## [[Instruction Execution]]

## [[Interrupts]]

## [[Memory Hierarchy in an OS]]

## [[Input & Output Operations]]