
# RTL of the Instructions

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition of RTL](#definition-of-rtl)
- [RTL Symbols](#rtl-symbols)
- [RTL of Fetch Cycle](#rtl-of-fetch-cycle)
- [RTL of Decode Cycle](#rtl-of-decode-cycle)
- [RTL of Memory Reference Instructions](#rtl-of-memory-reference-instructions)
- [RTL of Register Reference Instructions](#rtl-of-register-reference-instructions)
- [RTL of I/O Instructions](#rtl-of-io-instructions)
- [Importance of RTL](#importance-of-rtl)
- [Conclusion](#conclusion)

---

## Introduction

A computer executes instructions by performing a sequence of operations on registers and memory.

Register Transfer Language (RTL) is used to describe these operations in a symbolic and organized form.

It helps explain how data moves between registers and how operations are performed inside the CPU.

## Definition of RTL

Register Transfer Language (RTL) is a symbolic notation used to describe the transfer of data between registers and the operations performed on that data.

## RTL Symbols

Common RTL symbols include:

| Symbol | Meaning |
|---|---|
| ← | Transfer or assignment |
| + | Addition |
| - | Subtraction |
| AND | Logical AND |
| OR | Logical OR |
| NOT or ' | Complement |
| M[AR] | Memory content at address AR |
| PC | Program Counter |
| AC | Accumulator |
| IR | Instruction Register |
| AR | Address Register |
| DR | Data Register |

## RTL of Fetch Cycle

The Fetch Cycle retrieves an instruction from memory.

### First Timing Step

```text
T0: AR ← PC
```

The address in PC is transferred to AR.

### Second Timing Step

```text
T1: IR ← M[AR]
    PC ← PC + 1
```

The instruction is loaded into IR and PC is incremented.

## RTL of Decode Cycle

During decoding:

```text
T2: D0-D7 ← Decode IR(12-14)
    AR ← IR(0-11)
    I ← IR(15)
```

The opcode is decoded, the address field is transferred to AR, and the indirect bit is identified.

## RTL of Memory Reference Instructions

### 1. AND

```text
AC ← AC AND M[AR]
```

Performs a bitwise AND operation.

### 2. ADD

```text
AC ← AC + M[AR]
E ← Carry
```

Adds memory data to the accumulator.

### 3. LDA

```text
AC ← M[AR]
```

Loads memory data into AC.

### 4. STA

```text
M[AR] ← AC
```

Stores AC into memory.

### 5. BUN

```text
PC ← AR
```

Transfers program execution to the specified address.

### 6. BSA

```text
M[AR] ← PC
AR ← AR + 1
PC ← AR
```

Stores the return address and transfers control to a subroutine.

### 7. ISZ

```text
DR ← M[AR]
DR ← DR + 1
M[AR] ← DR

If DR = 0:
    PC ← PC + 1
```

Increments a memory value and skips the next instruction if the result is zero.

## RTL of Register Reference Instructions

### 1. CLA

```text
AC ← 0
```

Clears the accumulator.

### 2. CLE

```text
E ← 0
```

Clears E.

### 3. CMA

```text
AC ← AC'
```

Complements AC.

### 4. CME

```text
E ← E'
```

Complements E.

### 5. CIR

```text
AC and E ← Circulate Right
```

Rotates AC and E right by one bit.

### 6. CIL

```text
AC and E ← Circulate Left
```

Rotates AC and E left by one bit.

### 7. INC

```text
AC ← AC + 1
```

Increments AC.

### 8. SPA

```text
If AC(15) = 0:
    PC ← PC + 1
```

Skips if AC is positive.

### 9. SNA

```text
If AC(15) = 1:
    PC ← PC + 1
```

Skips if AC is negative.

### 10. SZA

```text
If AC = 0:
    PC ← PC + 1
```

Skips if AC is zero.

### 11. SZE

```text
If E = 0:
    PC ← PC + 1
```

Skips if E is zero.

### 12. HLT

```text
S ← 0
```

Stops computer execution.

## RTL of I/O Instructions

### 1. INP

```text
AC(0-7) ← INPR
FGI ← 0
```

Transfers input data to AC.

### 2. OUT

```text
OUTR ← AC(0-7)
FGO ← 0
```

Transfers data from AC to the output register.

### 3. SKI

```text
If FGI = 1:
    PC ← PC + 1
```

Skips if input is ready.

### 4. SKO

```text
If FGO = 1:
    PC ← PC + 1
```

Skips if output is ready.

### 5. ION

```text
IEN ← 1
```

Enables interrupts.

### 6. IOF

```text
IEN ← 0
```

Disables interrupts.

## Importance of RTL

1. Explains data transfer between registers.
2. Describes internal CPU operations.
3. Helps understand instruction execution.
4. Provides a symbolic representation of hardware operations.
5. Helps in designing and analyzing control units.

## Conclusion

Register Transfer Language describes how data moves between registers and how operations are performed inside a computer. It provides a clear representation of instruction execution and CPU operations.
