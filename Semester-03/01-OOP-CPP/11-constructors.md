
# Constructors

**Subject:** Object Oriented Programming (OOP)  
**Language:** C++

## Important Points
- [Introduction](#introduction)
- [Definition](#definition)
- [Purpose](#purpose)
- [Characteristics of Constructor](#characteristics-of-constructor)
- [Types of Constructors](#types-of-constructors)
- [Default Constructor](#default-constructor)
- [Parameterized Constructor](#parameterized-constructor)
- [Copy Constructor](#copy-constructor)
- [Syntax](#syntax)
- [Example](#example)
- [Working](#working)
- [Advantages](#advantages)
- [Conclusion](#conclusion)

## Introduction

A constructor is a special member function of a class in C++. It is automatically called when an object is created.

## Definition

A constructor is a special member function that initializes an object when it is created.

## Purpose

The main purposes of constructors are:

- To initialize objects.
- To assign initial values to data members.
- To reduce repeated initialization code.
- To ensure objects start with valid values.

## Characteristics of Constructor

- It has the same name as the class.
- It has no return type, not even `void`.
- It is called automatically when an object is created.
- It is usually declared in the public section.
- It can be overloaded.

## Types of Constructors

The main types of constructors in C++ are:

- Default Constructor
- Parameterized Constructor
- Copy Constructor

## Default Constructor

A default constructor is a constructor that can be called without providing arguments.

**Example:**

```cpp
class Student {
public:
    Student() {
        cout << "Student Created";
    }
};
```

## Parameterized Constructor

A parameterized constructor is a constructor that accepts arguments to initialize an object with specific values.

**Example:**

```cpp
class Student {
public:
    int age;

    Student(int a) {
        age = a;
    }
};
```

## Copy Constructor

A copy constructor is a constructor that initializes a new object using another object of the same class.

**Example:**

```cpp
class Student {
public:
    int age;

    Student(int a) {
        age = a;
    }

    Student(const Student &s) {
        age = s.age;
    }
};
```

## Syntax

```cpp
class ClassName {
public:
    ClassName() {
        // Initialization code
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

    Student(int a) {
        age = a;
    }

    void display() {
        cout << "Age: " << age;
    }
};

int main() {
    Student s1(20);

    s1.display();

    return 0;
}
```

## Working

- `Student` is a class.
- `Student(int a)` is a parameterized constructor.
- `s1(20)` creates an object and passes 20 as an argument.
- The constructor assigns 20 to the `age` variable.
- `display()` shows the value of age.

## Advantages

- Automatically initializes objects.
- Saves time and reduces repeated code.
- Makes object initialization easier.
- Helps maintain valid initial values.
- Supports constructor overloading.

## Conclusion

A constructor is a special member function that is automatically called when an object is created. It initializes objects and helps make programs organized and efficient.

---

**Prepared by:** Muhammad Ali  
**Subject:** Object Oriented Programming  
**Topic:** 11 — Constructors
