
# Intel 8086 Family of Microprocessors

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition of Intel 8086 Family](#definition-of-intel-8086-family)
- [Members of Intel 8086 Family](#members-of-intel-8086-family)
- [Intel 8086](#intel-8086)
- [Intel 8088](#intel-8088)
- [Intel 80186](#intel-80186)
- [Intel 80188](#intel-80188)
- [Intel 80286](#intel-80286)
- [Comparison of Intel 8086 Family](#comparison-of-intel-8086-family)
- [Important Features of Intel 8086](#important-features-of-intel-8086)
- [Applications of Intel 8086 Family](#applications-of-intel-8086-family)
- [Conclusion](#conclusion)

---

## Introduction

Intel 8086 is an important 16-bit microprocessor introduced by Intel in 1978.

It became the foundation of the x86 family of processors.

Intel developed several related processors based on the 8086 architecture. These processors improved processing performance, memory management, and hardware integration.

The major members of the early 8086 family include the 8086, 8088, 80186, 80188, and 80286.

## Definition of Intel 8086 Family

The Intel 8086 Family is a group of microprocessors based on or closely related to the original Intel 8086 architecture.

These processors share important architectural concepts, including 16-bit processing and compatibility with the x86 instruction set.

## Members of Intel 8086 Family

The major processors of this family are:

1. Intel 8086
2. Intel 8088
3. Intel 80186
4. Intel 80188
5. Intel 80286

## Intel 8086

Intel 8086 was introduced in 1978.

It is a 16-bit microprocessor designed for general-purpose computing.

### Important Features

- It is a 16-bit microprocessor.
- It has a 16-bit data bus.
- It has a 20-bit address bus.
- It can address up to 1 MB of physical memory.
- It contains 14 programmer-visible 16-bit registers, including the IP and FLAGS registers.
- It has a 6-byte instruction prefetch queue.
- It uses memory segmentation.
- It supports a maximum clock frequency of 10 MHz in its original family of speed grades.

## Intel 8088

Intel 8088 was introduced in 1979.

It is internally similar to the 8086 but uses an 8-bit external data bus.

### Important Features

- It is internally a 16-bit processor.
- It has an 8-bit external data bus.
- It has a 20-bit address bus.
- It can address up to 1 MB of physical memory.
- It has a 4-byte instruction prefetch queue.
- It was used in the original IBM Personal Computer.

### Difference Between 8086 and 8088

| Intel 8086 | Intel 8088 |
|---|---|
| 16-bit internal processor. | 16-bit internal processor. |
| 16-bit external data bus. | 8-bit external data bus. |
| 20-bit address bus. | 20-bit address bus. |
| 6-byte instruction queue. | 4-byte instruction queue. |
| Higher data transfer capacity per bus transfer. | Lower data transfer capacity per bus transfer. |

## Intel 80186

Intel 80186 was introduced in 1982.

It was an improved version based on the 8086 architecture.

### Important Features

- It is a 16-bit microprocessor.
- It uses a 16-bit external data bus.
- It has a 20-bit address bus.
- It integrates additional system components into the processor.
- It includes an interrupt controller, timer functions, and DMA-related control features.
- It was mainly used in embedded systems and specialized applications.

## Intel 80188

Intel 80188 is closely related to the 80186.

It provides similar internal processing capabilities but uses an 8-bit external data bus.

### Important Features

- It is internally a 16-bit processor.
- It has an 8-bit external data bus.
- It has a 20-bit address bus.
- It integrates additional hardware functions.
- It was used in embedded and control systems.

## Intel 80286

Intel 80286 was introduced in 1982.

It was a more advanced 16-bit processor with improved memory management capabilities.

### Important Features

- It is a 16-bit microprocessor.
- It has a 16-bit data bus.
- It has a 24-bit address bus.
- It can address up to 16 MB of physical memory.
- It introduced Protected Mode.
- It also supports Real Mode for compatibility with earlier processors.
- It provides improved memory protection and multitasking support.

## Comparison of Intel 8086 Family

| Processor | Internal Width | External Data Bus | Address Bus | Physical Memory |
|---|---:|---:|---:|---:|
| 8086 | 16-bit | 16-bit | 20-bit | 1 MB |
| 8088 | 16-bit | 8-bit | 20-bit | 1 MB |
| 80186 | 16-bit | 16-bit | 20-bit | 1 MB |
| 80188 | 16-bit | 8-bit | 20-bit | 1 MB |
| 80286 | 16-bit | 16-bit | 24-bit | 16 MB |

## Important Features of Intel 8086

The Intel 8086 introduced several important features that influenced future processor development.

### 1. 16-Bit Architecture

It can process 16-bit data and uses 16-bit registers.

### 2. 20-Bit Address Bus

It uses a 20-bit address bus to address up to 1 MB of physical memory.

### 3. Memory Segmentation

It divides memory into logical segments such as:

- Code Segment
- Data Segment
- Stack Segment
- Extra Segment

### 4. Instruction Prefetching

It uses a 6-byte instruction queue to fetch upcoming instructions while the Execution Unit processes the current instruction.

### 5. Bus Interface Unit and Execution Unit

The processor is divided into two major units:

- **Bus Interface Unit (BIU):** Fetches instructions and handles memory and I/O bus operations.
- **Execution Unit (EU):** Decodes and executes instructions.

## Applications of Intel 8086 Family

Intel 8086 family processors were used in different computing applications.

**Examples:**

- Personal Computers
- Industrial Control Systems
- Embedded Systems
- Educational Microprocessor Systems
- Automation Systems

## Conclusion

The Intel 8086 family played an important role in the development of microprocessor technology.

Processors such as the 8086, 8088, 80186, 80188, and 80286 introduced improvements in processing, hardware integration, and memory management.

The Intel 8086 became the foundation of the x86 architecture used in later generations of processors.
