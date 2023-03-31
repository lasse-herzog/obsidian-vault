In a single processor system all processes have to run sequentialy. If a process has to wait for some I/O operation computation time is wasted. Multitasking optimizes this process by keeping multiple processes in memory and assigning the CPU to another process during an I/O operation.

### Scheduling Queues
When processes enter the system they are put into a **job queue**. Processes that are waiting to be executed  are stored in RAM inside a **ready queue**.  In case a process needs to access a device it enters the **device queue** for that particular device.

### Schedulers
Every scheduling queue needs a **Scheduler** which selects a process from the queue. In batch systems processes are kept on a  mass storage device until the **long-term scheduler/job scheduler** selects processes from this pool and loads them into memory. A **short-term scheduler/CPU scheduler** selects one of the ready processes and allocates the CPU to the selcted process.

The short-term scheduler must operate much more frequently than the long-term scheduler and must therefore be much faster. The long-term scheduler often only needs to operate when processes are terminated and a new process can be loaded.

A long-term scheduler should select a good *mix* of *I/O bound* and *CPU bound* processes to balance the utilization of the ready and the I/O Queue. This results in maximal performance. 

Some OS also have an additional *medium-term scheduler* for *swapping* processes in and out of memory.

