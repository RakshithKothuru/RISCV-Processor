# 5-Stage Pipelined RISC-V Processor

## 📌 Project Overview

This repository contains the implementation of a 5-stage pipelined RISC-V processor. The design follows the classic five pipeline stages:

Instruction Fetch (IF)
Instruction Decode (ID)
Execute (EX)
Memory Access (MEM)
Write Back (WB)

## 📌 Technologies Used
✅ Designed using **Verilog HDL**  
✅ Simulated using **Icarus Verilog (iverilog) & GTKWave**  
✅ Developed in **VS Code** 

## 📌 Supported Instruction Types

✅ R-Type Instructions

✅ I-Type Instructions

✅ S-Type Instructions


## 📌 Arithmetic and Logical Operations Supported


✅ Addition (ADD)

✅ Subtraction (SUB)

✅ Bitwise AND (AND)

✅ Bitwise OR (OR)

✅ Set Less Than (SLT)

## Pipeline Stages
 
1. Instruction Fetch (IF)
Fetches instructions from memory using the Program Counter (PC).
The PC increments sequentially as there is no branch/jump handling.

2. Instruction Decode (ID)
Decodes the fetched instruction.
Reads source registers and generates control signals.

3. Execute (EX)
Performs ALU computations for arithmetic, logical, and memory address calculations.
Handles forwarding to resolve data hazards.

4. Memory Access (MEM)
Handles load and store operations.
Uses a simple synchronous memory interface.

5. Write Back (WB)
Writes results back to the register file if needed.

## Hazard Handling

Data Hazards: Managed through data forwarding from EX/MEM and MEM/WB stages.

Control Hazards: Since there is no branch prediction, control hazards are handled by stalling or flushing the pipeline.

## Future Enhancements

Implement branch prediction to reduce control hazards.

Add jump instructions (JAL, JALR) support.

Extend to support more RISC-V instructions.





