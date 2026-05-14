# 7-RV_D1SK3_L2_Bit_Number_System_For_Signed_Numbers

## Overview

This lecture introduces signed number representation in binary systems.

The lecture explains:
- why signed numbers are required
- sign representation
- positive and negative numbers
- signed number ranges
- 2’s complement representation

Signed number systems are essential for:
- arithmetic operations
- processor ALU design
- instruction execution
- digital hardware implementation

---

# Why Signed Numbers are Needed

Unsigned numbers can only represent:
- positive values
- zero

However, real-world computations also require:
- negative numbers

Examples:
- subtraction
- temperature values
- offsets
- memory addressing
- arithmetic computations

Therefore, processors require signed number representation.

---

# Signed Binary Numbers

In signed binary representation:
- the Most Significant Bit (MSB) acts as the sign bit

Convention:

| MSB | Meaning |
|---|---|
| 0 | Positive |
| 1 | Negative |

---

# 4-Bit Signed Number Example

Example:

```text id="tugpjg"
0101₂ = +5
1101₂ = Negative Number
```
The MSB determines whether the number is:

- positive
- negative

---

# Signed Number Range

For an N-bit signed number using 2’s complement:

- Minimum Value = -2ᴺ⁻¹
- Maximum Value = 2ᴺ⁻¹ - 1

---

# Examples of Signed Number Ranges

| Number of Bits | Range            |
| -------------- | ---------------- |
| 4-bit          | -8 to +7         |
| 8-bit          | -128 to +127     |
| 16-bit         | -32768 to +32767 |
| 32-bit         | -2³¹ to 2³¹-1    |

---

# 2’s Complement Representation

Modern processors use 2’s complement representation.

Method:

- Invert all bits
- Add 1

---

# Example — 2’s Complement

Convert +5 to -5.

- Step 1 — +5 = 0101

- Step 2 — invert bits: 1010

- Step 3 — add 1: 1011

Therefore -5 = 1011₂

Why 2’s Complement is Important

---

# Advantages:

- simple hardware implementation
- easy arithmetic operations
- single representation of zero
- efficient ALU design

Because of these advantages almost all modern processors use 2’s complement arithmetic.

---

# Overflow in Signed Numbers

Overflow occurs when result exceeds representable range.

Example:

- adding two large positive numbers
- adding two large negative numbers

Processors typically detect overflow during ALU operations.

---

# Connection to Processor Hardware

Signed number representation is critical for:

- ALU arithmetic
- subtraction operations
- branch comparisons
- address calculations
- signed instructions

The processor internally performs:

- binary arithmetic
- sign handling
- overflow detection

using hardware logic.

---

# Key Learning Outcome

After this lecture, the learner understands:

- signed binary representation
- sign bits
- signed number ranges
- 2’s complement arithmetic

---

# Notes

Nearly all modern processors internally use 2’s complement representation for signed arithmetic operations.