Conditional branches change the flow of execution depending on the current state of the Condition flags or the value in a general-purpose register. [[Condition Codes]]

|Mnemonic|Instruction|Branch offset range from the PC|
|-|-|-|
|B.cond|Branch conditionally|±1MB|
|BC.cond|Branch Consistent conditionally|±1MB|
|CBNZ|Compare and branch if nonzero|±1MB|
|CBZ|Compare and branch if zero|±1MB|
|TBNZ|Test bit and branch if nonzero|±32KB|
|TBZ|Test bit and branch if zero|±32KB|
