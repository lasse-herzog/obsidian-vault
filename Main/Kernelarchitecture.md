The OS kernel contains basic functionality and directly interfaces with the hardware. The kernel has full hardware access (kernel mode) while funtionality outside the kernel can only utilize virtual memory and itnerface indirectly with hardware (user mode).
### Monolithic Kernel
The whole OS is the kernel. Every routine of the kernel has access to every other routine in the system.
Pros:
- less context switches => better performance
- Stability
Cons:
- failed components can not be restarted and may bring the whole OS down
- high 
### Microkernel
A microkernel only contains the minimal necessary functionality like:
- Memory and task managment
- Synchronisation and inter-task communication
- necessary drivers (for e.g. booting)
Pros:
- Simple replacement of components
- in theory better stability and security than monolithic kernels
Cons:
- less performance because of more context switching
- designing a micro kernel is more complex
### Hybrid kernel
Hybrid kernel are a compromise between monolithic and microkernel. They also run most of the OS components in user mode but the kernel contains performance critical components. 
Pros:
- better performance than microkernel
- better stability than monolithic kernel
