# 60-RV_D5SK3_L1_Introduction_To_Load_Store_Instructions_And_Lab_To_Redirect_Loads

## Overview

This lecture introduces support for load instructions and the associated pipeline hazards caused by memory access latency. The lecture focuses on:

- load/store instructions
- data memory integration
- memory address generation
- load-use hazards
- load shadow handling
- PC redirection after loads
- pipeline invalidation
- load replay behavior
- load latency management

Unlike ALU operations, load instructions cannot produce data immediately. Memory requires additional cycles before returning valid load data. Because of this, the instructions immediately following a load may execute too early and observe incorrect data. To solve this, the CPU introduces a load shadow, similar to the earlier branch shadow mechanism.

---

# Address Generation

Load/store addresses are computed using:
```text
Address = rs1 + immediate
```
This is identical to the ADDI computation already implemented earlier. The address generation uses:

- source register 1 as base pointer
- immediate as offset

---

# Load Latency Problem

Unlike ALU instructions, memory does not immediately return data. The load data becomes available only after multiple cycles. This creates a new pipeline hazard:
```text
Load →
Instruction 1 →
Instruction 2
```
The instructions following load may attempt to use data before it has actually been written into the register file.

---

# Load Shadow

To solve this, the CPU introduces a load shadow. The two instructions immediately after the load are invalidated. This creates empty slots that allow:

- memory data to return
- register file write to complete
- bypass paths to receive updated data

This mechanism is conceptually similar to the earlier branch shadow.

---

# PC Redirection For Loads

After detecting a load:

- the PC is redirected
- the next correct instruction is replayed
- invalid shadow instructions are squashed

The redirected PC becomes:
```text
PC(load) + 4
```
which is the next sequential instruction after the load.

---

# Hardware Perspective

Pipeline control logic becomes necessary to:

- stall/replay instructions
- preserve correctness
- synchronize memory timing with execution timing

---

# Key Learning Outcome

After this lecture, the learner understands:

- load/store instruction behavior
- memory address computation
- load latency
- load shadows
- replay-based hazard handling
- PC redirection for loads
- pipeline invalidation for memory hazards

We extend the CPU from a purely computational pipeline into a memory-access capable processor.

---

# Notes

Actual load data handling is not yet implemented in this lecture. This lecture only introduces:

- load shadow creation
- PC replay logic
- invalid instruction injection