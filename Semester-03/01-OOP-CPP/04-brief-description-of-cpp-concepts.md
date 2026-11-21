
# Brief Description of C++ Concepts

**Subject:** Object Oriented Programming (OOP)  
**Language:** C++

## Important Points
- [Introduction](#introduction)
- [Definition](#definition)
- [Basic C++ Concepts](#basic-c-concepts)
- [Example](#example)
- [Conclusion](#conclusion)

## Introduction

C++ is a general-purpose programming language that supports procedural, object-oriented, and generic programming. It provides different concepts for developing efficient and organized software.

## Definition

C++ is a high-level, general-purpose programming language developed by Bjarne Stroustrup. It is an extension of the C programming language.

## Basic C++ Concepts

### Variables
Variables are named memory locations used to store data.

### Data Types
Data types define the type of data a variable can store, such as `int`, `float`, `char`, and `double`.

### Operators
Operators are symbols used to perform operations on data, such as `+`, `-`, `*`, and `/`.

### Conditional Statements
Conditional statements are used to make decisions in a program, such as `if`, `else`, and `switch`.

### Loops
Loops are used to repeat a block of code, such as `for`, `while`, and `do-while`.

### Functions
Functions are reusable blocks of code that perform specific tasks.

### Classes and Objects
Classes are blueprints, while objects are instances of classes.

### Inheritance
Inheritance allows one class to acquire properties and functions of another class.

### Polymorphism
Polymorphism allows the same interface or function name to perform different behaviors.

### Encapsulation
Encapsulation combines data and functions into a single unit and controls access to data.

### Abstraction
Abstraction hides implementation details and shows essential features.

## Example

```cpp
#include <iostream>
using namespace std;

class Student {
public:
    string name = "Ali";

    void display() {
        cout << "Student Name: " << name;
    }
};

int main() {
    Student s;
    s.display();

    return 0;
}
```

## Output

```text
Student Name: Ali
```

## Conclusion

C++ provides programming concepts such as variables, data types, functions, classes, objects, inheritance, polymorphism, encapsulation, and abstraction. These concepts help developers create efficient and organized programs.

---

**Prepared by:** Muhammad Ali  
**Subject:** Object Oriented Programming  
**Topic:** 04 — Brief Description of C++ Concepts
