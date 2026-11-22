
# Variants of MOV Instruction

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition](#definition)
- [Purpose](#purpose)
- [Types of MOV Instruction](#types-of-mov-instruction)
- [Examples](#examples)
- [Important Rules](#important-rules)
- [Conclusion](#conclusion)

---

## Introduction

The MOV instruction is one of the most commonly used instructions in 8086 Assembly Language. It transfers data from a source to a destination.

## Definition

The MOV instruction copies data from a source operand to a destination operand.

**Syntax:**

```asm
MOV destination, source
```

## Purpose

- Transfers data between registers.
- Transfers data between registers and memory.
- Loads immediate values into registers.
- Initializes registers with values.

## Types of MOV Instruction

### 1. Immediate to Register

Transfers a constant value into a register.

```asm
MOV AX, 1234H
MOV BL, 05H
```

### 2. Register to Register

Copies data from one register to another.

```asm
MOV AX, BX
MOV CL, DL
```

### 3. Memory to Register

Copies data from a memory location into a register.

```asm
MOV AX, [2000H]
```

### 4. Register to Memory

Copies data from a register into a memory location.

```asm
MOV [2000H], AX
```

### 5. Immediate to Memory

Transfers a constant value directly into a memory location.

```asm
MOV BYTE PTR [2000H], 25H
```

## Examples

```asm
MOV AX, 1000H
MOV BX, AX
MOV CX, 2000H
MOV [3000H], CX
```

**Working:**

- AX receives 1000H.
- BX receives the value of AX.
- CX receives 2000H.
- The value of CX is copied into memory location 3000H.

## Important Rules

- MOV does not change the source operand.
- Both operands must have the same size.
- Memory-to-memory MOV is not allowed in 8086.
- MOV cannot transfer an immediate value directly into a segment register.
- MOV does not affect the status flags.

## Conclusion

The MOV instruction is used to copy data between registers, memory locations, and immediate values. It does not perform arithmetic operations.
