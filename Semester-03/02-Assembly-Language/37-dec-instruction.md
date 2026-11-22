
# DEC Instruction

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

The DEC instruction is used to decrease the value of an operand by one.

## Definition

DEC (Decrement) is an arithmetic instruction that subtracts 1 from the destination operand.

## Purpose

- Decreases a register value by one.
- Decreases a memory value by one.
- Updates counters and loop variables.

## Syntax

```asm
DEC destination
```

## Working

1. The CPU reads the destination operand.
2. It subtracts 1 from the value.
3. The updated result is stored in the same destination.
4. Status flags are updated.

## Example

```asm
MOV AX, 5

DEC AX
```

**Before DEC:**

AX = 5

**After DEC:**

AX = 4

## Flags Affected

| Flag | Effect |
|---|---|
| CF | Not affected. |
| ZF | Set if the result is zero. |
| SF | Updated according to the result. |
| OF | Updated according to signed overflow. |
| PF | Updated according to parity. |
| AF | Updated according to auxiliary borrow. |

## Conclusion

The DEC instruction decreases the value of its destination operand by one. It does not affect the Carry Flag.
