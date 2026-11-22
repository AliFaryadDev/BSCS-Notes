
# INC Instruction

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

The INC instruction is used to increase the value of an operand by one.

## Definition

INC (Increment) is an arithmetic instruction that adds 1 to the destination operand.

## Purpose

- Increases a register value by one.
- Increases a memory value by one.
- Updates counters and loop variables.

## Syntax

```asm
INC destination
```

## Working

1. The CPU reads the destination operand.
2. It adds 1 to the value.
3. The updated result is stored in the same destination.
4. Status flags are updated.

## Example

```asm
MOV AX, 5

INC AX
```

**Before INC:**

AX = 5

**After INC:**

AX = 6

## Flags Affected

| Flag | Effect |
|---|---|
| CF | Not affected. |
| ZF | Set if the result is zero. |
| SF | Updated according to the result. |
| OF | Updated according to signed overflow. |
| PF | Updated according to parity. |
| AF | Updated according to auxiliary carry. |

## Conclusion

The INC instruction increases the value of its destination operand by one. It does not affect the Carry Flag.
