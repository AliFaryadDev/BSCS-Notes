
# XCHG Instruction

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition](#definition)
- [Purpose](#purpose)
- [Syntax](#syntax)
- [Working](#working)
- [Example](#example)
- [Important Rules](#important-rules)
- [Conclusion](#conclusion)

---

## Introduction

The XCHG instruction is used to exchange data between two operands.

## Definition

XCHG (Exchange) is an Assembly Language instruction that swaps the values of two operands.

## Purpose

- Exchanges data between registers.
- Exchanges data between a register and a memory location.
- Swaps values without using an additional register.

## Syntax

```asm
XCHG destination, source
```

## Working

The XCHG instruction performs three basic steps:

1. Takes the value of the first operand.
2. Takes the value of the second operand.
3. Exchanges both values.

## Example

```asm
MOV AX, 1000H
MOV BX, 2000H

XCHG AX, BX
```

**Before XCHG:**

| Register | Value |
|---|---|
| AX | 1000H |
| BX | 2000H |

**After XCHG:**

| Register | Value |
|---|---|
| AX | 2000H |
| BX | 1000H |

## Important Rules

- Both operands must have the same size.
- At least one operand must be a register.
- Memory-to-memory exchange is not allowed.
- XCHG does not affect the status flags.

## Conclusion

The XCHG instruction exchanges the values of two operands without changing the total data stored in them.
