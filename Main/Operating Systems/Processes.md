A **Process** is the instance of a program being executed by one or many [[threads]]. It is the unit of work in a modern time-sharing system. An OS must not only execute user programs but also fulfill various other tasks. Processes can therefore be seperated in *system processes* and *user processes*. Most operating systems use a **process identifier (pid)** to identify processes. As a process executes it changes [[Process State|state]]. Processes are represented by datastructures called [[Process Control Block|process control block (PCB)]]. The task of selecting the next process is called [[Process Scheduling]]. A process might be interrupted in which case its current **context** needs to be saved. This task is known as [[Context Switch]].

### Process Creation
A Process may create several **child processes** during its execution. The creator of a child process is called **parent process**. When a child process is created it might get its ressources directly from the OS or it get a subset of the parent processes ressources.  A parent process may also pass some parameters to the subprocess.

When a child process is created there are 2 possibilities:
1. The parent process continues to execute with its children
2. The parent process waits until all its child process have terminated

There are also two address-space possibilities for the new process:
1.  The child process is a duplicate of the parent process (it has the same program and data as the parent)
2.  The child process has a new program loaded into it

