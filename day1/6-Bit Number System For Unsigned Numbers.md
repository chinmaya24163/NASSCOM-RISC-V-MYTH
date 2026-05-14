# 6-Bit Number System For Unsigned Numbers

## Overview

This lecture introduces the binary number system for unsigned numbers.

The lecture explains:
- binary representation
- bit positions
- powers of 2
- decimal-to-binary conversion
- unsigned number ranges

Understanding binary representation is fundamental for:
- digital electronics
- processor architecture
- memory systems
- arithmetic operations inside hardware

---

# What is a Bit?

A bit (Binary Digit) is the smallest unit of digital information.

A bit can have only two values:

```text
0 or 1
```
These values correspond to:

- LOW / HIGH
- FALSE / TRUE
- OFF / ON

inside digital hardware systems.

---

# Binary Number System

Computers use the binary number system because digital hardware naturally operates using:

- two voltage levels
- switching logic
- transistor states

Binary uses base-2 representation.

Example:
```text
1011₂
```

---

# Bit Positions and Powers of 2

Each bit position represents a power of 2.

Example for a 4-bit number:
| Bit Position | Power of 2 | Decimal Value |
| ------------ | ---------- | ------------- |
| 3            | 2³         | 8             |
| 2            | 2²         | 4             |
| 1            | 2¹         | 2             |
| 0            | 2⁰         | 1             |

---

# Example Binary to Decimal Conversion

Convert:
```text
1011₂
```
to decimal.

Calculation:
```text
= (1 × 2³) + (0 × 2²) + (1 × 2¹) + (1 × 2⁰)
= 8 + 0 + 2 + 1
= 11₁₀
```

---

# Unsigned Numbers

Unsigned numbers represent only:

- positive values
- zero

There is:

- no sign bit
- no negative representation

---

# Range of Unsigned Numbers

For an N-bit unsigned number:

- Minimum Value = 0
- Maximum Value = 2ᴺ - 1

---

# Examples of Unsigned Ranges

| Number of Bits | Range      |
| -------------- | ---------- |
| 1-bit          | 0 to 1     |
| 2-bit          | 0 to 3     |
| 4-bit          | 0 to 15    |
| 8-bit          | 0 to 255   |
| 16-bit         | 0 to 65535 |

---

# Decimal to Binary Conversion

Example:

Convert decimal 13 to binary.
```text
13 ÷ 2 = 6 remainder 1
 6 ÷ 2 = 3 remainder 0
 3 ÷ 2 = 1 remainder 1
 1 ÷ 2 = 0 remainder 1
```

Reading remainders bottom-to-top:
```text
1101₂
```

---

# Importance in Hardware

Processors internally operate entirely using binary values. Every operation inside a CPU eventually becomes binary manipulation.

---

# Key Learning Outcome

After this lecture, the learner understands:

- binary number representation
- powers of 2
- unsigned number systems
- binary/decimal conversion
- number ranges in digital systems

---

# Notes

All digital hardware fundamentally operates using binary information.