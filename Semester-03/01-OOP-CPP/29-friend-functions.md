
# Friend Functions

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

Friend Functions are an important feature of C++ that allow an external function to access the private and protected members of a class.

## Definition

A Friend Function is a non-member function that is declared inside a class using the `friend` keyword and can access its private and protected members.

## Purpose

The main purposes of Friend Functions are:

- To access private and protected members of a class.
- To allow external functions to work with class data.
- To share data between different classes or functions.
- To provide flexibility in programming.
- To support operator overloading.

## Characteristics

- A friend function is not a member of the class.
- It is declared inside the class using the `friend` keyword.
- It can access private and protected members.
- It is defined outside the class like a normal function.
- It is called like a normal function, not through an object.
- It does not use the `this` pointer.

## Syntax

```cpp id="9wxv8r"
class ClassName {
private:
    int value;

public:
    friend void display(ClassName obj);
};

void display(ClassName obj) {
    // Access class members
}
```

## Example

```cpp id="7n2k3p"
#include <iostream>
using namespace std;

class Student {
private:
    int marks = 90;

public:
    friend void display(Student s);
};

void display(Student s) {
    cout << "Marks: " << s.marks;
}

int main() {
    Student s;

    display(s);

    return 0;
}
```

## Output

```text id="3n4x5z"
Marks: 90
```

## Working

- `Student` is a class containing a private data member `marks`.
- The `display()` function is declared as a friend using the `friend` keyword.
- The friend function is defined outside the class.
- An object of the Student class is passed to the function.
- The function accesses the private member `marks`.
- The marks are displayed on the screen.

## Advantages

- Allows access to private and protected members.
- Supports operator overloading.
- Helps functions work with multiple classes.
- Provides flexibility in programming.
- Can simplify certain operations.

## Conclusion

A Friend Function is a non-member function that can access the private and protected members of a class. It is declared using the `friend` keyword and provides additional flexibility in C++ programming.

---

**Prepared by:** Muhammad Ali  
**Subject:** Object Oriented Programming  
**Topic:** 29 — Friend Functions
