
# Memory Reference Instructions

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition](#definition)
- [Types of Memory Reference Instructions](#types-of-memory-reference-instructions)
- [AND Instruction](#and-instruction)
- [ADD Instruction](#add-instruction)
- [LDA Instruction](#lda-instruction)
- [STA Instruction](#sta-instruction)
- [BUN Instruction](#bun-instruction)
- [BSA Instruction](#bsa-instruction)
- [ISZ Instruction](#isz-instruction)
- [Comparison of Instructions](#comparison-of-instructions)
- [Conclusion](#conclusion)

---

## Introduction

Memory Reference Instructions are instructions that access memory locations to read or write data during program execution.

In Mano's Basic Computer, these instructions use a 12-bit address field to identify memory locations.

They are used for arithmetic operations, data transfer, branching, and program control.

## Definition

Memory Reference Instructions are machine instructions that access memory locations to perform operations on stored data or to change the sequence of program execution.

## Types of Memory Reference Instructions

Mano's Basic Computer has seven memory reference instructions:

1. AND
2. ADD
3. LDA
4. STA
5. BUN
6. BSA
7. ISZ

**Note:** These are instructions of Mano's Basic Computer model, not the Intel 8086 instruction set.

## AND Instruction

The AND instruction performs a bitwise AND operation between the contents of the accumulator and a memory operand.

**Operation:**

```text
AC ← AC AND M[Address]
```

**Example:**

```text
AC = 1100
M[Address] = 1010

Result = 1000
```

## ADD Instruction

The ADD instruction adds the contents of a memory location to the accumulator.

**Operation:**

```text
AC ← AC + M[Address]
E  ← Carry
```

The carry is stored in the E flip-flop.

**Example:**

```text
AC = 5
M[Address] = 3

Result = 8
```

## LDA Instruction

LDA stands for Load Accumulator.

It loads data from a memory location into the accumulator.

**Operation:**

```text
AC ← M[Address]
```

**Example:**

```text
M[100] = 25

LDA 100

AC = 25
```

## STA Instruction

STA stands for Store Accumulator.

It stores the contents of the accumulator into a memory location.

**Operation:**

```text
M[Address] ← AC
```

**Example:**

```text
AC = 50

STA 100

M[100] = 50
```

## BUN Instruction

BUN stands for Branch Unconditionally.

It transfers program execution to the specified memory address.

**Operation:**

```text
PC ← Address
```

**Example:**

```text
BUN 200
```

The next instruction is fetched from address 200.

## BSA Instruction

BSA stands for Branch and Save Return Address.

It is used to call a subroutine.

**Operation:**

```text
M[Address] ← PC
PC ← Address + 1
```

It saves the return address in memory and transfers control to the subroutine.

## ISZ Instruction

ISZ stands for Increment and Skip if Zero.

It increments the contents of a memory location by one.

If the result becomes zero, the next instruction is skipped.

**Operation:**

```text
M[Address] ← M[Address] + 1

If M[Address] = 0:
    PC ← PC + 1
```

## Comparison of Instructions

| Instruction | Function |
|---|---|
| AND | Performs bitwise AND |
| ADD | Adds memory data to AC |
| LDA | Loads data into AC |
| STA | Stores AC into memory |
| BUN | Performs unconditional branch |
| BSA | Calls a subroutine |
| ISZ | Increments memory and skips if zero |

## Conclusion

Memory Reference Instructions are used to access memory and perform different operations. Mano's Basic Computer provides seven memory reference instructions for arithmetic, data transfer, and program control.
