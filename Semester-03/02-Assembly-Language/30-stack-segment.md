
# Stack Segment

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition of Stack Segment](#definition-of-stack-segment)
- [Purpose of Stack Segment](#purpose-of-stack-segment)
- [SS Register](#ss-register)
- [SP Register](#sp-register)
- [Stack Organization](#stack-organization)
- [Stack Operations](#stack-operations)
- [PUSH Operation](#push-operation)
- [POP Operation](#pop-operation)
- [Stack Initialization](#stack-initialization)
- [Complete Example](#complete-example)
- [Conclusion](#conclusion)

---

## Introduction

The Stack Segment is a memory area used to temporarily store data during program execution.

It is commonly used for saving register values, procedure return addresses, and temporary information.

In Intel 8086, the Stack Segment is identified by the SS register and works with the Stack Pointer (SP).

## Definition of Stack Segment

A Stack Segment is a memory section used to store temporary data in a Last In, First Out (LIFO) structure.

## Purpose of Stack Segment

- Temporarily stores data.
- Saves register values.
- Stores procedure return addresses.
- Supports procedure calls and returns.
- Helps manage temporary information during program execution.

## SS Register

SS stands for Stack Segment.

It is a 16-bit segment register in the Intel 8086 processor.

### Functions of SS

1. Stores the base address of the stack segment.
2. Identifies the memory segment used for stack operations.
3. Works with SP to locate the top of the stack.
4. Helps the processor access stack memory.

## SP Register

SP stands for Stack Pointer.

It is a 16-bit pointer register in the Intel 8086 processor.

### Functions of SP

1. Stores the offset address of the top of the stack.
2. Changes during PUSH and POP operations.
3. Works with SS to identify stack memory locations.
4. Helps manage stack operations.

## Stack Organization

The stack follows the Last In, First Out (LIFO) principle.

This means the last item inserted into the stack is the first item removed.

### Example

```text
        STACK

       +-------+
       |   30  |  ← Top
       +-------+
       |   20  |
       +-------+
       |   10  |
       +-------+
```

If the stack contains 10, 20, and 30, the first value removed will be 30.

### Stack Direction

In Intel 8086, the stack grows toward lower memory addresses.

- PUSH decreases SP.
- POP increases SP.

## Stack Operations

The two main stack operations are:

1. PUSH
2. POP

## PUSH Operation

PUSH is used to place data onto the stack.

In the 8086, a word is pushed onto the stack.

### Working

1. SP decreases by 2.
2. The data is stored at the memory location SS:SP.

**Operation:**

```text
SP ← SP - 2
SS:SP ← Data
```

**Example:**

```asm
MOV AX, 1234H
PUSH AX
```

The value of AX is stored on the stack.

## POP Operation

POP is used to remove data from the top of the stack.

In the 8086, a word is popped from the stack.

### Working

1. Data is read from SS:SP.
2. The data is transferred to the destination.
3. SP increases by 2.

**Operation:**

```text
Destination ← SS:SP
SP ← SP + 2
```

**Example:**

```asm
POP BX
```

The top word of the stack is transferred into BX.

## Stack Initialization

In MASM/TASM-style programming, the `.STACK` directive reserves stack memory.

**Example:**

```asm
.STACK 100H
```

This reserves 100H bytes for the stack.

The assembler and program environment arrange the stack segment and initial stack pointer.

## Complete Example

```asm
.MODEL SMALL
.STACK 100H

.DATA

.CODE

MAIN PROC

    MOV AX, @DATA
    MOV DS, AX

    MOV AX, 1234H
    PUSH AX

    MOV BX, 5678H

    POP BX

    MOV AH, 4CH
    INT 21H

MAIN ENDP

END MAIN
```

### Working

1. AX receives 1234H.
2. PUSH AX stores 1234H on the stack.
3. BX receives 5678H.
4. POP BX retrieves the top stack value.
5. BX receives 1234H.

**Final Result:**

```text
AX = 1234H
BX = 1234H
```

## Conclusion

The Stack Segment is used for temporary data storage in Intel 8086. The SS register identifies the stack segment, while SP points to the top of the stack. PUSH and POP instructions manage stack data using the LIFO principle.
