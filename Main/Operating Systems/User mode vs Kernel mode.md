User mode and kernel mode are both cpu modes with different hardware access.
- The execution of elevated instructions is illegal in user mode.
- Memory access is restricted in user mode
- Allows for isolation of processes
Switching between user and kernelmode is voluntary. The switch from user to kernel mode is the result of an [[Interrupts]] (e.g. syscall or exception).
