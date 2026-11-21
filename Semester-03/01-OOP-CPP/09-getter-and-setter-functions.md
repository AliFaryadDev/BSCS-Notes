
# Getter and Setter Functions

**Subject:** Object Oriented Programming (OOP)  
**Language:** C++

## Important Points
- [Introduction](#introduction)
- [Definition](#definition)
- [Getter Function](#getter-function)
- [Setter Function](#setter-function)
- [Purpose](#purpose)
- [Syntax](#syntax)
- [Example](#example)
- [Working](#working)
- [Advantages](#advantages)
- [Conclusion](#conclusion)

## Introduction

Getter and Setter functions are used in Object-Oriented Programming to access and modify private data members of a class.

## Definition

Getter and Setter functions are public member functions that allow controlled access to private data members of a class.

## Getter Function

A Getter function is a public member function used to read or return the value of a private data member.

**Example:**

```cpp
int getAge() {
    return age;
}
```

## Setter Function

A Setter function is a public member function used to set or update the value of a private data member.

**Example:**

```cpp
void setAge(int a) {
    age = a;
}
```

## Purpose

The main purposes of Getter and Setter functions are:

- To access private data members.
- To modify private data members.
- To provide controlled access to data.
- To protect data from invalid values.
- To support encapsulation.

## Syntax

```cpp
class Student {
private:
    int age;

public:
    void setAge(int a) {
        age = a;
    }

    int getAge() {
        return age;
    }
};
```

## Example

```cpp
#include <iostream>
using namespace std;

class Student {
private:
    int age;

public:
    void setAge(int a) {
        age = a;
    }

    int getAge() {
        return age;
    }
};

int main() {
    Student s1;

    s1.setAge(20);

    cout << "Age: " << s1.getAge();

    return 0;
}
```

## Working

- `Student` is a class.
- `age` is a private data member.
- `setAge()` is a Setter function that assigns a value to age.
- `getAge()` is a Getter function that returns the value of age.
- `s1.setAge(20)` sets the age to 20.
- `s1.getAge()` retrieves and displays the age.

## Advantages

- Protects private data members.
- Provides controlled access to data.
- Supports data validation.
- Improves data security.
- Supports encapsulation.

## Conclusion

Getter and Setter functions provide controlled access to private data members. Getter functions read data, while Setter functions modify data. They help implement encapsulation in C++.

---

**Prepared by:** Muhammad Ali  
**Subject:** Object Oriented Programming  
**Topic:** 09 — Getter/Setter Functions
