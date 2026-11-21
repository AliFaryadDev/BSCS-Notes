
# Overloading Binary Operators

**Subject:** Object Oriented Programming (OOP)  
**Language:** C++

## Important Points
- [Introduction](#introduction)
- [Definition](#definition)
- [Purpose](#purpose)
- [Characteristics](#characteristics)
- [Syntax](#syntax)
- [Example](#example)
- [Working](#working)
- [Advantages](#advantages)
- [Conclusion](#conclusion)

## Introduction

Binary Operator Overloading is a feature of C++ that allows binary operators to work with user-defined objects.

## Definition

Binary Operator Overloading is the process of defining how a binary operator performs an operation on objects of a class.

## Purpose

The main purposes of Binary Operator Overloading are:

- To perform operations on objects.
- To make code easier to read.
- To use operators with user-defined data types.
- To provide flexibility in programming.
- To simplify object operations.

## Characteristics

- Binary operators work with two operands.
- They can be overloaded using member or non-member functions.
- At least one operand must be a user-defined type.
- Operator overloading does not change the original meaning of operators for built-in types.
- The operator's precedence and associativity cannot be changed.

## Syntax

```cpp
returnType operator symbol (ClassName obj);
```

## Example

```cpp
#include <iostream>
using namespace std;

class Number {
public:
    int value;

    Number(int v) {
        value = v;
    }

    Number operator+(Number obj) {
        return Number(value + obj.value);
    }
};

int main() {
    Number n1(10), n2(20);

    Number n3 = n1 + n2;

    cout << "Sum: " << n3.value;

    return 0;
}
```

## Output

```text
Sum: 30
```

## Working

- `Number` is a class containing an integer data member.
- The `operator+()` function overloads the `+` operator.
- Two objects `n1` and `n2` are created.
- The expression `n1 + n2` calls the overloaded operator function.
- The function adds the values of both objects.
- A new object `n3` stores the result.
- The result is displayed on the screen.

## Advantages

- Improves code readability.
- Allows operators to work with objects.
- Simplifies object operations.
- Makes programs more flexible.
- Supports compile-time polymorphism.

## Conclusion

Binary Operator Overloading allows operators such as `+`, `-`, `*`, and `/` to perform operations on user-defined objects. It makes programs easier to read and use.

---

**Prepared by:** Muhammad Ali  
**Subject:** Object Oriented Programming  
**Topic:** 37 — Overloading Binary Operators
