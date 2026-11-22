
# Addressing Modes

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition](#definition)
- [Types of Addressing Modes](#types-of-addressing-modes)
- [Direct Addressing Mode](#direct-addressing-mode)
- [Indirect Addressing Mode](#indirect-addressing-mode)
- [Register Addressing Mode](#register-addressing-mode)
- [Immediate Addressing Mode](#immediate-addressing-mode)
- [Relative Addressing Mode](#relative-addressing-mode)
- [Indexed Addressing Mode](#indexed-addressing-mode)
- [Comparison of Addressing Modes](#comparison-of-addressing-modes)
- [Conclusion](#conclusion)

---

## Introduction

Addressing Modes describe how an instruction identifies the data or operand required for an operation.

They determine where the operand is located and how the processor obtains it.

Different addressing modes provide flexibility in accessing data from registers, memory, or directly from an instruction.

## Definition

An Addressing Mode is the method used by a processor instruction to specify the location or value of its operand.

## Types of Addressing Modes

Common addressing modes include:

1. Direct Addressing Mode
2. Indirect Addressing Mode
3. Register Addressing Mode
4. Immediate Addressing Mode
5. Relative Addressing Mode
6. Indexed Addressing Mode

## Direct Addressing Mode

In Direct Addressing Mode, the instruction directly specifies the memory address of the operand.

**Example:**

```text
LDA 500
```

The processor loads the contents of memory location 500 into the accumulator.

**Effective Address:**

```text
EA = Address field
```

## Indirect Addressing Mode

In Indirect Addressing Mode, the address field points to a memory location that contains the actual address of the operand.

**Example:**

```text
LDA I 500
```

The processor first accesses memory location 500 to obtain the effective address and then retrieves the operand.

**Effective Address:**

```text
EA = M[Address field]
```

## Register Addressing Mode

In Register Addressing Mode, the operand is stored in a CPU register.

**Example:**

```asm
MOV AX, BX
```

The contents of BX are copied into AX.

## Immediate Addressing Mode

In Immediate Addressing Mode, the actual data is provided directly in the instruction.

**Example:**

```asm
MOV AX, 10
```

The value 10 is loaded into AX.

## Relative Addressing Mode

In Relative Addressing Mode, the effective address is calculated using the current instruction pointer and a displacement.

It is commonly used in branch and jump instructions.

**Example:**

```asm
JMP SHORT LABEL
```

The processor uses a relative displacement to determine the target instruction address.

## Indexed Addressing Mode

In Indexed Addressing Mode, an index register is added to a displacement to calculate the effective address.

It is commonly used to access arrays and tables.

**Example:**

```asm
MOV AX, [SI+10]
```

The effective address is calculated using SI plus the displacement.

## Comparison of Addressing Modes

| Addressing Mode | Operand Location |
|---|---|
| Direct | Memory address is specified directly |
| Indirect | Actual address is obtained indirectly |
| Register | CPU register |
| Immediate | Value is inside the instruction |
| Relative | Address is calculated using displacement |
| Indexed | Address is calculated using index register |

## Important Note

Mano's Basic Computer specifically demonstrates direct and indirect memory addressing modes in its memory reference instructions.

Intel 8086 supports a wider range of addressing modes, including register, immediate, direct memory, based, indexed, and relative addressing.

## Conclusion

Addressing Modes determine how a processor locates and accesses operands. They provide different ways to obtain data from registers, memory, and instructions.
