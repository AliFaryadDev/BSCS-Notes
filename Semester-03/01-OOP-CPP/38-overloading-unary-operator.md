
# Overloading Unary Operators

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

Unary Operator Overloading is a feature of C++ that allows unary operators to perform operations on user-defined objects.

## Definition

Unary Operator Overloading is the process of defining how a unary operator performs an operation on an object of a class.

## Purpose

The main purposes of Unary Operator Overloading are:

- To perform operations on objects.
- To simplify object manipulation.
- To improve code readability.
- To provide flexibility in programming.
- To use unary operators with user-defined data types.

## Characteristics

- Unary operators work with one operand.
- They can be overloaded using member or non-member functions.
- At least one operand must be a user-defined type.
- They can be used to change or access object values.
- Their original meaning for built-in types remains unchanged.

## Common Unary Operators

- `++` : Increment operator.
- `--` : Decrement operator.
- `-` : Unary minus operator.
- `!` : Logical NOT operator.

## Syntax

```cpp
returnType operator symbol();
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

    void operator-() {
        value = -value;
    }
};

int main() {
    Number n(10);

    -n;

    cout << "Value: " << n.value;

    return 0;
}
```

## Output

```text
Value: -10
```

## Working

- `Number` is a class containing an integer data member.
- The `operator-()` function overloads the unary minus operator.
- An object `n` is created with value 10.
- The expression `-n` calls the overloaded operator function.
- The function changes the value to -10.
- The result is displayed on the screen.

## Advantages

- Improves code readability.
- Allows unary operators to work with objects.
- Simplifies object manipulation.
- Provides flexibility.
- Supports compile-time polymorphism.

## Conclusion

Unary Operator Overloading allows unary operators such as `++`, `--`, `-`, and `!` to perform operations on user-defined objects.

---

**Prepared by:** Muhammad Ali  
**Subject:** Object Oriented Programming  
**Topic:** 38 — Overloading Unary Operators
