A thread is an independent sequence of execution within the code of one process and may be viewed as a subprocess.
### Kernel threads
A kernel thread is a lightweight unit of kernel scheduling. A process may contain multiple kernel threads which share the same memory and file ressources. The kernel can assign exactly one kernel thread to each logical core in the system. Swaping kernel threads is much more expensive than swaping user threads.
### User threads
User threads are managed and scheduled in [[userspace]] and therefore independent from the kernel. Those threads get mapped to several kernel threads. Context switching between user threads is very easy.