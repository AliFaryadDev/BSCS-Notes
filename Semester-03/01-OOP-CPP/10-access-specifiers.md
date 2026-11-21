
# Access Specifiers

**Subject:** Object Oriented Programming (OOP)  
**Language:** C++

## Important Points
- [Introduction](#introduction)
- [Definition](#definition)
- [Types of Access Specifiers](#types-of-access-specifiers)
- [Public Access Specifier](#public-access-specifier)
- [Private Access Specifier](#private-access-specifier)
- [Protected Access Specifier](#protected-access-specifier)
- [Syntax](#syntax)
- [Example](#example)
- [Working](#working)
- [Difference Between Access Specifiers](#difference-between-access-specifiers)
- [Advantages](#advantages)
- [Conclusion](#conclusion)

## Introduction

Access Specifiers are an important feature of Object-Oriented Programming. They define the accessibility of class members, such as data members and member functions.

## Definition

Access Specifiers are keywords in C++ that control the accessibility of class members from different parts of a program.

## Types of Access Specifiers

C++ provides three types of access specifiers:

- Public
- Private
- Protected

## Public Access Specifier

Public members can be accessed from anywhere in the program through an object of the class, subject to normal access rules.

**Example:**

```cpp
public:
    int age = 20;
```

## Private Access Specifier

Private members can only be accessed directly within the same class. They cannot be accessed directly from outside the class.

**Example:**

```cpp
private:
    int age = 20;
```

## Protected Access Specifier

Protected members can be accessed within the same class and its derived classes. They cannot be accessed directly from outside the class through an object.

**Example:**

```cpp
protected:
    int age = 20;
```

## Syntax

```cpp
class Student {
public:
    int rollNo;

private:
    int age;

protected:
    int marks;
};
```

## Example

```cpp
#include <iostream>
using namespace std;

class Student {
public:
    int rollNo = 101;

private:
    int age = 20;

protected:
    int marks = 85;

public:
    void display() {
        cout << "Roll No: " << rollNo << endl;
        cout << "Age: " << age << endl;
        cout << "Marks: " << marks;
    }
};

int main() {
    Student s1;

    cout << s1.rollNo << endl;

    s1.display();

    return 0;
}
```

## Working

- `Student` is a class.
- `rollNo` is a public data member and can be accessed through an object.
- `age` is a private data member and can only be accessed directly inside the class.
- `marks` is a protected data member and can be accessed inside the class and its derived classes.
- `display()` is a public member function that accesses all three members.
- `s1.display()` calls the function and displays their values.

## Difference Between Access Specifiers

| Public | Private | Protected |
|---|---|---|
| Accessible from anywhere through an object. | Accessible directly only within the same class. | Accessible within the same class and derived classes. |
| Can be accessed outside the class. | Cannot be accessed directly outside the class. | Cannot be accessed directly outside the class through an object. |
| Used for public interfaces. | Used to hide data. | Used to support inheritance. |

## Advantages

- Provides data protection.
- Controls access to class members.
- Supports encapsulation.
- Hides sensitive data.
- Improves program security and organization.

## Conclusion

Access Specifiers control the accessibility of class members in C++. The three types are Public, Private, and Protected. They help protect data and implement encapsulation.

---

**Prepared by:** Muhammad Ali  
**Subject:** Object Oriented Programming  
**Topic:** 10 — Access Specifiers
