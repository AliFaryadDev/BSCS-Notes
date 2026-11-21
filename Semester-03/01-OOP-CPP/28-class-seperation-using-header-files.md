
# Class Separation Using Header Files

**Subject:** Object Oriented Programming (OOP)  
**Language:** C++

## Important Points
- [Introduction](#introduction)
- [Definition](#definition)
- [Purpose](#purpose)
- [Header Files](#header-files)
- [Class Separation](#class-separation)
- [Syntax](#syntax)
- [Example](#example)
- [Working](#working)
- [Advantages](#advantages)
- [Conclusion](#conclusion)

## Introduction

Class Separation Using Header Files is a programming technique in C++ that organizes code into separate files. It makes programs easier to manage, understand, and maintain.

## Definition

Class Separation Using Header Files is the process of declaring a class in a header file and defining its member functions in a separate source file.

## Purpose

The main purposes of class separation are:

- To organize code into separate files.
- To improve code readability.
- To make programs easier to maintain.
- To promote code reusability.
- To separate class declarations from function definitions.

## Header Files

A header file is a file with the `.h` extension that usually contains:

- Class declarations.
- Function prototypes.
- Constants.
- Other declarations.

Example: `Student.h`

## Class Separation

In C++, class code is commonly divided into three files:

1. **Header File (.h):** Contains the class declaration.
2. **Source File (.cpp):** Contains the definitions of member functions.
3. **Main File (.cpp):** Contains the `main()` function and creates objects.

## Syntax

**Header File: Student.h**

```cpp
#ifndef STUDENT_H
#define STUDENT_H

class Student {
public:
    void display();
};

#endif
```

**Source File: Student.cpp**

```cpp
#include <iostream>
#include "Student.h"
using namespace std;

void Student::display() {
    cout << "Hello Student";
}
```

**Main File: main.cpp**

```cpp
#include "Student.h"

int main() {
    Student s;
    s.display();

    return 0;
}
```

## Example

The above three files work together to create a simple Student program.

## Output

```text
Hello Student
```

## Working

- `Student.h` contains the declaration of the Student class.
- `Student.cpp` contains the definition of the `display()` function.
- `main.cpp` includes the header file.
- An object of the Student class is created in `main()`.
- The `display()` function is called using the object.
- The compiler and linker combine the compiled files to create the final program.

## Advantages

- Makes code organized.
- Improves readability.
- Makes debugging easier.
- Supports code reusability.
- Makes large projects easier to maintain.
- Allows multiple source files to use the same class declaration.

## Conclusion

Class Separation Using Header Files is a technique used to organize C++ programs by separating class declarations and function definitions into different files. It improves code organization, readability, and maintainability.

---

**Prepared by:** Muhammad Ali  
**Subject:** Object Oriented Programming  
**Topic:** 28 — Class Separation Using Header Files
