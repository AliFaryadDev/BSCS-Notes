
# Destructor

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
- [Difference Between Constructor and Destructor](#difference-between-constructor-and-destructor)
- [Conclusion](#conclusion)

## Introduction

A Destructor is a special member function of a class in C++. It is automatically called when an object is destroyed.

## Definition

A Destructor is a special member function that is used to perform cleanup tasks when an object is destroyed.

## Purpose

The main purposes of a destructor are:

- To release resources used by an object.
- To free dynamically allocated memory.
- To close files and connections.
- To perform cleanup tasks.
- To prevent resource leaks.

## Characteristics

- It has the same name as the class, preceded by a tilde (`~`).
- It has no return type.
- It takes no arguments.
- It is called automatically when an object is destroyed.
- A class can have only one destructor.
- It cannot be overloaded.

## Syntax

```cpp
class ClassName {
public:
    ~ClassName() {
        // Cleanup code
    }
};
```

## Example

```cpp
#include <iostream>
using namespace std;

class Student {
public:
    Student() {
        cout << "Constructor Called" << endl;
    }

    ~Student() {
        cout << "Destructor Called" << endl;
    }
};

int main() {
    Student s1;

    cout << "Program Running" << endl;

    return 0;
}
```

## Working

- `Student` is a class.
- `Student()` is the constructor.
- `~Student()` is the destructor.
- When object `s1` is created, the constructor is called.
- The program executes its statements.
- When `main()` ends, object `s1` is destroyed.
- The destructor is automatically called.

## Advantages

- Releases resources automatically.
- Helps prevent memory leaks.
- Performs cleanup tasks.
- Closes files and connections.
- Improves resource management.

## Difference Between Constructor and Destructor

| Constructor | Destructor |
|---|---|
| Initializes an object. | Performs cleanup when an object is destroyed. |
| Has the same name as the class. | Has the same name preceded by `~`. |
| Can accept arguments. | Takes no arguments. |
| Can be overloaded. | Cannot be overloaded. |
| Called when an object is created. | Called when an object is destroyed. |

## Conclusion

A Destructor is a special member function that is automatically called when an object is destroyed. It performs cleanup tasks and helps manage resources.

---

**Prepared by:** Muhammad Ali  
**Subject:** Object Oriented Programming  
**Topic:** Destructor
