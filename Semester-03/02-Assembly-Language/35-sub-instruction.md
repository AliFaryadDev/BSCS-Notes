
# SUB Instruction

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

The SUB instruction is used to subtract one operand from another in Assembly Language.

## Definition

SUB is an arithmetic instruction that subtracts the source operand from the destination operand and stores the result in the destination.

## Purpose

- Performs subtraction.
- Subtracts register values.
- Subtracts immediate values.
- Subtracts data from memory.

## Syntax

```asm
SUB destination, source
```

## Working

1. The CPU reads the destination operand.
2. The CPU reads the source operand.
3. The source value is subtracted from the destination value.
4. The result is stored in the destination operand.
5. Status flags are updated.

## Example

```asm
MOV AX, 30
MOV BX, 10

SUB AX, BX
```

**Before SUB:**

| Register | Value |
|---|---:|
| AX | 30 |
| BX | 10 |

**After SUB:**

| Register | Value |
|---|---:|
| AX | 20 |
| BX | 10 |

The result is stored in AX.

## Flags Affected

| Flag | Purpose |
|---|---|
| CF | Indicates an unsigned borrow. |
| ZF | Set when the result is zero. |
| SF | Indicates the sign of the result. |
| OF | Indicates signed overflow. |
| PF | Indicates even parity in the low byte. |
| AF | Indicates borrow between bit 3 and bit 4. |

## Conclusion

The SUB instruction subtracts the source operand from the destination operand and stores the result in the destination.
