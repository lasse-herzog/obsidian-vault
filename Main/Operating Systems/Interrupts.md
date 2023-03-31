Interrupts are a way for OS to react to the environment. An interrupt may cause a transition from user to kernel mode. If an interrupt occurs the OS performs the following steps:
1. save the state of the current process
2. transfer control to an interrupt service routine (ISR)
3. restore the state of the process after the interrupt is serviced
