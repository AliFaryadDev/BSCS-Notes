
# Instruction Cycle, Timing and Decoding

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Instruction Cycle](#instruction-cycle)
- [Timing and Control](#timing-and-control)
- [Timing Signals](#timing-signals)
- [Instruction Decoding](#instruction-decoding)
- [Instruction Cycle Phases](#instruction-cycle-phases)
- [Timing Sequence](#timing-sequence)
- [Example of Instruction Execution](#example-of-instruction-execution)
- [Conclusion](#conclusion)

---

## Introduction

The CPU executes instructions through a sequence of operations called the Instruction Cycle.

Each operation requires specific timing signals and control signals.

Instruction decoding identifies the operation to be performed, while timing and control coordinate the execution of each step.

## Instruction Cycle

The Instruction Cycle is the complete sequence of operations performed by the CPU to fetch, decode, and execute an instruction.

The main phases are:

1. Fetch
2. Decode
3. Execute

## Timing and Control

Timing and Control coordinate the operations of different computer components.

They ensure that each operation occurs at the correct time and in the correct sequence.

The Control Unit generates control signals according to the instruction being executed.

## Timing Signals

In Mano's Basic Computer, a sequence counter (SC) and a timing decoder generate timing signals.

The timing signals are represented as:

```text
T0, T1, T2, T3, T4, T5 ...
```

Each timing signal represents a specific step in instruction execution.

## Instruction Decoding

Instruction Decoding is the process of interpreting an instruction to determine which operation must be performed.

In Mano's Basic Computer, the Instruction Register (IR) contains the instruction.

The opcode is decoded to identify the required operation.

### Main Components

- Instruction Register (IR)
- Instruction Decoder
- Control Logic
- Timing Decoder

## Instruction Cycle Phases

### 1. Fetch Phase

The CPU retrieves the instruction from memory.

Typical register transfer operations:

```text
T0: AR ← PC
T1: IR ← M[AR], PC ← PC + 1
```

### 2. Decode Phase

The Control Unit decodes the instruction.

```text
T2: D0-D7 ← Decode IR(12-14)
    AR ← IR(0-11)
    I  ← IR(15)
```

The opcode is decoded, the address field is transferred to AR, and the indirect bit is identified.

### 3. Indirect Address Phase

If indirect addressing is used for a memory reference instruction, the effective address is obtained from memory.

```text
T3: AR ← M[AR]
```

This step is conditional and is not required for direct addressing.

### 4. Execute Phase

The CPU performs the operation specified by the instruction.

For example, an ADD instruction performs:

```text
AC ← AC + M[AR]
```

The exact timing depends on the instruction.

## Timing Sequence

A simplified timing sequence is:

```text
T0 → T1 → T2 → T3 → T4 → T5
```

Not every instruction requires all timing steps.

After the instruction is completed, the sequence counter is cleared to begin the next instruction cycle.

## Example of Instruction Execution

Consider the instruction:

```text
ADD 500
```

The CPU performs the following operations:

1. Fetches the ADD instruction from memory.
2. Decodes the ADD opcode.
3. Identifies the memory address.
4. Retrieves the operand from memory.
5. Adds the operand to the accumulator.
6. Stores the result in AC.

## Conclusion

Instruction Cycle, Timing, and Decoding explain how the CPU fetches, interprets, and executes instructions. Timing signals coordinate the operations, while the decoder identifies the required instruction.
