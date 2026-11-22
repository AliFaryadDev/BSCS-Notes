
# Organization of Intel 8088/8086 Processor

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Basic Organization](#basic-organization)
- [Bus Interface Unit (BIU)](#bus-interface-unit-biu)
- [Execution Unit (EU)](#execution-unit-eu)
- [Functions of BIU](#functions-of-biu)
- [Functions of EU](#functions-of-eu)
- [Instruction Prefetch Queue](#instruction-prefetch-queue)
- [Working of Intel 8086](#working-of-intel-8086)
- [Difference Between BIU and EU](#difference-between-biu-and-eu)
- [Conclusion](#conclusion)

---

## Introduction

Intel 8086 and 8088 are 16-bit microprocessors developed by Intel.

Their internal architecture is divided into two major units:

1. Bus Interface Unit (BIU)
2. Execution Unit (EU)

These two units work together to fetch, decode, and execute instructions.

This organization improves processor efficiency by allowing instruction fetching and execution to overlap.

## Basic Organization

The Intel 8086 processor consists of two major functional units.

### 1. Bus Interface Unit (BIU)

The BIU handles communication between the processor and external devices such as memory and I/O devices.

### 2. Execution Unit (EU)

The EU executes instructions and performs arithmetic and logical operations.

## Bus Interface Unit (BIU)

The Bus Interface Unit is responsible for fetching instructions and transferring data between the processor and external devices.

### Components of BIU

1. Segment Registers
2. Instruction Pointer (IP)
3. Instruction Queue
4. Address Generation Circuit
5. Bus Control Logic

### Functions of BIU

- Fetches instructions from memory.
- Reads data from memory.
- Writes data to memory.
- Performs I/O operations.
- Generates 20-bit physical addresses.
- Stores prefetched instructions in the instruction queue.

## Execution Unit (EU)

The Execution Unit is responsible for executing instructions fetched by the BIU.

### Components of EU

1. Arithmetic Logic Unit (ALU)
2. General Purpose Registers
3. Pointer and Index Registers
4. Flag Register
5. Instruction Decoder
6. Control Circuitry

### Functions of EU

- Decodes instructions.
- Performs arithmetic operations.
- Performs logical operations.
- Executes instructions.
- Updates processor flags.
- Requests memory operations from the BIU when required.

## Instruction Prefetch Queue

An Instruction Prefetch Queue is a temporary storage area that holds instructions fetched from memory before execution.

### Queue Size

- Intel 8086: 6 bytes
- Intel 8088: 4 bytes

### Purpose

The queue allows the BIU to fetch upcoming instructions while the EU executes previously fetched instructions.

This overlapping operation improves processor performance.

**Note:** When a jump or branch changes the instruction sequence, the queue is cleared and refilled from the new address.

## Working of Intel 8086

The processor works through the following steps:

1. The BIU fetches instructions from memory.
2. The fetched instructions are stored in the instruction queue.
3. The EU takes instructions from the queue.
4. The instruction decoder identifies the operation.
5. The ALU or another execution component performs the operation.
6. The BIU handles memory or I/O access when required.

## Difference Between BIU and EU

| BIU | EU |
|---|---|
| Stands for Bus Interface Unit. | Stands for Execution Unit. |
| Handles external bus operations. | Executes instructions. |
| Fetches instructions from memory. | Decodes and executes instructions. |
| Generates physical addresses. | Performs arithmetic and logical operations. |
| Contains the instruction queue. | Contains the ALU and instruction decoder. |

## Conclusion

The Intel 8086 and 8088 processors use two major units: BIU and EU. The BIU handles communication and instruction fetching, while the EU executes instructions. Their parallel operation improves processor efficiency.
