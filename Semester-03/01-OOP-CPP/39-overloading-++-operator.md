
# Overloading ++ Operator

**Subject:** Object Oriented Programming (OOP)  
**Language:** C++

## Important Points
- [Introduction](#introduction)
- [Definition](#definition)
- [Purpose](#purpose)
- [Types of Increment Operator](#types-of-increment-operator)
- [Syntax](#syntax)
- [Example](#example)
- [Working](#working)
- [Advantages](#advantages)
- [Conclusion](#conclusion)

## Introduction

The Increment Operator (`++`) is a unary operator in C++ that increases the value of a variable by one. It can also be overloaded to work with user-defined objects.

## Definition

Overloading the `++` operator is the process of defining how the increment operator increases the value of an object of a class.

## Purpose

The main purposes of overloading the `++` operator are:

- To increase object values by one.
- To perform increment operations on objects.
- To improve code readability.
- To simplify object manipulation.
- To provide flexibility in programming.

## Types of Increment Operator

There are two types of increment operators:

### Prefix Increment

The operator is written before the operand.

```cpp
++obj;
```

It increments the object before its updated value is used.

### Postfix Increment

The operator is written after the operand.

```cpp
obj++;
```

It uses the original value before incrementing the object.

## Syntax

**Prefix:**

```cpp
ClassName operator++();
```

**Postfix:**

```cpp
ClassName operator++(int);
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

    void operator++() {
        ++value;
    }
};

int main() {
    Number n(10);

    ++n;

    cout << "Value: " << n.value;

    return 0;
}
```

## Output

```text
Value: 11
```

## Working

- `Number` is a class containing an integer data member.
- The `operator++()` function overloads the prefix increment operator.
- An object `n` is created with value 10.
- The expression `++n` calls the overloaded function.
- The value of the object increases by one.
- The new value becomes 11.
- The result is displayed on the screen.

## Advantages

- Allows increment operations on objects.
- Improves code readability.
- Simplifies object manipulation.
- Provides flexibility.
- Supports compile-time polymorphism.

## Conclusion

Overloading the `++` operator allows the increment operator to increase the value of a user-defined object. It supports both prefix and postfix forms.

---

**Prepared by:** Muhammad Ali  
**Subject:** Object Oriented Programming  
**Topic:** 39 — Overloading ++ Operator
