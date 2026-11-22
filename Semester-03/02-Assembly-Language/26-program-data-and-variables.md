
# Program Data and Variables

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition of Data](#definition-of-data)
- [Definition of Variables](#definition-of-variables)
- [Data Types in Assembly Language](#data-types-in-assembly-language)
- [DB Directive](#db-directive)
- [DW Directive](#dw-directive)
- [DD Directive](#dd-directive)
- [Defining Variables](#defining-variables)
- [Initializing Variables](#initializing-variables)
- [Uninitialized Variables](#uninitialized-variables)
- [Constants](#constants)
- [Accessing Variables](#accessing-variables)
- [Conclusion](#conclusion)

---

## Introduction

Programs use data to perform calculations, comparisons, and other operations.

In Assembly Language, data is stored in memory or registers.

Variables are used to reserve memory locations for storing values that can be accessed during program execution.

## Definition of Data

Data refers to values or information that a computer processes and stores.

**Examples:**

- Numbers
- Characters
- Text
- Addresses

## Definition of Variables

A Variable is a named memory location used to store data that can be accessed or modified during program execution.

## Data Types in Assembly Language

Assembly Language uses different data sizes to store values.

Common data definition directives include:

1. DB — Define Byte
2. DW — Define Word
3. DD — Define Doubleword

## DB Directive

DB stands for Define Byte.

It reserves one or more bytes of memory.

**Size:** 8 bits

**Example:**

```asm
NUM DB 10
```

This defines a variable named NUM and stores the value 10 in one byte.

## DW Directive

DW stands for Define Word.

It reserves one or more words of memory.

**Size:** 16 bits

**Example:**

```asm
NUM DW 1000
```

This defines a 16-bit variable.

## DD Directive

DD stands for Define Doubleword.

It reserves four bytes of memory.

**Size:** 32 bits

**Example:**

```asm
NUM DD 100000
```

This defines a 32-bit variable.

## Defining Variables

Variables are defined using a name, a data definition directive, and an optional initial value.

**Syntax:**

```asm
VARIABLE_NAME DB VALUE
```

**Examples:**

```asm
AGE DB 20
MARKS DW 450
TOTAL DD 100000
```

## Initializing Variables

Initializing a variable means assigning an initial value when it is defined.

**Example:**

```asm
NUM1 DB 10
NUM2 DW 500
```

## Uninitialized Variables

An uninitialized variable reserves memory without specifying an initial value.

In MASM/TASM, the question mark `?` can be used for this purpose.

**Example:**

```asm
RESULT DB ?
TOTAL DW ?
```

The initial contents should not be assumed to be zero.

## Constants

A Constant is a fixed value that does not change during program execution.

The EQU directive is commonly used to define symbolic constants.

**Example:**

```asm
MAX EQU 100
```

The name MAX represents the constant value 100.

## Accessing Variables

Variables can be accessed by using their names in instructions.

**Example:**

```asm
.DATA
    NUM1 DB 5
    NUM2 DB 3

.CODE
    MOV AL, NUM1
    ADD AL, NUM2
```

### Working

1. NUM1 contains 5.
2. NUM2 contains 3.
3. MOV loads NUM1 into AL.
4. ADD adds NUM2 to AL.

**Final Result:**

```text
AL = 8
```

## Data Definition Comparison

| Directive | Full Form | Size |
|---|---|---|
| DB | Define Byte | 8 bits |
| DW | Define Word | 16 bits |
| DD | Define Doubleword | 32 bits |

## Conclusion

Program Data and Variables are used to store information in Assembly Language. Directives such as DB, DW, and DD reserve memory according to the required data size.
