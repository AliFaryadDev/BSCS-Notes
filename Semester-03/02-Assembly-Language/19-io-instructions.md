
# I/O Instructions

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition](#definition)
- [Input and Output Operations](#input-and-output-operations)
- [Types of I/O Instructions](#types-of-io-instructions)
- [INP Instruction](#inp-instruction)
- [OUT Instruction](#out-instruction)
- [SKI Instruction](#ski-instruction)
- [SKO Instruction](#sko-instruction)
- [ION Instruction](#ion-instruction)
- [IOF Instruction](#iof-instruction)
- [I/O Flags](#io-flags)
- [Conclusion](#conclusion)

---

## Introduction

Input/Output (I/O) Instructions allow a computer to communicate with external devices.

These instructions transfer data between the processor and input/output devices.

In Mano's Basic Computer, I/O instructions mainly use the Input Register (INPR), Output Register (OUTR), and associated control flags.

## Definition

I/O Instructions are machine instructions used to transfer data between the CPU and external input/output devices and control I/O operations.

## Input and Output Operations

### Input Operation

An input operation transfers data from an external device to the computer.

**Examples:**
- Keyboard
- Input terminals
- Sensors

### Output Operation

An output operation transfers data from the computer to an external device.

**Examples:**
- Monitor
- Printer
- Display devices

## Types of I/O Instructions

Mano's Basic Computer has six I/O instructions:

1. INP
2. OUT
3. SKI
4. SKO
5. ION
6. IOF

## INP Instruction

INP stands for Input.

It transfers an 8-bit character from the Input Register to the lower 8 bits of the Accumulator.

**Operation:**

```text
AC(0-7) ← INPR
FGI ← 0
```

Here, FGI is the input flag.

## OUT Instruction

OUT stands for Output.

It transfers the lower 8 bits of the Accumulator to the Output Register.

**Operation:**

```text
OUTR ← AC(0-7)
FGO ← 0
```

Here, FGO is the output flag.

## SKI Instruction

SKI stands for Skip on Input Flag.

It skips the next instruction if the input flag is set.

**Operation:**

```text
If FGI = 1:
    PC ← PC + 1
```

## SKO Instruction

SKO stands for Skip on Output Flag.

It skips the next instruction if the output flag is set.

**Operation:**

```text
If FGO = 1:
    PC ← PC + 1
```

## ION Instruction

ION stands for Interrupt On.

It enables the interrupt system.

**Operation:**

```text
IEN ← 1
```

## IOF Instruction

IOF stands for Interrupt Off.

It disables the interrupt system.

**Operation:**

```text
IEN ← 0
```

## I/O Flags

### 1. FGI — Input Flag

Indicates whether input data is available in the input register.

### 2. FGO — Output Flag

Indicates whether the output device is ready to receive new data.

### 3. IEN — Interrupt Enable Flag

Controls whether interrupts are enabled or disabled.

## Conclusion

I/O Instructions provide communication between the processor and external devices. They allow input, output, device status checking, and interrupt control.
