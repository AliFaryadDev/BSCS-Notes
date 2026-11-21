
# "this" Pointer

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

The `this` pointer is an important feature of C++ used inside non-static member functions. It refers to the current object that calls the member function.

## Definition

The `this` pointer is an implicit pointer available inside non-static member functions that stores the address of the current object.

## Purpose

The main purposes of the `this` pointer are:

- To refer to the current object.
- To differentiate between data members and function parameters.
- To access current object's members.
- To return the current object from a member function.
- To avoid naming conflicts.

## Characteristics

- It is an implicit pointer.
- It refers to the current object.
- It is available inside non-static member functions.
- It is not available inside static member functions.
- It can access the current object's data members and member functions.
- Its type depends on the class.

## Syntax

```cpp id="w4k8zp"
this->memberName;
```

Here, `this` points to the current object, and `->` is used to access its members.

## Example

```cpp id="m7q2vx"
#include <iostream>
using namespace std;

class Student {
private:
    int marks;

public:
    void setMarks(int marks) {
        this->marks = marks;
    }

    void display() {
        cout << "Marks: " << this->marks;
    }
};

int main() {
    Student s;

    s.setMarks(90);
    s.display();

    return 0;
}
```

## Output

```text id="n3p5wy"
Marks: 90
```

## Working

- `Student` is a class containing a private data member `marks`.
- The `setMarks()` function receives a parameter named `marks`.
- `this->marks` refers to the data member of the current object.
- The parameter `marks` contains the value passed to the function.
- `this->marks = marks` assigns the parameter value to the object's data member.
- The `display()` function accesses and displays the object's marks.

## Advantages

- Helps identify the current object.
- Resolves naming conflicts.
- Makes code easier to understand.
- Allows returning the current object.
- Provides access to the current object's members.

## Conclusion

The `this` pointer is an implicit pointer in C++ that refers to the current object. It is mainly used to access the current object's members and resolve naming conflicts.

---

**Prepared by:** Muhammad Ali  
**Subject:** Object Oriented Programming  
**Topic:** 31 — "this" Pointer
