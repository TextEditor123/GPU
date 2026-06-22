I'm looking up "von neumann architecture" and reading through the google ai overview

Von Neumann architecture
- single shared memory stores both program instructions and data

Core Components
4 primary subsystems that communicate through buses

Central Processing Unit (CPU) comprisesd of 3 parts
- Control Unit (CU)
- Arithmetic Logic Unit (ALU)
- Registers

Memory Unit

Input/Output (I/O) Devices

Advantages
- Simplicity and Versatility
- Cost-Effective

The Von Neumann Bottleneck
- Because instructions and data share the same communication pathways (buses) and reside in the same memory, the CPU cannot read an instruction and read/write data at the same time.
- Even though modern processors have vastly outpaced memory in terms of speed, the CPU frequently sits idle, waiting for data to travel back and forth over these shared pathways.

Alternatives:
- Harvard Architecture

Modern Workarounds:
- fast cache and pipelining to load data and instructions before they are actively needed.




