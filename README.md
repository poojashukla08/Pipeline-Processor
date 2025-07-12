# Pipeline-Processor
COMPANY: CODTECH IT SOLUTIONS

NAME:POOJA SHUKLA

INTERN ID: CT06DH677

DOMAIN: VLSI

DURATION: 6 WEEKS

MENTOR: NEELA SANTOSH

4- Stage pipeline processor performing basic operations like add, sub and load

----------------------------------------------------------------------------------------------------
Task: 4-Stage Pipeline Processor Performing Basic Operations Like ADD, SUB, and LOAD

### Overview

This project implements a **4-stage pipelined processor** using **Verilog HDL**, capable of executing fundamental instructions such as `ADD`, `SUB`, and `LOAD`. The processor is designed to simulate instruction-level parallelism through pipelining, improving execution throughput over a non-pipelined design. The design and simulation are implemented and verified using **EDA Playground**, a free online platform for HDL development and waveform visualization.

The processor includes a complete testbench and is organized for simulation, waveform generation, and verification of functional correctness.

---

###  Objectives

The main goal of this task is to develop and verify a basic pipelined processor with a clean architectural pipeline consisting of the following four stages:

1. **Instruction Fetch (IF):** Fetches instructions from instruction memory based on the current program counter (PC).
2. **Instruction Decode/Register Fetch (ID):** Decodes the instruction and reads operands from the register file.
3. **Execute (EX):** Performs arithmetic or memory address calculation operations.
4. **Write Back (WB):** Writes results back to the register file.

This architecture demonstrates how pipeline registers between stages manage data flow and simulate real-world CPU behavior with multiple instructions executing concurrently in different stages.

---

###  Features

* **Instruction Set Architecture (ISA)**:

  * `ADD rd, rs1, rs2`: Performs register-to-register addition.
  * `SUB rd, rs1, rs2`: Performs register-to-register subtraction.
  * `LOAD rd, rs1, imm`: Loads data from memory at `rs1 + imm` into `rd`.

* **16-bit instruction format**:

  ```
  [15:12] Opcode
  [11:8]  Destination Register (rd)
  [7:4]   Source Register 1 (rs1)
  [3:0]   Source Register 2 or Immediate (rs2/imm)
  ```

* **16 general-purpose 16-bit registers**

* **256-word instruction memory and data memory**

* **Simulated pipeline registers for stage transitions**

* **Waveform generation using `$dumpfile` and `$dumpvars` for analysis in EPWave viewer**

---

### Testbench & Simulation (EDA Playground)

The processor is tested using a custom **testbench (`tb_cpu.v`)** written in Verilog and run on **EDA Playground**. The testbench initializes registers and memory with test data and loads a set of instructions into the instruction memory to simulate processor behavior over several clock cycles.

Key test instructions:

* `ADD R1, R2, R3` → Verifies arithmetic addition
* `SUB R4, R1, R2` → Verifies subtraction using result of previous instruction
* `LOAD R5, R6, 4` → Verifies memory access using address computation

Waveforms are automatically generated during simulation using EDA Playground’s **EPWave viewer**, enabling easy observation of signal transitions through the pipeline and validation of data flow between stages.

---

###  Project Structure

```
/PipelinedCPU.v      # Processor Design
/tb_cpu.v            # Testbench
/cpu_wave.vcd        # Waveform dump (generated after simulation)
/README.md           # Documentation and setup guide
```

---

###  Future Enhancements

* Add `STORE`, `JUMP`, and `BRANCH` instructions
* Implement hazard detection and forwarding
* Insert stall control logic for realistic instruction delays
* Add support for signed/unsigned arithmetic

---

### 🛠 Platform Used

All simulation and waveform analysis for this project were done using **[EDA Playground](https://www.edaplayground.com)**, an online platform for HDL simulation and collaborative development.

-----------------------------------------------------------------------------------------------------------------
### OUTPUT
<img width="986" height="811" alt="Image" src="https://github.com/user-attachments/assets/ec615c8f-3e91-42dc-8cdd-13723977fff6" />

### OUTPUT WAVEFORM
<img width="1845" height="391" alt="Image" src="https://github.com/user-attachments/assets/fe7a0203-b18b-49cc-958a-520d162ddfdd" />

