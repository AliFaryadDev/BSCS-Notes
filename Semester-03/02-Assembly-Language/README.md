
# Computer Organization & Assembly Language

**Course Code:** CC-210  
**Credit Hours:** 3 (2,1)  
**Category:** Computing Core  
**Prerequisite:** CC-110 — Digital Logic Design  
**Co-Requisite:** None  
**Follow-up:** None

---

## Table of Contents

- [Course Introduction](#course-introduction)
- [Course Learning Outcomes (CLOs)](#course-learning-outcomes-clos)
- [Course Description](#course-description)
  - [01 — Introduction to Computer Systems](#01--introduction-to-computer-systems)
  - [02 — Evolution of Intel Microprocessor](#02--evolution-of-intel-microprocessor)
  - [03 — Introduction to Assembly Language](#03--introduction-to-assembly-language)
  - [04 — Computer Organization](#04--computer-organization)
  - [05 — Instruction Cycle](#05--instruction-cycle)
  - [06 — Memory Architecture](#06--memory-architecture)
  - [07 — Memory Representation & Hierarchy](#07--memory-representation--hierarchy)
  - [08 — Data, Address and Control Buses](#08--data-address-and-control-buses)
  - [09 — Intel 8086 Family of Microprocessors](#09--intel-8086-family-of-microprocessors)
  - [10 — Organization of Intel 8088/8086 Processor](#10--organization-of-intel-80888086-processor)
  - [11 — Registers and Their Categories](#11--registers-and-their-categories)
  - [12 — Functions of Registers](#12--functions-of-registers)
  - [13 — Memory Addressing](#13--memory-addressing)
  - [14 — Real Mode Memory Structure](#14--real-mode-memory-structure)
  - [15 — Memory Segmentation](#15--memory-segmentation)
  - [16 — Basic Computer Instructions](#16--basic-computer-instructions)
  - [17 — Addressing Modes](#17--addressing-modes)
  - [18 — Instruction Timing and Decoding](#18--instruction-timing-and-decoding)
  - [19 — RTL of Instructions](#19--rtl-of-instructions)
  - [20 — Basic Computer Operation Flowchart](#20--basic-computer-operation-flowchart)
  - [21 — Design of CPU](#21--design-of-cpu)
  - [22 — Assembly Language Syntax](#22--assembly-language-syntax)
  - [23 — Program Data and Variables](#23--program-data-and-variables)
  - [24 — Program Structure](#24--program-structure)
  - [25 — Memory Models](#25--memory-models)
  - [26 — Data, Stack and Code Segments](#26--data-stack-and-code-segments)
  - [27 — Variants of MOV Instruction](#27--variants-of-mov-instruction)
  - [28 — Basic Instructions](#28--basic-instructions)
  - [29 — Processor Status and Flags Register](#29--processor-status-and-flags-register)
  - [30 — Flow Control Instructions](#30--flow-control-instructions)
  - [31 — Jump Instructions](#31--jump-instructions)
  - [32 — Looping Structures](#32--looping-structures)
  - [33 — Logic Instructions](#33--logic-instructions)
  - [34 — Shift and Rotate Instructions](#34--shift-and-rotate-instructions)
  - [35 — Number Input and Output Procedures](#35--number-input-and-output-procedures)
  - [36 — Stack, PUSH and POP](#36--stack-push-and-pop)
  - [37 — CALL and RET Instructions](#37--call-and-ret-instructions)
  - [38 — MUL and DIV Instructions](#38--mul-and-div-instructions)
  - [39 — Related Programming Examples](#39--related-programming-examples)
  - [40 — XLAT Instruction](#40--xlat-instruction)
  - [41 — String Instructions](#41--string-instructions)
  - [42 — File Operations](#42--file-operations)
- [Textbooks](#textbooks)
- [Reference Material](#reference-material)

---

## Course Introduction

The main objective of this course is to introduce the organization of computer systems and usage of assembly language for optimization and control.

Emphasis is placed on exposing the low-level logic employed for problem solving while using assembly language as a tool.

At the end of the course, students should be capable of writing moderately complex assembly language subroutines and interfacing them with any high-level language.

## Course Learning Outcomes (CLOs)

At the end of this course, students will be able to:

| CLO | Learning Outcome | BT | PLO |
|---|---|---|---|
| CLO1 | Acquire the basic knowledge of computer organization, computer architecture and assembly language. | C2 (Understand) | 1 |
| CLO2 | Understand the concepts of basic computer organization, architecture, and assembly language techniques. | C2 (Understand) | 2 |
| CLO3 | Solve problems related to computer organization and assembly language. | C3 (Apply) | 3, 4, 5 |

## Course Description

### 01 — Introduction to Computer Systems

- Introduction to Computer Systems

### 02 — Evolution of Intel Microprocessor

- Evolution of Intel Microprocessor

### 03 — Introduction to Assembly Language

- Introduction to Assembly Language

### 04 — Computer Organization

- Computer Organization

### 05 — Instruction Cycle

- Instruction Cycle

### 06 — Memory Architecture

- Memory Architecture

### 07 — Memory Representation & Hierarchy

- Memory Representation & Hierarchy

### 08 — Data, Address and Control Buses

- Data Bus
- Address Bus
- Control Bus

### 09 — Intel 8086 Family of Microprocessors

- Intel 8086 Family of Microprocessors

### 10 — Organization of Intel 8088/8086 Processor

- Organization of Intel 8088/8086 Processor

### 11 — Registers and Their Categories

- Registers
- Categories of Registers

### 12 — Functions of Registers

- Functions of Registers

### 13 — Memory Addressing

- Memory Addressing

### 14 — Real Mode Memory Structure

- Real Mode Memory Structure

### 15 — Memory Segmentation

- Memory Segmentation
- Segment/Offset Scheme

### 16 — Basic Computer Instructions

- Memory Reference Instructions
- Register Reference Instructions
- I/O Instructions

### 17 — Addressing Modes

- Addressing Modes

### 18 — Instruction Timing and Decoding

- Instruction Cycle
- Timing and Decoding

### 19 — RTL of Instructions

- RTL of the Instructions

### 20 — Basic Computer Operation Flowchart

- Complete Flowchart for the Basic Computer Operation

### 21 — Design of CPU

- Design of the CPU of a Basic Computer

### 22 — Assembly Language Syntax

- Assembly Language Syntax

### 23 — Program Data and Variables

- Program Data
- Variables

### 24 — Program Structure

- Program Structure

### 25 — Memory Models

- Memory Models

### 26 — Data, Stack and Code Segments

- Data Segment
- Stack Segment
- Code Segment

### 27 — Variants of MOV Instruction

- Variants of MOV Instruction

### 28 — Basic Instructions

- XCHG
- ADD
- SUB
- INC
- DEC
- NEG

### 29 — Processor Status and Flags Register

- Processor Status and Flags Register

### 30 — Flow Control Instructions

- Flow Control Instructions

### 31 — Jump Instructions

- Unconditional Jump
- Conditional Jumps

### 32 — Looping Structures

- Looping Structures

### 33 — Logic Instructions

- AND
- OR
- XOR
- NOT
- TEST

### 34 — Shift and Rotate Instructions

- Shift Instructions
- Rotate Instructions

### 35 — Number Input and Output Procedures

- Procedures to Input Binary, Decimal and Hexadecimal Numbers
- Procedures to Output Binary, Decimal and Hexadecimal Numbers

### 36 — Stack, PUSH and POP

- The Stack
- PUSH Instruction
- POP Instruction

### 37 — CALL and RET Instructions

- CALL Instruction
- RET Instruction

### 38 — MUL and DIV Instructions

- MUL Instruction
- DIV Instruction

### 39 — Related Programming Examples

- Related Programming Examples

### 40 — XLAT Instruction

- XLAT Instruction

### 41 — String Instructions

- String Instructions
- MOVSB/W
- LOADSB/W
- STOSSB/W
- SCASB/W
- CMPSB/W

### 42 — File Operations

- File Operations
- Reading a File
- Writing a File

---

## Textbooks

1. Charles Marut and Ytha Yu, *Assembly Language Programming and Organization of the IBM PC*, 1st Edition, McGraw-Hill, 1992. ISBN: 97800707026925.
2. M. Morris Mano, *Computer System Architecture*, 3rd Edition, Pearson, 1993. ISBN: 9780131755635.

## Reference Material

1. Barry B. Brey, *The Intel Microprocessors 8086/8088, 80186/80188, 80286, 80386, 80486, Pentium and Pentium Pro-Processor, Pentium II, Pentium III, Pentium 4*, 7th Edition, Prentice Hall, 2005. ISBN: 0131195069.
2. Kip R. Irvine, *Assembly Language for Intel Based Computers*, 4th Edition, Prentice Hall, 2002. ISBN: 9780130910134.

---

**BS Computer Science | CC-210 | Computer Organization & Assembly Language**
