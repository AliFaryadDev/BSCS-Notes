
# NEG Instruction

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition](#definition)
- [Purpose](#purpose)
- [Syntax](#syntax)
- [Working](#working)
- [Example](#example)
- [Flags Affected](#flags-affected)
- [Conclusion](#conclusion)

---

## Introduction

The NEG instruction is used to change the sign of a number by calculating its two's complement.

## Definition

NEG (Negate) is an arithmetic instruction that subtracts the destination operand from zero.

**Formula:**

`NEG destination = 0 - destination`

## Purpose

- Converts a positive number into a negative number.
- Converts a negative number into a positive number.
- Calculates the two's complement of a number.

## Syntax

```asm
NEG destination
```

## Working

1. The CPU reads the destination operand.
2. It subtracts the value from zero.
3. The two's complement result is stored in the same destination.
4. Status flags are updated.

## Example

```asm
MOV AL, 5

NEG AL
```

**Before NEG:**

AL = 5

**After NEG:**

AL = -5

In 8-bit binary:

```text
 00000101    (5)
 11111010    (One's complement)
+       1
---------
 11111011    (-5)
```

## Flags Affected

| Flag | Effect |
|---|---|
| CF | Set if the original operand was non-zero; otherwise cleared. |
| ZF | Set if the result is zero. |
| SF | Updated according to the result. |
| OF | Set if the most negative signed value is negated. |
| PF | Updated according to parity. |
| AF | Updated according to auxiliary carry/borrow. |

## Conclusion

The NEG instruction calculates the two's complement of an operand and stores the result in the same destination.
