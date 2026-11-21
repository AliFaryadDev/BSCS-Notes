
# Static Member Functions

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

Static Member Functions are an important feature of C++ that belong to a class rather than individual objects. They can be called using the class name without creating an object.

## Definition

A Static Member Function is a function declared inside a class using the `static` keyword. It belongs to the class and can directly access only static data members and other static member functions.

## Purpose

The main purposes of Static Member Functions are:

- To access static data members.
- To perform class-level operations.
- To access shared information.
- To call functions without creating objects.
- To manage common data of a class.

## Characteristics

- It is declared using the `static` keyword.
- It belongs to the class rather than individual objects.
- It can be called using the class name and `::` operator.
- It can directly access only static members.
- It does not have a `this` pointer.
- It can be called without creating an object.

## Syntax

```cpp
class ClassName {
public:
    static void functionName();
};

void ClassName::functionName() {
    // Function body
}
```

## Example

```cpp
#include <iostream>
using namespace std;

class Student {
public:
    static int count;

    Student() {
        count++;
    }

    static void display() {
        cout << "Total Students: " << count;
    }
};

int Student::count = 0;

int main() {
    Student s1;
    Student s2;
    Student s3;

    Student::display();

    return 0;
}
```

## Output

```text
Total Students: 3
```

## Working

- `Student` is a class containing a static data member `count`.
- The static member function `display()` is declared using the `static` keyword.
- Three objects of the Student class are created.
- The constructor increases the shared `count` variable each time an object is created.
- The static function accesses the static data member `count`.
- The function is called using `Student::display()` without creating another object.
- The total number of students is displayed.

## Advantages

- Allows functions to be called without creating objects.
- Provides access to static data members.
- Helps perform class-level operations.
- Improves code organization.
- Useful for managing shared information.

## Conclusion

Static Member Functions are functions that belong to a class rather than individual objects. They can be called using the class name and directly access static members of the class.

---

**Prepared by:** Muhammad Ali  
**Subject:** Object Oriented Programming  
**Topic:** 33 — Static Member Functions
