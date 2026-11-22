
# Instruction Cycle

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition](#definition)
- [Stages of Instruction Cycle](#stages-of-instruction-cycle)
- [Fetch Cycle](#fetch-cycle)
- [Decode Cycle](#decode-cycle)
- [Execute Cycle](#execute-cycle)
- [Store Cycle](#store-cycle)
- [Role of Program Counter](#role-of-program-counter)
- [Instruction Cycle Example](#instruction-cycle-example)
- [Conclusion](#conclusion)

---

## Introduction

A computer executes programs by processing instructions stored in memory.

The CPU performs a repeated sequence of operations to execute each instruction. This sequence is called the Instruction Cycle.

The Instruction Cycle is an important concept in Computer Organization because it explains how the processor executes machine instructions.

## Definition

The Instruction Cycle is the complete sequence of steps performed by the CPU to fetch, decode, and execute an instruction stored in memory.

## Stages of Instruction Cycle

The basic Instruction Cycle consists of three main stages:

1. Fetch
2. Decode
3. Execute

Some descriptions also include a separate Store or Write-Back stage.

## Fetch Cycle

The Fetch Cycle is the first stage of the Instruction Cycle.

During this stage, the CPU retrieves the next instruction from memory.

### Working

1. The Program Counter (PC) contains the address of the next instruction.
2. The address is transferred to the Memory Address Register (MAR).
3. The memory sends the instruction to the Memory Data Register (MDR).
4. The instruction is transferred to the Instruction Register (IR).
5. The Program Counter is updated to point to the next instruction.

## Decode Cycle

The Decode Cycle is the second stage of the Instruction Cycle.

During this stage, the Control Unit interprets the instruction stored in the Instruction Register.

### Working

1. The Control Unit examines the instruction.
2. It identifies the operation to perform.
3. It determines the required operands.
4. It identifies the addressing mode.
5. It generates the necessary control signals.

## Execute Cycle

The Execute Cycle is the stage in which the CPU performs the operation specified by the instruction.

### Working

1. Required operands are obtained.
2. The ALU or another CPU component performs the operation.
3. The result is generated.
4. The result is sent to the required destination.

## Store Cycle

The Store Cycle, also called Write-Back, saves the result of an operation when required.

### Working

1. The CPU receives the processing result.
2. The result is written into a destination register or memory location.
3. The processor prepares to execute the next instruction.

**Note:** Not every instruction requires a separate memory write-back operation.

## Role of Program Counter

The Program Counter (PC) is a special-purpose register that holds the address of the next instruction to be fetched.

**Functions:**

- Stores the address of the next instruction.
- Helps maintain the sequence of program execution.
- Updates automatically during normal instruction execution.
- Can be changed by jump and branch instructions.

## Instruction Cycle Example

Consider the following instruction:

```asm
ADD AX, BX
```

This instruction adds the contents of BX to AX.

### Working

**1. Fetch:**

The CPU fetches the ADD instruction from memory.

**2. Decode:**

The Control Unit identifies the ADD operation and its operands.

**3. Execute:**

The ALU adds the contents of AX and BX.

**4. Store:**

The result is stored in AX.

### Example Values

```text
AX = 5
BX = 3

ADD AX, BX

Final AX = 8
```

## Conclusion

The Instruction Cycle is the process through which a CPU executes instructions. Its main stages are Fetch, Decode, and Execute. These stages allow the processor to perform program operations in an organized sequence.
