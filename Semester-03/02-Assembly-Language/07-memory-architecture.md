
# Memory Architecture

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition](#definition)
- [Memory Organization](#memory-organization)
- [Types of Computer Memory](#types-of-computer-memory)
- [Primary Memory](#primary-memory)
- [Secondary Memory](#secondary-memory)
- [Memory Address and Location](#memory-address-and-location)
- [Memory Capacity](#memory-capacity)
- [Memory Read and Write Operations](#memory-read-and-write-operations)
- [Conclusion](#conclusion)

---

## Introduction

Memory is an essential part of a computer system.

It stores instructions, data, and processing results so that the CPU can access them when required.

Memory Architecture describes how computer memory is organized, accessed, and managed within a computer system.

## Definition

Memory Architecture is the organization and structure of computer memory, including its types, storage locations, addressing methods, and communication with the CPU.

## Memory Organization

Computer memory is organized into a collection of storage locations.

Each storage location has a unique address that allows the CPU to access its contents.

### Basic Memory Structure

Memory can be represented as a collection of locations:

```text
Address       Data
-------------------
0000          10101010
0001          11001100
0002          11110000
0003          00001111
```

Each address identifies a specific memory location.

## Types of Computer Memory

Computer memory is generally divided into two major categories:

1. Primary Memory
2. Secondary Memory

## Primary Memory

Primary Memory is the main memory that is directly accessible by the CPU.

It stores data and instructions required during computer operation.

### Types of Primary Memory

#### 1. RAM (Random Access Memory)

RAM temporarily stores data and programs currently being used by the CPU.

**Characteristics:**

- It is volatile memory.
- Data is lost when power is turned off.
- It supports both read and write operations.
- It provides fast access to stored information.

**Types of RAM:**

- SRAM (Static RAM)
- DRAM (Dynamic RAM)

#### 2. ROM (Read Only Memory)

ROM stores instructions and data that are retained even when power is turned off.

**Characteristics:**

- It is non-volatile memory.
- It retains data without electrical power.
- It is used to store firmware and startup instructions.

**Types of ROM:**

- PROM
- EPROM
- EEPROM

## Secondary Memory

Secondary Memory is used to store data and programs for long-term use.

It is generally non-volatile and provides larger storage capacity than primary memory.

**Examples:**

- Hard Disk Drive (HDD)
- Solid State Drive (SSD)
- USB Flash Drive
- Optical Discs

## Memory Address and Location

A Memory Address is a unique number used to identify a specific location in memory.

Each memory location stores a fixed amount of data.

For example:

```text
Address 1000 → Data 25
Address 1001 → Data 40
Address 1002 → Data 60
```

The CPU uses memory addresses to read or write information.

## Memory Capacity

Memory Capacity refers to the total amount of data that a memory device can store.

Memory capacity is measured in different units.

| Unit | Equivalent |
|---|---|
| 1 Bit | One binary digit |
| 1 Nibble | 4 Bits |
| 1 Byte | 8 Bits |
| 1 KB | 1024 Bytes |
| 1 MB | 1024 KB |
| 1 GB | 1024 MB |
| 1 TB | 1024 GB |

**Note:** These are traditional binary-based units. The corresponding standardized binary units are KiB, MiB, GiB, and TiB.

## Memory Read and Write Operations

### 1. Read Operation

A Read Operation retrieves data from a memory location.

**Steps:**

1. The CPU places the required address on the address bus.
2. It sends a Read control signal.
3. Memory retrieves the requested data.
4. The data is transferred to the CPU.

### 2. Write Operation

A Write Operation stores data into a memory location.

**Steps:**

1. The CPU places the target address on the address bus.
2. It places the data on the data bus.
3. It sends a Write control signal.
4. Memory stores the data at the specified address.

## Conclusion

Memory Architecture explains how data and instructions are stored and accessed in a computer system. Primary and secondary memory work together to provide temporary and permanent data storage.
