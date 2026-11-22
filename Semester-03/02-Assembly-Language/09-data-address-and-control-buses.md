
# Data, Address and Control Buses

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition of Bus](#definition-of-bus)
- [Types of System Buses](#types-of-system-buses)
- [Data Bus](#data-bus)
- [Address Bus](#address-bus)
- [Control Bus](#control-bus)
- [Comparison of System Buses](#comparison-of-system-buses)
- [Working of System Buses](#working-of-system-buses)
- [Bus Width](#bus-width)
- [Conclusion](#conclusion)

---

## Introduction

A computer system contains different components such as the CPU, memory, and input/output devices.

These components need to communicate with each other to transfer data, addresses, and control signals.

A Bus provides the communication pathway between these components.

## Definition of Bus

A Bus is a communication pathway that transfers data, addresses, and control signals between different components of a computer system.

## Types of System Buses

A System Bus consists of three main types:

1. Data Bus
2. Address Bus
3. Control Bus

## Data Bus

The Data Bus is used to transfer actual data between the CPU, memory, and input/output devices.

### Characteristics

- It carries actual data and instructions.
- It is generally bidirectional.
- Its width determines how many bits can be transferred at one time.
- A wider data bus can transfer more bits in a single transfer.

### Example

If a processor has a 16-bit data bus, it can transfer 16 bits of data in one bus transfer.

## Address Bus

The Address Bus carries the address of the memory location or input/output device that the CPU wants to access.

### Characteristics

- It carries memory or I/O addresses.
- It is generally unidirectional from the CPU.
- Its width determines the addressable range.
- A wider address bus can identify more locations.

### Example

The Intel 8086 has a 20-bit address bus.

Its maximum addressable physical memory space is:

```text
2²⁰ = 1,048,576 Bytes

= 1 MB
```

## Control Bus

The Control Bus carries control and timing signals between the CPU, memory, and input/output devices.

It coordinates different operations of a computer system.

### Common Control Signals

#### 1. Read Signal

It indicates that the CPU wants to read data from memory or an I/O device.

#### 2. Write Signal

It indicates that the CPU wants to write data into memory or an I/O device.

#### 3. Interrupt Signal

It is used to request the CPU's attention from another device.

#### 4. Clock Signal

It provides timing information to synchronize operations.

#### 5. Reset Signal

It initializes the processor or system when activated.

## Comparison of System Buses

| Data Bus | Address Bus | Control Bus |
|---|---|---|
| Transfers data. | Transfers addresses. | Transfers control signals. |
| Generally bidirectional. | Generally unidirectional from CPU. | Direction depends on the signal. |
| Width determines data transferred at once. | Width determines addressable range. | Coordinates system operations. |

## Working of System Buses

System buses work together to perform memory operations.

### Example: Memory Read Operation

Suppose the CPU wants to read data from memory address 1000.

**Step 1 — Address Bus:**

The CPU sends address 1000 to memory.

**Step 2 — Control Bus:**

The CPU sends a Read signal.

**Step 3 — Data Bus:**

Memory sends the requested data to the CPU.

### Example: Memory Write Operation

Suppose the CPU wants to store value 25 at memory address 1000.

**Step 1 — Address Bus:**

The CPU sends address 1000.

**Step 2 — Data Bus:**

The CPU sends value 25.

**Step 3 — Control Bus:**

The CPU sends a Write signal.

**Result:**

Memory stores value 25 at address 1000.

## Bus Width

Bus Width refers to the number of bits that a bus can carry or represent at one time.

### Types

1. **Data Bus Width:** Determines the number of data bits transferred in one bus transfer.
2. **Address Bus Width:** Determines the number of unique addresses that can be represented.

### Example

The Intel 8086 processor has:

- 16-bit Data Bus
- 20-bit Address Bus

Therefore, it can transfer 16 bits of data in one bus transfer and address up to 1 MB of physical memory.

## Conclusion

Data, Address, and Control Buses provide communication between the CPU, memory, and I/O devices. The Data Bus transfers information, the Address Bus identifies locations, and the Control Bus coordinates operations.
