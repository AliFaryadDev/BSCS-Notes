
# Data Segment

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition of Data Segment](#definition-of-data-segment)
- [Purpose of Data Segment](#purpose-of-data-segment)
- [DS Register](#ds-register)
- [Declaring Data Segment](#declaring-data-segment)
- [Initializing Data Segment](#initializing-data-segment)
- [Declaring Variables](#declaring-variables)
- [Accessing Data Segment Variables](#accessing-data-segment-variables)
- [Complete Example](#complete-example)
- [Conclusion](#conclusion)

---

## Introduction

The Data Segment is a memory area used to store variables, constants, and other data required by an Assembly Language program.

In Intel 8086, the Data Segment is identified by the DS (Data Segment) register.

It allows the processor to access program data stored in memory.

## Definition of Data Segment

A Data Segment is a logical memory section used to store program variables, constants, and other data.

## Purpose of Data Segment

- Stores program variables.
- Stores initialized data.
- Stores uninitialized data.
- Provides access to program data.
- Separates data from executable instructions.

## DS Register

DS stands for Data Segment.

It is a 16-bit segment register in the Intel 8086 processor.

### Functions of DS

1. Stores the base address of the data segment.
2. Helps the CPU access variables stored in memory.
3. Provides the segment part of a memory address.
4. Works with offset addresses to calculate physical addresses.

## Declaring Data Segment

In MASM/TASM-style Assembly Language, the `.DATA` directive is used to begin the data section.

**Syntax:**

```asm
.DATA

VARIABLE_NAME DB VALUE
```

**Example:**

```asm
.DATA

NUM1 DB 10
NUM2 DB 20
```

Here:

- NUM1 stores 10.
- NUM2 stores 20.

## Initializing Data Segment

Before accessing variables through DS, the Data Segment register must be initialized.

**Instructions:**

```asm
MOV AX, @DATA
MOV DS, AX
```

### Explanation

1. `@DATA` represents the address of the program's data segment.
2. `MOV AX, @DATA` loads that address into AX.
3. `MOV DS, AX` transfers the address into DS.

**Important:** A segment register generally cannot receive an immediate value directly, so a general-purpose register is used.

## Declaring Variables

Variables can be declared using different data definition directives.

### 1. DB — Define Byte

Reserves 8 bits.

```asm
AGE DB 20
```

### 2. DW — Define Word

Reserves 16 bits.

```asm
MARKS DW 500
```

### 3. DD — Define Doubleword

Reserves 32 bits.

```asm
TOTAL DD 100000
```

## Accessing Data Segment Variables

Variables can be accessed by using their names in instructions.

**Example:**

```asm
MOV AL, NUM1
```

This instruction loads the value of NUM1 into AL.

Another example:

```asm
MOV NUM2, AL
```

This stores the contents of AL into NUM2.

## Complete Example

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

### Working

1. The data segment is declared using `.DATA`.
2. NUM1 and NUM2 are initialized.
3. RESULT reserves one byte.
4. `MOV AX, @DATA` loads the data segment address.
5. `MOV DS, AX` initializes the DS register.
6. NUM1 is loaded into AL.
7. NUM2 is added to AL.
8. The result is stored in RESULT.

**Final Result:**

```text
NUM1 = 10
NUM2 = 20

RESULT = 30
```

## Conclusion

The Data Segment stores variables and other program data. In Intel 8086, the DS register identifies the data segment and helps the processor access its contents.
