- structural hazards result in ressource conflicts through simultaneous usage of the same ressources (e.g. memory access)
- data hazards if an instructions depends on the results of another instruction, e.g. read after write 
- control hazards are caused by Jump instructions which result in the pipeline needing to be flushed and refilled again
## Solutions
### Forwarding
A forwarding unit sends the ALU output back to the ALU input for easy access by the next execute. (2 new "flags" forward A and forward B)
### Branch Predictions
#### static
- default predictions 
	- default "branch not taken", bei Sprung vorwärts
	- default "branch taken", bei Sprung rückwärts -> Loop
- delayed branches: Filling the pipeline with jump independent instructions.
#### dynamic
- jump probability prediction (Branch History Table - BHT, Branch Prediction Buffer - BPB)
	- prediction if a jump occurs
- jump target prediction
	- prediction of the jump target
- BPB
	- Small Buffer that gets adressed by the target adress and contains one prediction bit
	- If the prediction was incorrect the prediction bit is inverted
- BTB
	- BTB contains the n last target adresses of jump instructons adressed by their lower adress numbers
	- BTB gets accessed in IF-Phase and returns the last target adress of the jump instruction
	- If the address was incorrect it is deleted

