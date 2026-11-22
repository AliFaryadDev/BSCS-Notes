
# Memory Addressing

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition of Memory Addressing](#definition-of-memory-addressing)
- [Memory Address](#memory-address)
- [Offset Address](#offset-address)
- [Segment Address](#segment-address)
- [Physical Address](#physical-address)
- [Physical Address Calculation](#physical-address-calculation)
- [Examples](#examples)
- [Conclusion](#conclusion)

---

## Introduction

Memory Addressing is an important concept in the Intel 8086 microprocessor.

The processor uses memory addresses to identify and access data and instructions stored in memory.

The Intel 8086 uses a segmented memory architecture and a 20-bit address bus to access up to 1 MB of physical memory.

## Definition of Memory Addressing

Memory Addressing is the method used by a processor to identify and access specific locations in memory.

## Memory Address

A Memory Address is a unique value that identifies a particular location in computer memory.

Each memory location in the Intel 8086 is byte-addressable.

This means each address identifies one byte of memory.

## Offset Address

An Offset Address is the displacement of a memory location from the beginning of a segment.

It is a 16-bit value in the Intel 8086.

**Example:**

```text
Offset = 0100H
```

It identifies a location 0100H bytes from the beginning of the selected segment.

## Segment Address

A Segment Address is the value stored in a segment register.

It identifies the starting position of a 64 KB memory segment in the 8086 segmented memory model.

**Examples:**

- CS
- DS
- SS
- ES

## Physical Address

A Physical Address is the actual 20-bit address used to access a location in physical memory.

In Intel 8086, it is calculated using a segment address and an offset address.

## Physical Address Calculation

The physical address is calculated using the following formula:

```text
Physical Address = Segment × 10H + Offset
```

Since multiplying by 10H shifts the segment value four bits to the left, it is equivalent to appending one hexadecimal zero.

## Examples

### Example 1

Given:

```text
Segment = 2000H
Offset  = 1000H
```

Calculation:

```text
2000H × 10H = 20000H

20000H + 1000H = 21000H
```

**Physical Address = 21000H**

### Example 2

Given:

```text
Segment = 1234H
Offset  = 5678H
```

Calculation:

```text
1234H × 10H = 12340H

12340H + 5678H = 179B8H
```

**Physical Address = 179B8H**

## Important Points

- Segment registers contain 16-bit values.
- Offset addresses are 16-bit values.
- Physical addresses are 20-bit values.
- The Intel 8086 can address up to 1 MB of physical memory.
- Different segment-offset combinations can identify the same physical address.

## Conclusion

Memory Addressing allows the Intel 8086 processor to access data and instructions in memory. It uses segment and offset addresses to calculate the actual 20-bit physical address.
