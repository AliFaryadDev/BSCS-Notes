
# Real Mode Memory Structure

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition of Real Mode](#definition-of-real-mode)
- [Memory Capacity](#memory-capacity)
- [Segment and Offset Addressing](#segment-and-offset-addressing)
- [Memory Segments](#memory-segments)
- [Physical Address Calculation](#physical-address-calculation)
- [Characteristics of Real Mode](#characteristics-of-real-mode)
- [Memory Overlapping](#memory-overlapping)
- [Conclusion](#conclusion)

---

## Introduction

Real Mode is the basic operating mode of the Intel 8086 processor.

It uses a segmented memory structure in which memory is accessed through segment and offset addresses.

Real Mode allows the processor to address up to 1 MB of physical memory.

## Definition of Real Mode

Real Mode is a processor operating mode in which memory is accessed using 16-bit segment and offset addresses to generate 20-bit physical addresses.

## Memory Capacity

The Intel 8086 has a 20-bit address bus.

Therefore, its maximum physical memory address space is:

```text
2²⁰ = 1,048,576 Bytes

= 1 MB
```

The address range is:

```text
00000H to FFFFFH
```

## Segment and Offset Addressing

In Real Mode, a memory address consists of two parts:

1. Segment Address
2. Offset Address

The segment address identifies the starting position of a segment.

The offset identifies a location within that segment.

### Example

```text
CS = 2000H
IP = 0100H
```

The physical address is calculated as:

```text
2000H × 10H = 20000H

20000H + 0100H = 20100H
```

Physical Address = 20100H

## Memory Segments

The Intel 8086 uses four main segment registers:

### 1. Code Segment (CS)

Contains program instructions.

### 2. Data Segment (DS)

Contains program data and variables.

### 3. Stack Segment (SS)

Contains stack data used during program execution.

### 4. Extra Segment (ES)

Provides an additional data segment.

## Physical Address Calculation

The physical address is calculated using:

```text
Physical Address = Segment × 10H + Offset
```

### Example

Given:

```text
DS = 3000H
Offset = 0200H
```

Calculation:

```text
3000H × 10H = 30000H

30000H + 0200H = 30200H
```

Physical Address = 30200H

## Characteristics of Real Mode

1. **20-Bit Addressing:** It uses 20-bit physical addresses.
2. **1 MB Memory Space:** It can address up to 1 MB of physical memory.
3. **Segmented Memory:** Memory is accessed using segment and offset addresses.
4. **16-Bit Registers:** Segment and offset values are 16 bits wide.
5. **No Hardware Memory Protection:** Real Mode does not provide protected-mode memory isolation.
6. **Compatibility:** It supports the basic 8086 programming environment.

## Memory Overlapping

Memory Overlapping occurs when two or more segment-offset combinations generate the same physical memory address.

This happens because segments can begin at addresses separated by 16 bytes while their offset ranges may overlap.

### Example

First Address:

```text
Segment = 1000H
Offset  = 0020H

Physical Address = 10020H
```

Second Address:

```text
Segment = 1001H
Offset  = 0010H

Physical Address = 10020H
```

Both combinations access the same physical memory location.

## Conclusion

Real Mode is the basic operating mode of the Intel 8086. It uses segmented memory addressing and allows access to 1 MB of physical memory through 16-bit segment and offset values.
