I'm manually typing out a somewhat paraphrase somewhat word for word of google AI overview
it is useful to just type out something to get a feel for the vocabulary
without feeling overly stressed about the details.
You're goal is to just represent the information well and try to mentally group things
together in a way that makes sense to you, and you're typing the vocabulary so it starts sticking in your mind.

---

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

---

... continued prompting with "where does the GPU come into play?"

GPU complements Von Neumann architecture by acting as a highly specialized, parallel accelerator alongside the main CPU.

While a standard CPU follows the Von Neumann model by executing complex instructions sequentially, the GPU is designed to process massive amounts of simple, repetitive data all at once.

The GPU does not replace the Central Processing Unit. It lives outside the main CPU and connects to it through a very fast communication pathway such as a PCI Express (PCIe) slot.

Dedicated GPU Memory. Modern discrete GPUs feature their own separate, ultra-fast memory pool (VRAM). This setup functions similarly to a Harvard-style approach for specific tasks, bypassing the main system's Von Neumann bottleneck. The CPU sends data across the PCIe bus to the VRAM, allowing the GPU to process it without slowing down the main system memory.

Shared Memory (Unified Architecture) in smartphones and integrated laptop chips (like Apple's M-series), the CPU and GPU share the exact same physical memory pool. This brings the GPU directly into the core Von Neumann memory space, eliminating the slow transfer step across a PCIe bus.

How the GPU Differs from the CPU:
- CPU (Von Neumann Core): Optimized for low-latency, sequential processing. It features a few powerful processor cores designed to handle complex, unpredictable logic tracks one step after another.
- GPU (Massive Parallelism): Optimized for high-throughput, parallel processing. It features thousands of smaller, simpler cores designed to execute the exact same mathematical instruction simultaneously across a massive grid of data.

Primary Use Cases:
- Graphics Rendering: calculating the color, shading, and position of millions of pixels on a screen simultaneously.
- Artificial Intelligence: Executing the massive matrix multiplications required to train and run deep learning models.
- Scientific Simulations: processing complex mathematical models, such as weather forecasting or molecular dynamics, where calculations can be split into thousands of independent parts.

---

... continued prompting with "What is the lowest level way of interacting with the GPU"

The lowest-level way of interacting with a GPU is through Driver-Level APIs and writing Machine Code (Assembly) that executes directly on the GPU's execution units.

Because GPUs are treated as hardware peripherals, developers cannot write directly to the hardware registers without operating system permissions. Instead, they use a structured stack to get as close to the silicon as possible.

Driver-Level APIs (The Entry Point):
To bypass the overhead of heavy software frameworks, developers use low-overhead, "close-to-the-metal" Application Programming Interfaces (APIs). These APIs give direct control over memory allocation, thread scheduling, and hardware synchronization.
- Vulkan (Cross-Platform): The lowest-level open-standard API for graphics and compute. It removes the driver abstractions found in older APIs like OpenGL, forcing the developer to manually manage memory layout and command queues.
- DirectX 12 Agility / Direct3D 12 (Windows): Microsoft's low-level API that grants console-like, explicit control over the GPU.








