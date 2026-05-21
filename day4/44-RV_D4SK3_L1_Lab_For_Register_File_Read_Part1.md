# 44-RV_D4SK3_L1_Lab_For_Register_File_Read_Part1

## Overview

This lecture implements register file read logic for the RISC-V CPU. The lecture focuses on:

- register file interfaces
- source operand reads
- read enable signals
- source register indices
- dual-port register file reads
- destination register terminology
- register initialization
- operand fetch
- register-based execution

This lecture connects decoded instruction fields to actual operand values. The CPU now begins reading real source operands from architectural registers. 
The CPU now progresses from instruction interpretation to operand retrieval.

---

# Register File

Register file infrastructure already exists inside the provided shell. The register file is available
through a macro instantiation.

## Register File Capabilities

Capable of performing two reads in a cycle and one write.

## Register File Port Structure

The register file contains:
| Port Type   | Count |
| ----------- | ----- |
| Read Ports  | 2     |
| Write Ports | 1     |

## Why Two Reads?

Most RISC-V instructions require two source operands.
Examples:
```text
ADD rs1, rs2
SUB rs1, rs2
BEQ rs1, rs2
```

## Why One Write?

Most instructions produce one destination result.

## Read Enable Signals

The CPU only performs reads when source registers are valid.

## Register File Interface Flow

The datapath now becomes:
```text
Instruction →
Decode →
RS1/RS2 →
Register File →
Source Operand Values
```

## Register Initialization Strategy

The register file initializes:

| Register | Initial Value |
| -------- | ------------- |
| x0       | 0             |
| x1       | 1             |
| x2       | 2             |
| x5       | 5             |

etc.

## Why This Helps Debugging

It makes it easier than debugging all zero values. This makes register reads immediately visible.

---

![RF Read TLV And Block Diagram](images/lec44/RF_Read_TLV_And_Block_Diagram.png)

[Click Here To Open the RF Read implementation in Makerchip](https://makerchip.com/v132/ide/~0ADf9hjY/p-0vghED)

---

# Hardware Perspective

Instructions fundamentally operate on values stored in architectural registers. The register file forms the working state space of the processor.

---

# Key Learning Outcome

After this lecture, the learner understands:

- register file interfaces
- dual-read architectures
- register addressing
- read enable logic
- operand fetch
- architectural state storage
- source operand retrieval
- register-based execution

This lecture establishes operand fetch capability inside the RISC-V processor pipeline.

---

# Notes

This lecture introduces the architectural register file.