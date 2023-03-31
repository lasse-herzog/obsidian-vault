There are multiple forms of operands:
- *Constant* values are preceeded by the # sign, e.g. #0x2.
- *Register* forms refer to individual registers, e.g. X0.
- *Memory*  corresponds to some value stored in main memory. The different adressing modes are listed below where base is either a general-purpose register X0-X30 or the current stack pointer, SP.
### Adressing Modes
|Mode|Immediate Offset|Register Offset|Extended Register Offset|
|-|-|-|-|
|Base register only|[base{, #0}]|-|-|
|Base + offset|[base{, #imm}]|[base, Xm{, LSL #imm}]|[base, Wm, (S\|U)XT(X\|W) {#imm}]|
|Pre-indexed|[base, #imm]!|-|-|
|Post-Indexed|[base], #imm||-|
|Literal|label|-|-|

#### Register Offset
A register offset means that the offset is the 64 bits from a general-purpose register, Xm, optionally scaled by the transfer size, in bytes, if LSL #imm is present and where imm must be equal to log2(transfer_size). The SXTX extend/shift option is functionally equivalent to LSL, but the LSL option is preferred in source code. 

#### Extended Register Offset
An extended register offset means that offset is the bottom 32 bits from a general-purpose register Wm, sign-extended or zero-extended to 64 bits, and then scaled by the transfer size if so indicated by #imm, where imm must be equal to log2(transfer_size). An assembler must accept Wm or Xm as an extended register offset, but Wm is preferred for disassembly.