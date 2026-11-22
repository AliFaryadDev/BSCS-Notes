
# Code Segment

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition](#definition)
- [Purpose](#purpose)
- [Code Segment Register](#code-segment-register)
- [Working](#working)
- [Example](#example)
- [Conclusion](#conclusion)

---

## Introduction

In Assembly Language, a program is divided into different memory segments. The Code Segment stores the instructions that are executed by the processor.

## Definition

The Code Segment is a memory area that contains the machine instructions of a program.

## Purpose

- Stores program instructions.
- Helps the CPU locate the instructions.
- Separates program code from data and stack.

## Code Segment Register

The **CS (Code Segment) Register** stores the base address of the Code Segment.

The **IP (Instruction Pointer) Register** stores the offset address of the next instruction to be executed.

The physical address is calculated as:

`Physical Address = CS × 10H + IP`

## Working

1. CS identifies the starting location of the Code Segment.
2. IP identifies the next instruction within that segment.
3. The CPU combines CS and IP to calculate the physical address.
4. The CPU fetches and executes the instruction.

## Example

```asm
MOV AX, 10
MOV BX, 20
ADD AX, BX
```

These instructions are stored in the Code Segment and executed by the CPU.

## Conclusion

The Code Segment stores program instructions, while CS and IP help the processor locate the instructions to execute.
