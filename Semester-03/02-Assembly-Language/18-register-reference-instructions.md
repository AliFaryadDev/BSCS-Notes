
# Register Reference Instructions

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition](#definition)
- [Characteristics](#characteristics)
- [Types of Register Reference Instructions](#types-of-register-reference-instructions)
- [CLA Instruction](#cla-instruction)
- [CLE Instruction](#cle-instruction)
- [CMA Instruction](#cma-instruction)
- [CME Instruction](#cme-instruction)
- [CIR Instruction](#cir-instruction)
- [CIL Instruction](#cil-instruction)
- [INC Instruction](#inc-instruction)
- [SPA Instruction](#spa-instruction)
- [SNA Instruction](#sna-instruction)
- [SZA Instruction](#sza-instruction)
- [SZE Instruction](#sze-instruction)
- [HLT Instruction](#hlt-instruction)
- [Conclusion](#conclusion)

---

## Introduction

Register Reference Instructions perform operations directly on CPU registers without accessing memory for an operand.

In Mano's Basic Computer, these instructions mainly operate on the Accumulator (AC) and the E flip-flop.

They are used for clearing, complementing, shifting, incrementing, and testing register contents.

## Definition

Register Reference Instructions are instructions that perform operations directly on processor registers or control the processor without requiring a memory operand.

## Characteristics

- Operate directly on CPU registers.
- Do not require a memory operand.
- Perform register manipulation and testing.
- Are part of Mano's Basic Computer instruction set.

## Types of Register Reference Instructions

Mano's Basic Computer has twelve register reference instructions.

### 1. CLA — Clear Accumulator

Clears the contents of the accumulator.

**Operation:**

```text
AC ← 0
```

### 2. CLE — Clear E

Clears the E flip-flop.

**Operation:**

```text
E ← 0
```

### 3. CMA — Complement Accumulator

Complements every bit of the accumulator.

**Operation:**

```text
AC ← AC'
```

Example:

```text
Before: 1010
After:  0101
```

### 4. CME — Complement E

Complements the E flip-flop.

**Operation:**

```text
E ← E'
```

### 5. CIR — Circulate Right

Rotates the accumulator and E flip-flop one bit to the right.

**Operation:**

```text
AC and E ← Rotate Right
```

The least significant bit of AC moves into E, and the previous E moves into the most significant bit of AC.

### 6. CIL — Circulate Left

Rotates the accumulator and E flip-flop one bit to the left.

**Operation:**

```text
AC and E ← Rotate Left
```

The most significant bit of AC moves into E, and the previous E moves into the least significant bit of AC.

### 7. INC — Increment Accumulator

Increases the accumulator by one.

**Operation:**

```text
AC ← AC + 1
```

### 8. SPA — Skip if Positive AC

Skips the next instruction if the accumulator contains a positive value.

**Operation:**

```text
If AC(15) = 0:
    PC ← PC + 1
```

### 9. SNA — Skip if Negative AC

Skips the next instruction if the accumulator contains a negative value.

**Operation:**

```text
If AC(15) = 1:
    PC ← PC + 1
```

### 10. SZA — Skip if Zero AC

Skips the next instruction if the accumulator contains zero.

**Operation:**

```text
If AC = 0:
    PC ← PC + 1
```

### 11. SZE — Skip if E is Zero

Skips the next instruction if E is zero.

**Operation:**

```text
If E = 0:
    PC ← PC + 1
```

### 12. HLT — Halt

Stops the execution of the Basic Computer.

**Operation:**

```text
S ← 0
```

Here, S represents the run control flip-flop.

## Conclusion

Register Reference Instructions perform operations directly on CPU registers. They are used for clearing, complementing, rotating, incrementing, testing register values, and stopping processor execution.
