
# Memory Segmentation

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition of Memory Segmentation](#definition-of-memory-segmentation)
- [Purpose of Memory Segmentation](#purpose-of-memory-segmentation)
- [Types of Memory Segments](#types-of-memory-segments)
- [Code Segment](#code-segment)
- [Data Segment](#data-segment)
- [Stack Segment](#stack-segment)
- [Extra Segment](#extra-segment)
- [Segment Size](#segment-size)
- [Physical Address Calculation](#physical-address-calculation)
- [Advantages of Memory Segmentation](#advantages-of-memory-segmentation)
- [Conclusion](#conclusion)

---

## Introduction

Memory Segmentation is a memory management technique used by the Intel 8086 processor.

It divides the memory address space into logical sections called segments.

Each segment can contain up to 64 KB of data or instructions.

Segmentation helps organize programs, data, and stack operations.

## Definition of Memory Segmentation

Memory Segmentation is the process of dividing a computer's memory address space into logical sections called segments.

## Purpose of Memory Segmentation

- Organizes program instructions and data.
- Separates code, data, and stack areas.
- Allows access to a 1 MB physical memory space using 16-bit segment and offset values.
- Supports structured program organization.

## Types of Memory Segments

The Intel 8086 uses four main types of segments:

1. Code Segment
2. Data Segment
3. Stack Segment
4. Extra Segment

## Code Segment

The Code Segment contains the machine instructions of a program.

It is identified by the CS register.

The IP register stores the offset of the next instruction within this segment.

## Data Segment

The Data Segment contains variables and other program data.

It is identified by the DS register.

The CPU uses offsets to access data stored in this segment.

## Stack Segment

The Stack Segment contains temporary data used during program execution.

It is identified by the SS register.

It works with the Stack Pointer (SP) and Base Pointer (BP).

## Extra Segment

The Extra Segment provides an additional data storage area.

It is identified by the ES register.

It is commonly used in string operations as the destination segment.

## Segment Size

Each segment can contain up to 64 KB of memory.

This is because the offset is 16 bits wide.

Calculation:

```text
2¹⁶ = 65,536 Bytes

= 64 KB
```

## Physical Address Calculation

The Intel 8086 calculates the physical address using:

```text
Physical Address = Segment × 10H + Offset
```

### Example

Given:

```text
DS = 2500H
Offset = 0100H
```

Calculation:

```text
2500H × 10H = 25000H

25000H + 0100H = 25100H
```

Physical Address = 25100H

## Advantages of Memory Segmentation

1. **Organization:** Separates program code, data, and stack.
2. **Memory Access:** Allows access to a larger physical memory space.
3. **Program Structure:** Makes programs easier to organize.
4. **Flexible Addressing:** Allows different segment-offset combinations.
5. **Code and Data Separation:** Provides logical separation between instructions and data.

## Conclusion

Memory Segmentation divides memory into logical sections. The Intel 8086 uses Code, Data, Stack, and Extra segments to organize instructions and data while accessing up to 1 MB of physical memory.
