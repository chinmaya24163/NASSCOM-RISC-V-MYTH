# 64-RV_D5SK3_L5_Lab_To_Add_Control_Logic_For_Jump_Instructions

## Overview

This lab adds support for jump instructions to the RISC-V CPU.

The lecture focuses on:

- JAL implementation
- JALR implementation
- unconditional control flow
- jump target computation
- PC redirection
- jump shadow cycles
- control hazard handling
- JALR target address generation

Jumps are effectively unconditional branches.  
This lab extends the existing branch-control infrastructure to support jump-based control flow.

---

# Major Code Additions

## Added JALR Decode

A new decode signal was introduced:

```tlv
$is_jalr = $dec_bits ==? 11'bx_000_1100111;
```
JAL already existed through:
```text
$is_j_instr
```

## Added JALR Target Address Logic

A new target PC calculation was added:
```tv
$jalr_tgt_pc[31:0] = $src1_value + $imm;
```
Unlike branches and JAL:
```text
Target = PC + Immediate
```
JALR computes:
```text
Target = RS1 + Immediate
```
The computation is performed after bypass logic using $src1_value.

## Extended Pipeline Valid Logic

Jump shadow cycles were added:
```tlv
$valid =
   (!(>>1$taken_br)) &&
   (!(>>2$taken_br)) &&
   (!(>>1$is_load)) &&
   (!(>>2$is_load)) &&
   (!(>>1$is_jalr)) &&
   (!(>>2$is_jalr));
```
This injects invalid pipeline slots after jumps. 

## Extended Taken Branch Logic For JAL

JAL was merged into branch redirect handling:
```tlv
$taken_br = $is_j_instr ? 1'b1 :
            ...
```
JAL always redirects control flow unconditionally. This allows JAL to reuse:

- branch target logic
- branch flush logic
- PC redirect logic

## Added JALR PC Redirect Path

The PC update mux was extended:
```tlv
$pc[31:0] =
   (>>1$reset) ? 32'd0 :
   (>>3$is_jalr) ? >>3$jalr_tgt_pc :
   (>>3$taken_br) ? >>3$br_tgt_pc :
   ...
```
JALR uses its own redirect path because its target is register-relative.

---

# Hardware Perspective

Jump instructions modify control flow without requiring condition evaluation.
```text
JAL:
PC ← PC + Immediate
JALR:
PC ← RS1 + Immediate
```
Both introduce control hazards and therefore require pipeline invalidation.

---

![TLV](images/lec64/tlv1.png)

![TLV](images/lec64/tlv2.png)

![TLV](images/lec64/tlv3.png)

![TLV](images/lec64/tlv4.png)

![Block Diagram](images/lec64/BlockDiagram.png)

[Click Here To Open the implementation in Makerchip](https://makerchip.com/v132/ide/~0ADf9hjY/p-0Y6hDy)

---

# Key Learning Outcomes

After this lab, the learner understands:

- unconditional jumps
- JAL operation
- JALR operation
- register-relative control flow
- PC redirection
- control hazard handling
- jump shadow cycles
- jump target computation

This lab completes support for jump instructions in the custom RV32I CPU.
