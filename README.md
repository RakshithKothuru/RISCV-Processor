# 🚀 5-Stage Pipelined RISC-V Processor

## 📌 Project Overview

This repository contains the RTL design and simulation of a 5-stage pipelined 32-bit RISC-V processor. The processor supports a subset of the RV32I instruction set and follows the classic pipeline architecture with the following stages:

- **Instruction Fetch (IF)**
- **Instruction Decode (ID)**
- **Execute (EX)**
- **Memory Access (MEM)**
- **Write Back (WB)**

The design includes basic hazard handling through data forwarding, enabling improved performance by avoiding unnecessary stalls.

---

## 🛠️ Technologies Used

- ✅ Verilog HDL
- ✅ Icarus Verilog (for simulation)
- ✅ GTKWave (for waveform visualization)
- ✅ VS Code (for development)

---

## 🧮 Supported Instruction Types

- ✅ **R-Type** 
- ✅ **I-Type** 
- ✅ **S-Type**

---

## 🧠 Arithmetic and Logical Operations Supported

- ✅ **Addition** (`ADD`)
- ✅ **Subtraction** (`SUB`)
- ✅ **Bitwise AND** (`AND`)
- ✅ **Bitwise OR** (`OR`)
- ✅ **Set Less Than** (`SLT`)

---

## 📦 Pipeline Stage Details

### 🟦 Instruction Fetch (IF)
- Fetches instructions from memory using the Program Counter (PC).
- PC increments sequentially (no control flow instructions yet).

### 🟩 Instruction Decode (ID)
- Decodes instruction opcode and fields.
- Reads operands from the register file.
- Generates control signals for later stages.

### 🟨 Execute (EX)
- ALU performs arithmetic, logical, and address computations.
- Implements **data forwarding** to resolve Read After Write (RAW) hazards.

### 🟧 Memory Access (MEM)
- Performs memory reads and writes (load/store).
- Uses simple synchronous memory interface.

### 🟥 Write Back (WB)
- Writes the result back to the destination register if applicable.

---

## ⚠️ Hazard Handling

- ✅ **Data Hazards**: Handled using forwarding logic from EX/MEM and MEM/WB pipeline stages to eliminate stalls.
- ❌ **Control Hazards**: Not handled in the current version (no branches or jumps yet).

---

## 🚀 Future Enhancements

- ⏩ Add **branch and jump instruction** support (`BEQ`, `JAL`, `JALR`)
- 📈 Implement **branch prediction** to reduce control hazards
- 🔧 Expand support for more **RV32I** instructions

---

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](./LICENSE) file for details.

---

## 🔗 References

- Patterson, D. A., & Hennessy, J. L. (2017). *Computer Organization and Design RISC-V Edition: The Hardware Software Interface*. Morgan Kaufmann.
- [RISC-V ISA Manual (Volume I: User-Level ISA)](https://riscv.org/technical/specifications/)
- [Icarus Verilog](http://iverilog.icarus.com/)
- [GTKWave](http://gtkwave.sourceforge.net/)
- [RISC-V Wikipedia](https://en.wikipedia.org/wiki/RISC-V)
