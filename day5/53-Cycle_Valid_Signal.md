# 53-Cycle_Valid_Signal

## Overview

This lecture introduces the first pipelined implementation strategy for the RISC-V CPU using a three-cycle instruction cadence. The lecture focuses on:

- pipeline retiming
- waterfall-to-logic timing relationships
- negative timing dependencies
- control hazards
- read-after-write hazards
- valid signal generation
- three-cycle instruction spacing
- start pulse generation
- pipeline-valid propagation

The lecture explains:

- why simple stage rebucketing creates invalid timing dependencies
- how hazards appear in both waterfall and logic diagrams
- how spacing instructions apart resolves these timing conflicts

To avoid:

- branch timing hazards
- register read-after-write hazards

the processor temporarily operates one instruction every three cycles. This lecture establishes the first hazard-resolution strategy for the pipelined RISC-V processor.

---

# Pipeline Timing Problem

Simply changing pipeline stages in TL-Verilog
creates impossible timing paths.

---

# Simple Hazard Solution

Instead of advanced forwarding logic, the lecture introduces instruction spacing.

---

# Three-Cycle Cadence

The processor now operates one instruction every three cycles. This spaces instructions apart enough to eliminate backward timing dependencies.

---

# Start Signal

The lecture introduces start signal used to initialize valid pulse generation.

---

# Start Pulse Behavior

Reset was high last cycle but low this cycle. This creates one-cycle pulse after reset deassertion.

---

# Valid Pulse Propagation

We use ahead-by-three pipeline references to propagate valid pulses periodically.

---

# Pipeline Timing Flow

The datapath timing now becomes:
```text
Instruction →
Wait →
Wait →
Next Instruction
```

---

# Valid Signal As Oscillator

The valid pulse effectively behaves like periodic pipeline enable generator.

---

# Pipeline-Controlled Execution

Only cycles with valid = 1 contain meaningful instruction execution.

---

![Valid](images/lec53/Valid.png)

![Clock And Reset](images/lec53/Clk_rst.png)

![Valid And Start](images/lec53/Start_Valid.png)

---

# Hardware Perspective

This lecture introduces one of the simplest forms of hazard mitigation - instruction spacing. Instead of resolving hazards dynamically, the processor avoids hazards temporally.

---

# Key Learning Outcome

After this lecture, the learner understands:

- pipeline retiming hazards
- backward timing dependencies
- control hazards
- RAW hazards
- three-cycle instruction spacing
- valid signal generation
- periodic pipeline enables
- start pulse logic
- pipeline timing stabilization

This lecture establishes the first functional pipelined execution model for the RISC-V CPU.

---

# Notes

This lecture intentionally chooses a simple but inefficient hazard solution to build intuition for:

- pipeline timing
- instruction dependencies
- hazard management

before introducing more advanced techniques later.
