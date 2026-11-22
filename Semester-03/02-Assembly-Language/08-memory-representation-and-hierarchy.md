
# Memory Representation and Hierarchy

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Memory Representation](#memory-representation)
- [Binary Number System](#binary-number-system)
- [Bit and Byte Representation](#bit-and-byte-representation)
- [Character Representation](#character-representation)
- [Memory Hierarchy](#memory-hierarchy)
- [Levels of Memory Hierarchy](#levels-of-memory-hierarchy)
- [Comparison of Memory Levels](#comparison-of-memory-levels)
- [Importance of Memory Hierarchy](#importance-of-memory-hierarchy)
- [Conclusion](#conclusion)

---

## Introduction

A computer stores all data and instructions in digital form.

Memory Representation explains how data is represented and stored inside computer memory.

Memory Hierarchy describes the arrangement of different types of memory according to their speed, cost, and storage capacity.

## Memory Representation

Memory Representation is the method of storing data and instructions in computer memory using binary digits (0 and 1).

Computers use binary representation because their electronic circuits operate using two basic states.

- 0 represents a LOW or OFF state.
- 1 represents a HIGH or ON state.

## Binary Number System

The Binary Number System is a number system that uses only two digits: 0 and 1.

It has a base of 2.

### Example

```text
Decimal Number: 10

Binary Representation: 1010
```

The binary number 1010 represents decimal number 10.

### Binary Conversion

Each binary digit has a positional value based on powers of 2.

```text
Binary: 1010

1 × 2³ = 8
0 × 2² = 0
1 × 2¹ = 2
0 × 2⁰ = 0

Total = 10
```

## Bit and Byte Representation

Computer memory stores information using bits and bytes.

### 1. Bit

A Bit is the smallest unit of computer data.

It can contain only one of two values:

- 0
- 1

### 2. Nibble

A Nibble is a group of 4 bits.

**Example:**

```text
1010
```

### 3. Byte

A Byte is a group of 8 bits.

**Example:**

```text
10101010
```

A byte is commonly used to represent a character or a small integer.

### 4. Word

A Word is a group of bits processed as a unit by a processor.

The word size depends on the processor architecture.

**Examples:**

- 16-bit processor: 16-bit word
- 32-bit processor: 32-bit word
- 64-bit processor: 64-bit word

## Character Representation

Computers represent characters using binary codes.

Each character is assigned a numeric code that can be stored in memory.

### 1. ASCII

ASCII stands for American Standard Code for Information Interchange.

It is a character encoding standard that represents English letters, digits, and symbols.

Standard ASCII uses 7 bits and represents 128 characters.

**Examples:**

| Character | Decimal Code |
|---|---:|
| A | 65 |
| B | 66 |
| a | 97 |
| 0 | 48 |
| Space | 32 |

### 2. Unicode

Unicode is a universal character standard designed to represent characters from different languages and writing systems.

It supports many languages, symbols, and special characters.

Common Unicode encoding formats include:

- UTF-8
- UTF-16
- UTF-32

## Memory Hierarchy

Memory Hierarchy is the arrangement of computer memory into different levels according to speed, cost, capacity, and closeness to the CPU.

The fastest memory is generally closest to the CPU, while slower and larger storage is placed at lower levels.

## Levels of Memory Hierarchy

### 1. Registers

Registers are the fastest storage locations inside the CPU.

**Characteristics:**

- Extremely fast access.
- Very small storage capacity.
- Used to store operands, addresses, and results.

### 2. Cache Memory

Cache Memory is a small, high-speed memory that stores frequently accessed data and instructions.

It reduces the average time required by the CPU to access memory.

**Levels of Cache:**

- L1 Cache
- L2 Cache
- L3 Cache

### 3. Main Memory

Main Memory, commonly called RAM, stores programs and data currently being used by the computer.

It has more capacity than cache but is generally slower.

### 4. Secondary Storage

Secondary Storage provides long-term storage for programs, files, and data.

**Examples:**

- HDD
- SSD
- USB Drive

## Memory Hierarchy Diagram

```text
       Fastest
          |
       Registers
          |
       L1 Cache
          |
       L2 Cache
          |
       L3 Cache
          |
      Main Memory
         (RAM)
          |
    Secondary Storage
       (SSD/HDD)
          |
       Slowest
```

## Comparison of Memory Levels

| Memory Type | Speed | Capacity |
|---|---|---|
| Registers | Very High | Very Small |
| Cache | High | Small |
| RAM | Moderate | Large |
| SSD/HDD | Lower | Very Large |

## Importance of Memory Hierarchy

1. **Improved Performance:** Frequently used data can be accessed quickly.
2. **Cost Efficiency:** Expensive high-speed memory is used in smaller amounts.
3. **Large Storage:** Secondary storage provides large storage capacity.
4. **Efficient Processing:** Different memory levels work together to reduce data access time.

## Conclusion

Memory Representation explains how computers store data using binary digits. Memory Hierarchy organizes different memory types according to their speed, capacity, and cost to improve overall computer performance.
