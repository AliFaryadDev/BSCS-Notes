
# Program Structure

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition](#definition)
- [Main Sections of an Assembly Program](#main-sections-of-an-assembly-program)
- [Model Directive](#model-directive)
- [Stack Section](#stack-section)
- [Data Section](#data-section)
- [Code Section](#code-section)
- [Program Entry and Exit](#program-entry-and-exit)
- [Complete Assembly Program](#complete-assembly-program)
- [Conclusion](#conclusion)

---

## Introduction

Program Structure describes how an Assembly Language program is organized into different sections.

A structured program separates memory configuration, data declarations, executable instructions, and program termination.

In MASM/TASM-style 8086 programming, directives such as `.MODEL`, `.STACK`, `.DATA`, and `.CODE` are commonly used.

## Definition

Program Structure is the organization of an Assembly Language program into different sections to define memory, data, instructions, and execution flow.

## Main Sections of an Assembly Program

A typical 8086 assembly program contains:

1. Model Directive
2. Stack Section
3. Data Section
4. Code Section
5. Program Entry Point
6. Program Termination

## Model Directive

The `.MODEL` directive specifies the memory model of a program.

**Example:**

```asm
.MODEL SMALL
```

It tells the assembler to use the Small memory model.

## Stack Section

The `.STACK` directive reserves memory for stack operations.

**Example:**

```asm
.STACK 100H
```

This reserves 100H bytes for the stack.

## Data Section

The `.DATA` directive begins the data segment.

It is used to declare variables and constants.

**Example:**

```asm
.DATA

NUM1 DB 10
NUM2 DB 20
RESULT DB ?
```

## Code Section

The `.CODE` directive begins the code segment.

It contains the executable instructions of the program.

**Example:**

```asm
.CODE

MAIN PROC

    MOV AX, @DATA
    MOV DS, AX

    MOV AL, NUM1
    ADD AL, NUM2
    MOV RESULT, AL

MAIN ENDP
```

## Program Entry and Exit

### Program Entry

The `PROC` directive defines the beginning of a procedure.

**Example:**

```asm
MAIN PROC
```

### Program Exit

A DOS-based program can terminate using interrupt 21H with function 4CH.

**Example:**

```asm
MOV AH, 4CH
INT 21H
```

The `END` directive marks the end of the source program.

## Complete Assembly Program

```asm
.MODEL SMALL
.STACK 100H

.DATA
    NUM1 DB 10
    NUM2 DB 20
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

## Explanation

1. `.MODEL SMALL` selects the Small memory model.
2. `.STACK 100H` reserves stack memory.
3. `.DATA` starts the data section.
4. Variables are declared inside the data section.
5. `.CODE` starts the code section.
6. `MAIN PROC` defines the main procedure.
7. `MOV AX, @DATA` loads the data segment address.
8. `MOV DS, AX` initializes the DS register.
9. Arithmetic instructions perform the calculation.
10. `INT 21H` terminates the DOS program.
11. `END MAIN` marks the program entry point.

## Conclusion

Program Structure organizes an Assembly Language program into sections for memory configuration, data declarations, executable instructions, and program termination.
