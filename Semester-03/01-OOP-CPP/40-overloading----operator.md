
# Overloading -- Operator

**Subject:** Object Oriented Programming (OOP)  
**Language:** C++

## Important Points
- [Introduction](#introduction)
- [Definition](#definition)
- [Purpose](#purpose)
- [Types of Decrement Operator](#types-of-decrement-operator)
- [Syntax](#syntax)
- [Example](#example)
- [Working](#working)
- [Advantages](#advantages)
- [Conclusion](#conclusion)

## Introduction

The Decrement Operator (`--`) is a unary operator in C++ that decreases the value of a variable by one. It can also be overloaded to work with user-defined objects.

## Definition

Overloading the `--` operator is the process of defining how the decrement operator decreases the value of an object of a class.

## Purpose

The main purposes of overloading the `--` operator are:

- To decrease object values by one.
- To perform decrement operations on objects.
- To improve code readability.
- To simplify object manipulation.
- To provide flexibility in programming.

## Types of Decrement Operator

There are two types of decrement operators:

### Prefix Decrement

The operator is written before the operand.

```cpp
--obj;
```

It decrements the object before its updated value is used.

### Postfix Decrement

The operator is written after the operand.

```cpp
obj--;
```

It uses the original value before decrementing the object.

## Syntax

**Prefix:**

```cpp
ClassName operator--();
```

**Postfix:**

```cpp
ClassName operator--(int);
```

The dummy `int` parameter distinguishes the postfix version from the prefix version.

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

    void operator--() {
        --value;
    }
};

int main() {
    Number n(10);

    --n;

    cout << "Value: " << n.value;

    return 0;
}
```

## Output

```text
Value: 9
```

## Working

- `Number` is a class containing an integer data member.
- The `operator--()` function overloads the prefix decrement operator.
- An object `n` is created with value 10.
- The expression `--n` calls the overloaded function.
- The value of the object decreases by one.
- The new value becomes 9.
- The result is displayed on the screen.

## Advantages

- Allows decrement operations on objects.
- Improves code readability.
- Simplifies object manipulation.
- Provides flexibility.
- Supports compile-time polymorphism.

## Conclusion

Overloading the `--` operator allows the decrement operator to decrease the value of a user-defined object. It supports both prefix and postfix forms.

---

**Prepared by:** Muhammad Ali  
**Subject:** Object Oriented Programming  
**Topic:** 40 — Overloading -- Operator
