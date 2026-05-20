## Overview

This lecture focuses on:

- visualization tools
- CPU debugging
- waveform analysis
- pipeline behavior
- branch handling
- protected solution infrastructure
- visualization-driven learning

The lecture demonstrates the completed RISC-V CPU visualization and explains how learners should:

- debug
- compare
- analyze
- validate

their CPU implementations.

---

# Pipeline Branch Behavior

The PC continues after the branch because pipeline has not yet resolved branch. Then The machine realizes that it went too far. This demonstrates speculative/wrong-path execution.

## Branch Recovery

The CPU then redirects PC to proper branch target.

# Hardware Perspective 

Pipelined CPUs often execute wrong-path instructions temporarily. This is fundamental to:

- branch prediction
- speculative execution
- pipeline recovery
- CPU control flow handling

---

# Key Learning Outcome

After this lecture, the learner understands:

- CPU visualization usage
- pipeline debugging
- branch recovery behavior
- wrong-path execution
- register tracking
- structural CPU debugging

---

# Notes

This lecture introduces CPU debugging techniques.

The learner learns to debug using:

- visualization
- waveforms
- pipeline analysis
- branch tracking
- architectural state inspection.