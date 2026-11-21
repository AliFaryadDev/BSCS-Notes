
# Object Aggregation

**Subject:** Object Oriented Programming (OOP)  
**Language:** C++

## Important Points
- [Introduction](#introduction)
- [Definition](#definition)
- [Purpose](#purpose)
- [Relationship Between Objects](#relationship-between-objects)
- [Syntax](#syntax)
- [Example](#example)
- [Working](#working)
- [Advantages](#advantages)
- [Composition vs Aggregation](#composition-vs-aggregation)
- [Conclusion](#conclusion)

## Introduction

Object Aggregation is an important concept in Object-Oriented Programming (OOP). It allows one class to use an object of another class without owning its lifetime.

## Definition

Object Aggregation is a relationship in which one class contains a reference or pointer to an object of another class.

It represents a **Has-A Relationship**, where both objects can exist independently.

## Purpose

The main purposes of Object Aggregation are:

- To establish relationships between different objects.
- To reuse existing objects.
- To reduce dependency between classes.
- To make programs more flexible.
- To represent real-world relationships.

## Relationship Between Objects

Object Aggregation represents a **Has-A Relationship**.

Example:

- A Department has Teachers.
- A Team has Players.
- A Library has Books.

In these examples, the objects can exist independently of each other.

## Syntax

```cpp
class ClassA {
public:
    void display() {
        cout << "Class A Object";
    }
};

class ClassB {
private:
    ClassA* obj;

public:
    ClassB(ClassA* a) {
        obj = a;
    }
};
```

Here, `ClassB` stores a pointer to an existing object of `ClassA`.

## Example

```cpp
#include <iostream>
using namespace std;

class Teacher {
public:
    void display() {
        cout << "Teacher is teaching.";
    }
};

class Department {
private:
    Teacher* teacher;

public:
    Department(Teacher* t) {
        teacher = t;
    }

    void show() {
        teacher->display();
    }
};

int main() {
    Teacher t;
    Department d(&t);

    d.show();

    return 0;
}
```

## Output

```text
Teacher is teaching.
```

## Working

- `Teacher` is a class containing a `display()` function.
- `Department` is another class.
- The `Department` class stores a pointer to a `Teacher` object.
- In `main()`, an independent object of `Teacher` is created.
- Its address is passed to the `Department` constructor.
- The `show()` function accesses the Teacher object through the pointer.
- The Teacher object can exist independently of the Department object.

## Advantages

- Promotes code reusability.
- Reduces dependency between classes.
- Allows independent object lifetimes.
- Improves program flexibility.
- Helps represent real-world relationships.

## Composition vs Aggregation

| Composition | Aggregation |
|---|---|
| Strong Has-A Relationship | Weak Has-A Relationship |
| Owns the contained object | Does not own the referenced object |
| Object lifetime is tied to its owner | Objects can have independent lifetimes |
| Example: Car and Engine | Example: Department and Teacher |

## Conclusion

Object Aggregation allows one class to use an object of another class without owning its lifetime. It represents a Has-A Relationship and provides flexibility by allowing objects to exist independently.

---

**Prepared by:** Muhammad Ali  
**Subject:** Object Oriented Programming  
**Topic:** 27 — Object Aggregation
