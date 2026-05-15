# 12-registers_And_Their_Respective_ABI_Names

## Overview

This lecture concludes the discussion on:
- load/store instructions
- instruction formats
- register encoding
- ABI register naming

The lecture explains:
- RISC-V base integer instructions
- instruction classification
- R-type, I-type and S-type instructions
- why RISC-V has only 32 registers
- 5-bit register encoding
- ABI names of registers
- purpose of different registers

This lecture forms the bridge between:
- ISA instructions
- register architecture
- ABI conventions
- function call mechanisms

---

# Base Integer Instructions

The lecture begins by explaining:

```text id="jlwm122"
These instructions operate on integers.
```

The integers may be:

- signed integers
- unsigned integers

These instructions are called Base Integer Instructions.

---

# RV64I Instruction Set

The lecture specifically mentions RV64I instruction set.

The instructor explains that any CPU core implementing RV64I must implement at least the 47 base integer instructions.

The previously discussed instructions:

- ld
- add
- sd

are part of RV64I base integer instruction set.

## Instruction Classification

The lecture explains that instructions are further classified based on:

- operands used
- immediate values
- instruction bit layout

The classifications introduced are:

- R-type
- I-type
- S-type

## R-Type Instructions

Example instruction:
```text
add x8, x24, x8
```
The lecture explains that instructions operating only on registers are called R-type instructions.

Characteristics:

- operates only on registers
- contains rs1, rs2 and rd

## I-Type Instructions

Example instruction:
```text
ld x8, 16(x23)
```
The lecture explains that instructions operating on registers and an immediate are called I-type instructions. I-type comes from the word "Immediate".

Characteristics:

- one immediate value
- source register
- destination register

## S-Type Instructions

Example instruction:
```text
sd x8, 8(x23)
```
The lecture explains that instructions used for storing data are called S-type instructions.

Characteristics:

- source registers
- immediate value
- memory storage operation

![Registers](images/lec12/registers.png)

## Instruction Encoding Classification

The lecture emphasizes that instruction classification depends on:

- location of bits
- arrangement of fields
- opcode structure

The instructor also mentions that there are further instruction classifications which will be discussed later.

## Register Encoding

All register fields are 5 bits wide.

Examples:
```text
rs1
rs2
rd
```
all use 5-bit encoding.

## Why RISC-V Has 32 Registers

The instructor derives:
| Bits   | Possible Values |
| ------ | --------------- |
| 2 bits | 2² = 4          |
| 3 bits | 2³ = 8          |
| 4 bits | 2⁴ = 16         |
| 5 bits | 2⁵ = 32         |

Therefore 5-bit register encoding allows 32 registers. 
Hence RISC-V contains:
```text
X0 → X31
```

## Register Naming Convention

The lecture explains that RISC-V register names go from X0 to X31.
Which corresponds to:
```text
0 → 31
```

---

# ABI 

## ABI Register Names

The lecture introduces ABI names.

The ABI provides:

- specific names
- programmer-friendly access

to internal CPU registers.

The instructor explains that ABI accesses the internals of the RISC-V CPU core through these names.

| Register | ABI Name | Meaning        |
| -------- | -------- | -------------- |
| X0       | zero     | Hardwired zero |
| X1       | ra       | Return address |
| X2       | sp       | Stack pointer  |
| X3       | gp       | Global pointer |
| X4       | tp       | Thread pointer |

### Temporary Registers

The lecture explains that X5 to X7 are temporary registers.

Used for:

- temporary storage
- intermediate calculations

The instructor mentions these are related to stack concepts discussed later.

### Saved Registers

The lecture introduces X8 and X9 are saved registers. Also frame pointer concepts are introduced.

Further saved registers:
```text
X18 to X27 are saved registers.
```

### Argument Registers

The lecture explains that X10 to X17 are argument registers, used for passing arguments.

The instructor specifically mentions that function arguments will be discussed later.

### Temporary Registers Again

The lecture also mentions X28 to X31 are temporary registers.

![ABI](images/lec12/ABI.png)

## ABI Access Mechanism

The lecture explains that programmers access the RISC-V CPU core through ABI names.

Example names mentioned:
```text
a0
sp
ra
```

These names appear in:

- assembly programs
- sample codes
- system calls

---

# Hardware Perspective

The lecture directly connects:

- register encoding
- instruction formats
- ABI conventions

with actual processor hardware implementation.

The processor internally:

- decodes 5-bit register fields
- accesses register file
- executes instruction formats
- follows ABI conventions during program execution

---

# Key Learning Outcome

After this lecture, the learner understands:

- RV64I base integer instructions
- R/I/S instruction types
- why RISC-V has 32 registers
- 5-bit register encoding
- ABI register naming conventions
- purpose of different registers

---

# Notes

This lecture introduces the ABI naming conventions and explains the architectural reason behind the existence of exactly 32 integer registers in RISC-V architecture.