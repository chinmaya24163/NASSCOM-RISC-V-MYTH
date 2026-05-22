# 52-RV_D5SK1_L1_Introduction_To_Control_Flow_Hazard_And_Read_After_Write_Hazard

## Overview

This lecture introduces CPU pipelining concepts using the previously built RISC-V core. The lecture focuses on:

- CPU pipelining
- waterfall pipeline representation
- instruction overlap
- pipeline stage partitioning
- performance improvement through pipelining
- inter-instruction dependencies
- control hazards
- read-after-write hazards

The lecture explains:
- why pipelining improves performance
- how instructions overlap in execution
- how timing dependencies create hazards
- why some datapath dependencies become problematic after pipelining

This lecture establishes the conceptual foundation for:
- pipelined CPU design
- hazard analysis
- pipeline timing reasoning

inside the RISC-V processor.

---

# Motivation For Pipelining

To increase clock frequency, logic must be partitioned into multiple pipeline stages.

---

# Why Pipelining Helps

Instead of executing all logic in one cycle, the processor spreads execution across multiple cycles. This reduces combinational delay per cycle.

---

# Overlapped Execution

Pipelining allows multiple instructions to execute simultaneously in different stages.

---

# Branch Hazard

We don't know the branch target until stage three. But next instruction PC selection needs that information earlier. This creates a control hazard. Branch target computation occurs too late for immediate next PC selection.

---

# Read-After-Write Hazard

We might need to read before the previous instruction writes. This creates a read-after-write hazard. Register writes occur later in pipeline, while next instruction reads may occur earlier. This causes operand hazards.

# Hardware Perspective

Pipelining improves throughput but introduces timing dependencies between overlapping instructions. We must therefore solve:

- data hazards
- control hazards
- timing synchronization problems.

---

# Key Learning Outcome

After this lecture, the learner understands:

- CPU pipelining motivation
- waterfall pipeline representation
- overlapped instruction execution
- inter-instruction dependencies
- control hazards
- read-after-write hazards
- timing conflicts in pipelines
- performance-oriented stage partitioning

This lecture establishes the conceptual foundation for pipelined processor design.

---

# Notes

This lecture transitions to true pipelined CPU architecture reasoning.