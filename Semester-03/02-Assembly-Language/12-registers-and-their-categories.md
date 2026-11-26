# Registers and Their Categories

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition of Registers](#definition-of-registers)
- [Categories of 8086 Registers](#categories-of-8086-registers)
- [General Purpose Registers](#general-purpose-registers)
- [Segment Registers](#segment-register)
- [Pointer and Index Registers](#pointer-and-index-registers)
- [Control and Status Registers](#Control-and Status Registers)

- [Conclusion](#conclusion)

---

## Introduction

Registers are small and high-speed storage locations inside the CPU.

They temporarily store data, addresses, instructions, and intermediate results during program execution.

The Intel 8086 processor contains 14 programmer-visible 16-bit registers.

## Definition of Registers

A register is a small, high-speed storage location inside a processor used to hold data, addresses, instructions, or results temporarily.

## Categories of 8086 Registers

The registers of Intel 8086 are divided into two broad categories: **General Purpose Registers** and **Special Purpose Registers** (which include Segment, Pointer, Index, Instruction Pointer, and Flag registers).

### General Purpose Registers

General Purpose Registers are used to store data and intermediate results during program execution.

The Intel 8086 has four main general-purpose registers:

#### 1. AX — Accumulator Register

- Used in arithmetic and logical operations.
- Commonly used in multiplication and division.
- Can be divided into `AH` and `AL`.

#### 2. BX — Base Register

- Used to store base addresses.
- Can be used in memory addressing.
- Can be divided into `BH` and `BL`.

#### 3. CX — Count Register

- Used as a counter in loops.
- Used in shift and rotate operations.
- Can be divided into `CH` and `CL`.

#### 4. DX — Data Register

- Used in multiplication and division.
- Used in I/O operations.
- Can be divided into `DH` and `DL`.

### Special Purpose Registers

Special Purpose Registers are dedicated to specific processor tasks such as memory segmentation, stack management, instruction tracking, and status flags.

#### Segment Registers

Segment Registers store the starting addresses of memory segments.

The Intel 8086 has four segment registers:

1. **CS — Code Segment:** Stores the base address of the code segment.
2. **DS — Data Segment:** Stores the base address of the data segment.
3. **SS — Stack Segment:** Stores the base address of the stack segment.
4. **ES — Extra Segment:** Stores the base address of an additional data segment.

#### Pointer Registers

Pointer Registers are used to hold offset addresses associated with stack operations and instruction execution.

1. **SP — Stack Pointer**
   - Stores the offset address of the top of the stack.
   - Works with the Stack Segment register (`SS`).
2. **BP — Base Pointer**
   - Used to access data in the stack segment.
   - Commonly used to access procedure parameters and local variables.

#### Index Registers

Index Registers are used to store offset addresses and access data in memory, especially in indexed addressing and string operations.

1. **SI — Source Index**
   - Holds the source offset address.
   - Commonly used to access source data in memory.
   - Used in string operations.
2. **DI — Destination Index**
   - Holds the destination offset address.
   - Commonly used to access destination data in memory.
   - Used in string operations.

#### Instruction Pointer

The Instruction Pointer (`IP`) stores the offset address of the next instruction to be executed.

It works with the Code Segment (`CS`) register to identify the next instruction.

#### Flag Register

The Flag Register stores status and control flags that describe the results of operations and control processor behavior.

Important flags include:

- Carry Flag (`CF`)
- Zero Flag (`ZF`)
- Sign Flag (`SF`)
- Overflow Flag (`OF`)
- Parity Flag (`PF`)
- Auxiliary Carry Flag (`AF`)
- Direction Flag (`DF`)
- Interrupt Flag (`IF`)
- Trap Flag (`TF`)

## Conclusion

Registers are essential components of the Intel 8086 processor. They provide fast storage for data, addresses, and control information. Different register categories perform different tasks during instruction execution.
