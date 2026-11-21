# Static Data Members

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

Static Data Members are an important feature of C++ that allow a class to share one common variable among all its objects.

## Definition

A Static Data Member is a class variable declared using the `static` keyword. It is shared by all objects of the class, and only one copy exists for the entire class.

## Purpose

The main purposes of Static Data Members are:

- To share data among all objects.
- To maintain common information.
- To reduce memory usage.
- To keep track of the number of objects.
- To store class-level information.

## Characteristics

- It is declared using the `static` keyword inside a class.
- Only one copy exists for the entire class.
- All objects share the same static data member.
- It is not stored separately in each object.
- It is usually defined and initialized outside the class.
- It can be accessed using the class name and scope resolution operator `::`.

## Syntax

```cpp
class ClassName {
public:
    static int count;
};

int ClassName::count = 0;
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
};

int Student::count = 0;

int main() {
    Student s1;
    Student s2;
    Student s3;

    cout << "Total Objects: " << Student::count;

    return 0;
}
```

## Output

```text
Total Objects: 3
```

## Working

- `Student` is a class containing a static data member `count`.
- The static variable is declared using the `static` keyword.
- It is defined and initialized outside the class.
- When the first object is created, the constructor increases `count` by 1.
- The same happens when the second and third objects are created.
- The final value of `count` becomes 3.
- The static member is accessed using the class name `Student::count`.

## Advantages

- Saves memory because only one shared copy exists.
- Allows data sharing among objects.
- Helps maintain common information.
- Makes it easy to count objects.
- Provides class-level data management.

## Conclusion

Static Data Members are shared variables of a class. Only one copy exists for all objects, making them useful for storing common information and maintaining shared data.

---

**Prepared by:** Muhammad Ali  
**Subject:** Object Oriented Programming  
**Topic:** 32 — Static Data Members
