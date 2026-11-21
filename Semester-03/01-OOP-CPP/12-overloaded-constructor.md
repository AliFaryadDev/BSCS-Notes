
# Overloaded Constructor

**Subject:** Object Oriented Programming (OOP)  
**Language:** C++

## Important Points
- [Introduction](#introduction)
- [Definition](#definition)
- [Purpose](#purpose)
- [Working of Constructor Overloading](#working-of-constructor-overloading)
- [Rules of Constructor Overloading](#rules-of-constructor-overloading)
- [Syntax](#syntax)
- [Example](#example)
- [Working](#working)
- [Advantages](#advantages)
- [Conclusion](#conclusion)

## Introduction

Constructor Overloading is an important feature of Object-Oriented Programming. It allows a class to have multiple constructors with different parameters.

## Definition

Constructor Overloading is the process of defining multiple constructors in the same class with different parameter lists.

## Purpose

The main purposes of constructor overloading are:

- To initialize objects in different ways.
- To provide flexibility during object creation.
- To accept different numbers of arguments.
- To make object initialization easier.

## Working of Constructor Overloading

Constructor overloading works by defining multiple constructors with different parameter lists. The compiler selects the appropriate constructor according to the arguments passed during object creation.

## Rules of Constructor Overloading

- All constructors must have the same name as the class.
- Constructors must have different parameter lists.
- Constructors cannot differ only by return type because they have no return type.
- The appropriate constructor is selected based on the arguments.

## Syntax

```cpp
class ClassName {
public:
    ClassName() {
        // Default constructor
    }

    ClassName(int a) {
        // One parameter
    }

    ClassName(int a, int b) {
        // Two parameters
    }
};
```

## Example

```cpp
#include <iostream>
using namespace std;

class Student {
public:
    int age;

    Student() {
        age = 0;
    }

    Student(int a) {
        age = a;
    }

    Student(int a, int b) {
        age = a + b;
    }

    void display() {
        cout << "Age: " << age << endl;
    }
};

int main() {
    Student s1;
    Student s2(20);
    Student s3(10, 10);

    s1.display();
    s2.display();
    s3.display();

    return 0;
}
```

## Working

- `Student()` is a default constructor that sets age to 0.
- `Student(int a)` is a parameterized constructor that sets age to the given value.
- `Student(int a, int b)` accepts two arguments and adds them.
- `s1` calls the default constructor.
- `s2(20)` calls the one-parameter constructor.
- `s3(10, 10)` calls the two-parameter constructor.
- The `display()` function shows the values.

## Advantages

- Provides multiple ways to initialize objects.
- Increases flexibility.
- Reduces repeated code.
- Makes object creation easier.
- Supports constructor overloading.

## Conclusion

Constructor Overloading allows a class to have multiple constructors with different parameter lists. It provides flexibility by initializing objects in different ways.

---

**Prepared by:** Muhammad Ali  
**Subject:** Object Oriented Programming  
**Topic:** 12 — Overloaded Constructor
