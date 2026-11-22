
# Complete Flowchart for Basic Computer Operation

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition of Flowchart](#definition-of-flowchart)
- [Basic Steps of Computer Operation](#basic-steps-of-computer-operation)
- [Fetch Cycle](#fetch-cycle)
- [Decode Cycle](#decode-cycle)
- [Indirect Address Cycle](#indirect-address-cycle)
- [Execute Cycle](#execute-cycle)
- [Interrupt Cycle](#interrupt-cycle)
- [Complete Flowchart](#complete-flowchart)
- [Conclusion](#conclusion)

---

## Introduction

A Basic Computer performs operations by executing instructions stored in memory.

The Control Unit manages the sequence of operations required to execute each instruction.

A flowchart provides a visual representation of this process.

## Definition of Flowchart

A Flowchart is a graphical representation of a process or sequence of operations using standard symbols and connecting arrows.

## Basic Steps of Computer Operation

The basic computer operation consists of:

1. Fetch Cycle
2. Decode Cycle
3. Indirect Address Cycle (when required)
4. Execute Cycle
5. Interrupt Cycle (when an interrupt is pending and enabled)

## Fetch Cycle

The CPU retrieves the next instruction from memory.

```text
AR ← PC
IR ← M[AR]
PC ← PC + 1
```

## Decode Cycle

The Control Unit identifies the instruction operation.

```text
D0-D7 ← Decode IR(12-14)
AR ← IR(0-11)
I ← IR(15)
```

## Indirect Address Cycle

If indirect addressing is selected for a memory reference instruction, the CPU obtains the effective address from memory.

```text
AR ← M[AR]
```

## Execute Cycle

The CPU performs the operation specified by the decoded instruction.

Examples:

- ADD: Adds memory data to AC.
- LDA: Loads memory data into AC.
- STA: Stores AC into memory.
- BUN: Changes the program sequence.
- INP: Receives input data.

## Interrupt Cycle

An interrupt cycle occurs when an enabled interrupt request is pending.

The CPU saves the return address and transfers control to the interrupt service routine.

In Mano's Basic Computer, the interrupt cycle is initiated when the interrupt enable flip-flop is set and an input or output flag indicates a request.

## Complete Flowchart

```text
          START
            |
            v
      FETCH INSTRUCTION
            |
            v
      DECODE INSTRUCTION
            |
            v
    Is it a Memory Reference?
          /       \
        YES        NO
         |          |
         v          v
   Indirect Mode?  Decode Register
      /    \       or I/O Instruction
    YES     NO          |
     |       |          |
     v       |          |
GET EFFECTIVE ADDRESS   |
     |       |          |
     +-------+----------+
             |
             v
      EXECUTE INSTRUCTION
             |
             v
       Is HLT Executed?
          /       \
        YES        NO
         |          |
         v          v
        STOP    Interrupt Pending?
                   /    \
                 YES     NO
                  |       |
                  v       |
             INTERRUPT    |
               CYCLE       |
                  |        |
                  +--------+
                      |
                      v
                FETCH NEXT
                INSTRUCTION
```

## Conclusion

The flowchart of a Basic Computer explains the complete instruction execution process. It shows how the CPU fetches, decodes, and executes instructions, handles indirect addressing, and responds to interrupts.
