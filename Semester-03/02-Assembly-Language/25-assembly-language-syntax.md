
# Assembly Language Syntax

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition](#definition)
- [Basic Structure of Assembly Language](#basic-structure-of-assembly-language)
- [Instruction Format](#instruction-format)
- [Labels](#labels)
- [Mnemonics](#mnemonics)
- [Operands](#operands)
- [Comments](#comments)
- [Directives](#directives)
- [Assembly Language Example](#assembly-language-example)
- [Conclusion](#conclusion)

---

## Introduction

Assembly Language Syntax defines the rules and structure used to write Assembly Language programs.

It explains how instructions, labels, operands, comments, and directives are written in an assembly program.

In Intel 8086 programming, assemblers such as MASM and TASM use a structured syntax to translate assembly instructions into machine code.

## Definition

Assembly Language Syntax is the set of rules that determines how assembly instructions, operands, labels, and directives are written in a program.

## Basic Structure of Assembly Language

A typical assembly instruction follows this format:

```asm
LABEL: MNEMONIC OPERAND1, OPERAND2 ; COMMENT
```

### Parts of an Instruction

1. **Label:** An optional name that identifies an instruction or memory location.
2. **Mnemonic:** The operation to be performed.
3. **Operands:** The data or locations used by the instruction.
4. **Comment:** An explanation of the instruction.

## Instruction Format

An instruction contains an operation and may contain one or more operands.

**Example:**

```asm
MOV AX, BX
```

Explanation:

- MOV: Mnemonic.
- AX: Destination operand.
- BX: Source operand.

The instruction copies the contents of BX into AX.

## Labels

A Label is a symbolic name assigned to a memory location or instruction.

It is commonly used with jump and loop instructions.

**Example:**

```asm
START:
    MOV AX, 5
```

Here, START is the label.

## Mnemonics

Mnemonics are short symbolic names used to represent processor instructions.

**Examples:**

| Mnemonic | Meaning |
|---|---|
| MOV | Move data |
| ADD | Addition |
| SUB | Subtraction |
| INC | Increment |
| DEC | Decrement |
| JMP | Unconditional jump |
| CMP | Compare |

## Operands

Operands specify the data or locations on which an instruction operates.

### Types of Operands

1. **Register Operand:** Uses a CPU register.

```asm
MOV AX, BX
```

2. **Immediate Operand:** Uses a constant value.

```asm
MOV AX, 10
```

3. **Memory Operand:** Uses a memory location.

```asm
MOV AX, [2000H]
```

4. **Label Operand:** Uses a symbolic address.

```asm
JMP START
```

## Comments

Comments are explanatory statements written inside a program.

They are ignored by the assembler and do not generate machine instructions.

In MASM/TASM syntax, a semicolon is used to start a comment.

**Example:**

```asm
MOV AX, 5 ; Load 5 into AX
```

## Directives

Directives are instructions given to the assembler to control program organization and assembly.

They are not ordinary CPU instructions.

**Common Directives:**

| Directive | Purpose |
|---|---|
| DB | Define Byte |
| DW | Define Word |
| DD | Define Doubleword |
| EQU | Define a symbolic constant |
| SEGMENT | Define a segment |
| ENDS | End a segment |
| PROC | Begin a procedure |
| ENDP | End a procedure |
| END | End the source program |

## Assembly Language Example

```asm
.MODEL SMALL
.STACK 100H

.DATA
    NUM1 DB 5
    NUM2 DB 3
    RESULT DB ?

.CODE
MAIN PROC

    MOV AX, @DATA
    MOV DS, AX

    MOV AL, NUM1
    ADD AL, NUM2
    MOV RESULT, AL

    MOV AH, 4CH
    INT 21H

MAIN ENDP
END MAIN
```

### Explanation

- `.MODEL SMALL`: Selects the Small memory model.
- `.STACK 100H`: Reserves stack space.
- `.DATA`: Begins the data segment.
- `NUM1 DB 5`: Defines a byte variable.
- `NUM2 DB 3`: Defines another byte variable.
- `RESULT DB ?`: Reserves an uninitialized byte.
- `.CODE`: Begins the code segment.
- `MOV AX, @DATA`: Loads the data segment address.
- `MOV DS, AX`: Initializes DS.
- `MOV AL, NUM1`: Loads the first number.
- `ADD AL, NUM2`: Adds the second number.
- `MOV RESULT, AL`: Stores the result.
- `INT 21H`: Calls DOS services to terminate the program.
- `END MAIN`: Marks the program entry point.

## Conclusion

Assembly Language Syntax provides the rules for writing assembly instructions and programs. It includes labels, mnemonics, operands, comments, and directives that help organize assembly code.
