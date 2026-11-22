
# ADD Instruction

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

The ADD instruction is used to perform addition between two operands in Assembly Language.

## Definition

ADD is an arithmetic instruction that adds the source operand to the destination operand and stores the result in the destination.

## Purpose

- Performs addition.
- Adds register values.
- Adds immediate values.
- Adds data from memory.

## Syntax

```asm
ADD destination, source
```

## Working

1. The CPU reads the destination operand.
2. The CPU reads the source operand.
3. Both values are added.
4. The result is stored in the destination operand.
5. Status flags are updated according to the result.

## Example

```asm
MOV AX, 10
MOV BX, 20

ADD AX, BX
```

**Before ADD:**

| Register | Value |
|---|---:|
| AX | 10 |
| BX | 20 |

**After ADD:**

| Register | Value |
|---|---:|
| AX | 30 |
| BX | 20 |

The result is stored in AX.

## Flags Affected

| Flag | Purpose |
|---|---|
| CF | Indicates carry from the most significant bit. |
| ZF | Set when the result is zero. |
| SF | Indicates the sign of the result. |
| OF | Indicates signed overflow. |
| PF | Indicates even parity in the low byte. |
| AF | Indicates carry from bit 3 to bit 4. |

## Conclusion

The ADD instruction performs addition and stores the result in the destination operand. It also updates the status flags.
