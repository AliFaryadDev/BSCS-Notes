
# Functions of Registers

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Functions of General Purpose Registers](#functions-of-general-purpose-registers)
- [Functions of Segment Registers](#functions-of-segment-registers)
- [Functions of Pointer Registers](#functions-of-pointer-registers)
- [Functions of Index Registers](#functions-of-index-registers)
- [Function of Instruction Pointer](#function-of-instruction-pointer)
- [Function of Flag Register](#function-of-flag-register)
- [Register Examples](#register-examples)
- [Conclusion](#conclusion)

---

## Introduction

Registers are used by the CPU to store information temporarily during program execution.

Each register has a specific function that helps the processor perform operations efficiently.

The Intel 8086 contains different types of registers, including general-purpose, segment, pointer, index, instruction pointer, and flag registers.

## Functions of General Purpose Registers

### 1. AX — Accumulator Register

**Functions:**

- Stores operands and arithmetic results.
- Used in multiplication and division.
- Commonly used in input/output operations.

**Example:**

```asm
MOV AX, 10
ADD AX, 5
```

Result:

```text
AX = 15
```

### 2. BX — Base Register

**Functions:**

- Stores base addresses.
- Helps access memory locations.
- Can be used for general data storage.

**Example:**

```asm
MOV BX, 1000H
MOV AX, [BX]
```

The processor accesses the memory location using the offset stored in BX.

### 3. CX — Count Register

**Functions:**

- Stores loop counters.
- Controls the LOOP instruction.
- Holds the count for certain shift and rotate operations.

**Example:**

```asm
MOV CX, 5

L1:
    LOOP L1
```

The LOOP instruction decreases CX and repeats while CX is not zero.

### 4. DX — Data Register

**Functions:**

- Stores data for multiplication and division.
- Works with AX for larger arithmetic results.
- Stores I/O port addresses in certain I/O instructions.

**Example:**

```asm
MOV DX, 03F8H
```

## Functions of Segment Registers

### 1. CS — Code Segment

Stores the base address of the segment containing program instructions.

It works with IP to locate the next instruction.

### 2. DS — Data Segment

Stores the base address of the segment containing program data.

It is commonly used for accessing variables.

### 3. SS — Stack Segment

Stores the base address of the memory segment used for stack operations.

It works with SP and BP.

### 4. ES — Extra Segment

Provides an additional data segment.

It is commonly used as the destination segment in string operations.

## Functions of Pointer Registers

### 1. SP — Stack Pointer

- Points to the top of the stack using an offset.
- Changes during PUSH and POP operations.
- Works with SS to identify the stack location.

### 2. BP — Base Pointer

- Accesses data stored in the stack.
- Helps access procedure parameters.
- Provides a reference point for local variables.

## Functions of Index Registers

### 1. SI — Source Index

- Holds the offset of source data.
- Helps access data in arrays and memory.
- Used in string operations.

### 2. DI — Destination Index

- Holds the offset of destination data.
- Helps identify where data should be stored.
- Used in string operations.

## Function of Instruction Pointer

The IP register holds the offset address of the next instruction.

It works with CS to identify the next instruction in memory.

**Example:**

```text
CS = 2000H
IP = 0100H
```

The next instruction is located using the CS:IP address.

## Function of Flag Register

The Flag Register indicates the status of the processor after operations and controls certain processor activities.

### Status Flags

- **CF:** Indicates carry or borrow.
- **ZF:** Indicates whether the result is zero.
- **SF:** Indicates the sign of the result.
- **OF:** Indicates signed overflow.
- **PF:** Indicates even parity.
- **AF:** Indicates carry between lower and upper nibbles.

### Control Flags

- **TF:** Enables single-step execution.
- **IF:** Controls maskable interrupts.
- **DF:** Controls the direction of string operations.

## Register Examples

| Register | Main Function |
|---|---|
| AX | Arithmetic and accumulator operations |
| BX | Base addressing |
| CX | Counting and loops |
| DX | Data and I/O operations |
| CS | Code segment |
| DS | Data segment |
| SS | Stack segment |
| ES | Extra segment |
| SP | Stack top offset |
| BP | Stack data access |
| SI | Source indexing |
| DI | Destination indexing |
| IP | Next instruction offset |
| FLAGS | Status and control information |

## Conclusion

Each Intel 8086 register has a specific role. General-purpose registers handle data, segment registers identify memory segments, pointer and index registers access memory, IP tracks instructions, and FLAGS stores processor status and control information.
