
# Function Overloading

**Subject:** Object Oriented Programming (OOP)  
**Language:** C++

## Important Points
- [Introduction](#introduction)
- [Definition](#definition)
- [Purpose](#purpose)
- [Rules of Function Overloading](#rules-of-function-overloading)
- [Syntax](#syntax)
- [Example](#example)
- [Working](#working)
- [Advantages](#advantages)
- [Conclusion](#conclusion)

## Introduction

Function Overloading is an important feature of C++ that allows multiple functions to have the same name but different parameters.

## Definition

Function Overloading is the process of defining multiple functions with the same name but different parameter lists in the same scope.

## Purpose

The main purposes of function overloading are:

- To perform similar tasks using the same function name.
- To improve code readability.
- To provide flexibility.
- To reduce the need for different function names.
- To make programs easier to manage.

## Rules of Function Overloading

- Functions must have the same name.
- Functions must have different parameter lists.
- Parameters can differ in number, type, or order.
- Functions cannot be overloaded by changing only their return type.
- The compiler selects the appropriate function based on the arguments.

## Syntax

```cpp
returnType functionName(int a);

returnType functionName(int a, int b);

returnType functionName(double a);
```

## Example

```cpp
#include <iostream>
using namespace std;

class Calculator {
public:
    int add(int a, int b) {
        return a + b;
    }

    int add(int a, int b, int c) {
        return a + b + c;
    }

    double add(double a, double b) {
        return a + b;
    }
};

int main() {
    Calculator c;

    cout << c.add(10, 20) << endl;
    cout << c.add(10, 20, 30) << endl;
    cout << c.add(2.5, 3.5);

    return 0;
}
```

## Output

```text
30
60
6
```

## Working

- `Calculator` is a class.
- It contains three functions with the same name `add()`.
- The first function accepts two integers.
- The second function accepts three integers.
- The third function accepts two double values.
- The compiler selects the appropriate function according to the arguments.
- Each function performs addition and returns the result.

## Advantages

- Improves code readability.
- Allows the same function name for similar tasks.
- Provides flexibility.
- Reduces the need for multiple function names.
- Supports compile-time polymorphism.

## Conclusion

Function Overloading allows multiple functions to have the same name with different parameter lists. It improves code readability and supports compile-time polymorphism.

---

**Prepared by:** Muhammad Ali  
**Subject:** Object Oriented Programming  
**Topic:** Function Overloading
