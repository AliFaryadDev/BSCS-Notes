
# Memory Models

**Subject: Computer Organization & Assembly Language (CC-210)**  
**Semester: 03**

## 📄 Table of Contents

- [Introduction](#introduction)
- [Definition of Memory Model](#definition-of-memory-model)
- [Purpose of Memory Models](#purpose-of-memory-models)
- [Types of Memory Models](#types-of-memory-models)
- [Tiny Model](#tiny-model)
- [Small Model](#small-model)
- [Medium Model](#medium-model)
- [Compact Model](#compact-model)
- [Large Model](#large-model)
- [Huge Model](#huge-model)
- [Comparison of Memory Models](#comparison-of-memory-models)
- [Conclusion](#conclusion)

---

## Introduction

Memory Models define how code and data are organized into memory segments in an Assembly Language program.

In 16-bit DOS programming, memory models help determine the organization and size of code and data segments.

They are commonly specified using the `.MODEL` directive in MASM/TASM.

## Definition of Memory Model

A Memory Model is a predefined arrangement of code and data segments that determines how a program uses memory.

## Purpose of Memory Models

- Organize program code and data.
- Define the number of code and data segments.
- Help manage program memory requirements.
- Simplify memory organization in assembly programs.

## Types of Memory Models

Traditional 16-bit DOS programming uses six common memory models:

1. Tiny Model
2. Small Model
3. Medium Model
4. Compact Model
5. Large Model
6. Huge Model

## Tiny Model

The Tiny Model uses a single combined segment for code and data.

### Characteristics

- Code and data share one segment.
- The total program image must fit within one 64 KB segment.
- Commonly used for COM programs.

**Directive:**

```asm
.MODEL TINY
```

## Small Model

The Small Model uses:

- One code segment.
- One data segment.

Each segment can contain up to 64 KB.

**Directive:**

```asm
.MODEL SMALL
```

It is suitable for small programs.

## Medium Model

The Medium Model uses:

- Multiple code segments.
- One data segment.

It is useful for programs that require more than one code segment but have a relatively small data area.

**Directive:**

```asm
.MODEL MEDIUM
```

## Compact Model

The Compact Model uses:

- One code segment.
- Multiple data segments.

It is suitable for programs with larger data requirements.

**Directive:**

```asm
.MODEL COMPACT
```

## Large Model

The Large Model supports:

- Multiple code segments.
- Multiple data segments.

It is used for programs that require larger code and data areas.

**Directive:**

```asm
.MODEL LARGE
```

## Huge Model

The Huge Model is similar to the Large Model but supports large data objects that may extend beyond a single 64 KB segment.

It uses special compiler and memory-management support for handling such data.

**Directive:**

```asm
.MODEL HUGE
```

## Comparison of Memory Models

| Model | Code Organization | Data Organization |
|---|---|---|
| Tiny | One combined segment | Shared with code |
| Small | One code segment | One data segment |
| Medium | Multiple code segments | One data segment |
| Compact | One code segment | Multiple data segments |
| Large | Multiple code segments | Multiple data segments |
| Huge | Multiple code segments | Multiple data segments, including huge objects |

## Conclusion

Memory Models define how code and data are arranged in memory. Different models are used according to the size and memory requirements of a program.
