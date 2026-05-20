# 35-V_Labs_Part-1

## Overview

This lecture introduces:
- the RISC-V CPU shell
- MakerChip development infrastructure
- workshop starter code
- RISC-V assembler support
- CPU visualization tools
- instruction memory initialization
- register file infrastructure
- data memory infrastructure
- reference solutions
- visualization-assisted debugging

The lecture marks the beginning of hands-on RISC-V CPU implementation. The learner is now provided a partially completed CPU framework inside MakerChip.

---

# Shell Infrastructure

The shell already contains:

- predefined infrastructure
- helper macros
- visualization support
- memories
- assembler support

---

# TL-Verilog M4 Infrastructure

Certain advanced functionalities are unlocked through a macro preprocessor called M4.

---

# RISC-V Assembler

The assembler converts assembly instructions into instruction memory contents. The shell already contains preloaded assembly test program for summing up numbers from 1 to 9.

---

# Components Provided by Shell

The shell already provides:
| Component          | Purpose           |
| ------------------ | ----------------- |
| Instruction Memory | Stores program    |
| Register File      | CPU registers     |
| Data Memory        | Load/store memory |

The instruction memory already contains assembled test program.

## Register File Support

The provided register file supports:

- reads
- writes

for CPU datapath operations.

## ata Memory

The shell also provides data memory for future load/store instructions.

---

# Hardware Perspective

Modern hardware development relies heavily on:

- reusable shells
- libraries
- generators
- visualization systems
- debugging infrastructure

---

# Key Learning Outcome

After this lecture, the learner understands:

- RISC-V shell infrastructure
- provided CPU memories
- assembler integration
- CPU shell organization
- instruction memory initialization
- MakerChip CPU debugging tools

---

# Notes

The learner now works inside a reusable CPU shell containing:

- memories
- assembler support
- visualization
- debug infrastructure
- testing environment