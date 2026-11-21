# Registers and Their Categories

**Subject: Computer Organization and Assembly Language** | **Course: CC-210**

## 📄 Important Points

- [Introduction](#introduction)
- [Definition](#definition)
- [Characteristics](#characteristics)
- [Purpose of Registers](#purpose-of-registers)
- [Classification of Register](#classification-of-register)
- [Intel 8086 Register Organization](#intel-8086-register-organization)
- [16-bit and 8-bit Register Structure](#16-bit-and-8-bit-register-structure)
- [High and Low Byte Registers](#high-and-low-byte-registers)
- [Register Naming and Classification](#register-naming-and-classification)
- [Registers vs Cache Memory vs RAM](#registers-vs-cache-memory-vs-ram)
- [Conclusion](#conclusion)

## Introduction
Registers are small, high-speed storage locations inside the CPU.
They temporarily hold data, instructions, memory addresses, and intermediate results during program execution.

## Definition
> A register is a small storage unit within the CPU, designed to hold a specific amount of binary data for processing.

## Characteristics 
### Physical Characteristics
1. **Location:** Registers are located inside the CPU.
<br>
2. **Small Storage Capacity:** Registers can hold only a small amount of data such as 8 bits, 16 bits, 32 bits, or 64 bits, depending on the CPU architecture.
<br>
3. **Fixed Size:** Each register has a specific size, such as 8-bit, 16-bit, 32-bit, or 64-bit.

### Functional Characteristics
1. **High Speed:** Registers provide extremely fast access to data.
<br>
2. **Temporary Storage:** Registers hold data temporarily during processing.

**Mini Note**
<br>
> Registers can hold, update, and replace data very quickly during CPU processing.
<br>
**For Example:** A register may hold 10, then 15, and then 13 as calculations are performed. That's why they are called temporary storage units.

## Purpose of Registers

Registers are used to:

1. **Store Data:** Temporarily hold data required by the CPU.
2. **Store Instructions:** Hold instructions during processing.
3. **Store Memory Addresses:** Hold addresses used to access data in memory.
4. **Hold Intermediate Results:** Store temporary results during calculations.

## Classification of Register
1. **General Purpose Registers (GPRs)**

> **Definition:**<br> General Purpose Registers are a group of CPU registers in the 8086 microprocessor, classified into three categories: Data Registers, Pointer Registers, and Index Registers.
- [Data Register](#data-register)
- [Pointer Registers](#pointer-register)
- [Index Registers](#index-register)

2. **Special Purpose Registers (SPRs)**
> **Definition:**<br> Special Purpose Registers are a group of CPU registers in the 8086 microprocessor, used to control program execution, manage memory segments, and store the status of CPU operations.
 - [Segment Registers](#segment-register)
 - [Instruction Pointer (IP)](#instruction-pointer-(IP))
 - [Flag Register (FLAGS)](#flag-register-(flags)) <br>

___

### General Purpose Register
___

### Data Register

 **Defintion:**<br>
> Data Registers are a category of General Purpose Registers (GPRs) in the 8086 microprocessor, used to store data and perform arithmetic and logical operations.

**Types:** 
1. AX (Accumulator Register)
2. BX (Base Register)
3. CX (Count Register)
4. DX (Data Register)

**Functions:**
- **AX:**
  Used in arithmetic operations and storing intermediate results.
- **BX:**
Used to store base addresses and support memory addressing.
- **CX:**
Used as a counter in loop and shift operations.
- **DX:**
Used in multiplication, division and I/O operations.

**Features:**

- Each data register is a **16-bit register**.
- Each data register is divided into two **8-bit parts**:

  - **AX** = AH (Upper 8-bit) + AL (Lower 8-bit)
  - **BX** = BH (Upper 8-bit) + BL (Lower 8-bit)
  - **CX** = CH (Upper 8-bit) + CL (Lower 8-bit)
  - **DX** = DH (Upper 8-bit) + DL (Lower 8-bit)

> **Note:** Register names indicate their special purposes, not their complete limitations. The upper 8-bit part of AX is called **AH**, and the lower 8-bit part is called **AL**.



### Pointer Register

 **Defintion:**<br>
> Pointer Registers are a category of General Purpose Registers (GPRs) in the 8086 microprocessor, used to store offsets of memory locations in the stack segment and access stack data.

**Types:**<br><br>
8086 microprocessor has two Pointer Registers:
1. SP (Stack Pointer)
2. BP (Base Pointer)

**Functions:**<br>
- **SP:** Used to store the offset address of the current top of the stack and update its value during PUSH and POP operations.
- **BP:** Used to store a reference offset to access data, function parameters, and local variables in the stack segment.

 > PUSH / POP = SP changes.

**Features:** 

- Both Pointer Registers are **16-bit registers**.
- 8086 has two Pointer Registers:
  - **SP (Stack Pointer)**
  - **BP (Base Pointer)**
- Both are used to access data in the **Stack Segment (SS)**.
- SP is updated during PUSH and POP operations.

> **Note:** PUSH and POP operations update SP. BP normally remains unchanged during these operations.

### Index Register
**Definition:**

> Index Registers are a category of General Purpose Registers (GPRs) in the 8086 microprocessor, used to store offset addresses of source and destination data in memory.

**Types:**<br>

8086 microprocessor mein 2 Index Registers hote hain:

1. **SI (Source Index):** Stores the offset address of source data in memory.
2. **DI (Destination Index):** Stores the offset address of destination data in memory.

**Functions:**

- **SI (Source Index):** Holds the offset address of source data to access data from memory.
- **DI (Destination Index):** Holds the offset address of destination memory to store data.

**Example:**
- SI identifies where data is located.
- DI identifies where data needs to be stored.

**Features:**

- Both Index Registers are **16-bit registers**.
- 8086 has two Index Registers:
  - **SI (Source Index)**
  - **DI (Destination Index)**
- Both registers store **offset addresses** of memory locations.
- SI is commonly associated with the **Data Segment (DS)**.
- DI is commonly associated with the **Extra Segment (ES)**.
- Both are used in **indexed addressing and string operations**.

**Note:**
> - **DS:SI** is commonly used to access source data.
> - **ES:DI** is commonly used to access destination data.
> - SI and DI store offset addresses, while DS and ES identify memory segments.

___

### Special Purpose Register

___

### Segment Register
**Definition:**

> Segment Registers are a category of Special Purpose Registers in the 8086 microprocessor, used to hold the starting addresses of memory segments.

**Types:**

8086 microprocessor has four Segment Registers:

1. **CS (Code Segment):** Holds the starting address of the code segment.
2. **DS (Data Segment):** Holds the starting address of the data segment.
3. **SS (Stack Segment):** Holds the starting address of the stack segment.
4. **ES (Extra Segment):** Holds the starting address of the extra segment.

**Functions:**

- **CS (Code Segment):** Used to access program instructions stored in memory.
- **DS (Data Segment):** Used to access program data stored in memory.
- **SS (Stack Segment):** Used to access data stored in the stack.
- **ES (Extra Segment):** Used as an additional segment, commonly for destination data in string operations.

**Features:**

- All four Segment Registers are **16-bit registers**.
- Each Segment Register holds the starting address of a memory segment.
- 8086 supports four Segment Registers: CS, DS, SS, and ES.
- Each segment can address up to **64 KB of memory**.
- Segment Registers work with offset addresses to access memory locations.

**Note:**

> - Segment Registers store the starting address of memory segments.
> - Offset addresses identify specific locations within those segments.
> - The CPU combines a segment address and an offset address to calculate the physical memory address.

### Instruction Pointer
