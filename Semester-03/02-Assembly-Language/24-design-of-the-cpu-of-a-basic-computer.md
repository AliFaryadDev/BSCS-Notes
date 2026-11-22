
# Design of the CPU of a Basic Computer

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition](#definition)
- [Main Components of CPU](#main-components-of-cpu)
- [Registers](#registers)
- [Arithmetic Logic Unit](#arithmetic-logic-unit)
- [Control Unit](#control-unit)
- [Common Bus System](#common-bus-system)
- [Memory Unit](#memory-unit)
- [CPU Organization Diagram](#cpu-organization-diagram)
- [Working of CPU](#working-of-cpu)
- [Conclusion](#conclusion)

---

## Introduction

The Central Processing Unit (CPU) is the main processing component of a computer.

It executes instructions, performs arithmetic and logical operations, and controls the activities of other computer components.

The design of a Basic Computer CPU describes how registers, the ALU, control unit, and memory are organized to execute instructions.

## Definition

CPU Design is the process of organizing and connecting the internal components of a processor to perform instruction execution and data processing.

## Main Components of CPU

The CPU of Mano's Basic Computer contains:

1. Registers
2. Arithmetic Logic Unit (ALU)
3. Control Unit
4. Common Bus System

## Registers

Registers are temporary storage locations used during instruction execution.

Important registers in Mano's Basic Computer include:

| Register | Function |
|---|---|
| AR | Holds memory addresses |
| PC | Holds the next instruction address |
| DR | Holds data read from memory |
| AC | Stores arithmetic and logical results |
| IR | Holds the current instruction |
| TR | Temporarily stores data |
| INPR | Holds input data |
| OUTR | Holds output data |

Other important components include the E flip-flop, sequence counter, and status flags.

## Arithmetic Logic Unit

The Arithmetic Logic Unit performs arithmetic and logical operations.

### Arithmetic Operations

- Addition
- Increment
- Complement-related operations

### Logical Operations

- AND
- Complement
- Shift operations

The ALU uses register values to perform the required operations.

## Control Unit

The Control Unit coordinates the activities of the CPU.

### Functions

- Fetches instructions.
- Decodes instructions.
- Generates control signals.
- Controls register transfers.
- Coordinates ALU operations.
- Manages instruction timing.

In Mano's Basic Computer, the control system uses an instruction decoder, timing decoder, sequence counter, and control logic.

## Common Bus System

A Common Bus System provides a shared communication path between registers and other CPU components.

It allows data to move between different registers.

### Functions

- Transfers data between registers.
- Reduces the need for separate connections.
- Helps coordinate internal CPU operations.

## Memory Unit

The memory unit stores instructions and data required by the CPU.

In Mano's Basic Computer model, the main memory contains 4096 words, with each word containing 16 bits.

The Address Register (AR) is 12 bits wide and identifies one of the 4096 memory locations.

## CPU Organization Diagram

```text
              +----------------+
              |   Control Unit  |
              +--------+-------+
                       |
                       v
+----------+     +-----------+     +----------+
| Registers|<--->| Common Bus|<--->| Memory   |
+----------+     +-----------+     +----------+
     |
     v
+----------------+
|      ALU       |
+----------------+
     |
     v
  Result
```

## Working of CPU

The CPU performs the following operations:

1. Fetches an instruction from memory.
2. Stores it in the Instruction Register.
3. Decodes the instruction.
4. Obtains the required operands.
5. Performs the operation using the ALU or control logic.
6. Stores the result in a register or memory.
7. Moves to the next instruction.

## Conclusion

The CPU of a Basic Computer consists of registers, an ALU, a Control Unit, and a common bus system. These components work together to execute instructions and perform data processing.
