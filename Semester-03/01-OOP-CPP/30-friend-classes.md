
# Friend Classes

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

Friend Classes are an important feature of C++ that allow one class to access the private and protected members of another class.

## Definition

A Friend Class is a class that is declared as a friend of another class using the `friend` keyword. It can access the private and protected members of that class.

## Purpose

The main purposes of Friend Classes are:

- To allow one class to access another class's private data.
- To share information between classes.
- To provide flexibility in programming.
- To simplify communication between related classes.
- To support cooperation between classes.

## Characteristics

- A friend class is declared using the `friend` keyword.
- It can access private and protected members of the other class.
- It is not a member of the class that declares it as a friend.
- Friendship is not mutual automatically.
- Friendship is not inherited.
- Friendship is not transitive.

## Syntax

```cpp id="z4n8xp"
class ClassA {
private:
    int value = 100;

    friend class ClassB;
};

class ClassB {
    // Can access private members of ClassA
};
```

## Example

```cpp id="q2m5vb"
#include <iostream>
using namespace std;

class Student {
private:
    int marks = 90;

    friend class Teacher;
};

class Teacher {
public:
    void display(Student s) {
        cout << "Student Marks: " << s.marks;
    }
};

int main() {
    Student s;
    Teacher t;

    t.display(s);

    return 0;
}
```

## Output

```text id="p8k3wy"
Student Marks: 90
```

## Working

- `Student` is a class containing a private data member `marks`.
- The `Teacher` class is declared as a friend of `Student`.
- The `Teacher` class can access the private members of `Student`.
- The `display()` function receives a Student object.
- It accesses the private member `marks`.
- The marks are displayed on the screen.

## Advantages

- Allows access to private and protected members.
- Improves cooperation between related classes.
- Provides flexibility in programming.
- Simplifies certain class operations.
- Supports complex programming tasks.

## Conclusion

A Friend Class is a class that can access the private and protected members of another class. It is declared using the `friend` keyword and helps different classes work together.

---

**Prepared by:** Muhammad Ali  
**Subject:** Object Oriented Programming  
**Topic:** Friend Classes
