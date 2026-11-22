# Encapsulation 
**Subject: OOP** | **Language: C++**
## 📄 Important Point
- [Introduction](#introduction)
- [Definition](#definition)
- [Purpose](#purpose)
- [Access Specifiers](#access-specifiers)
- [Syntax](#syntax)
- [Example](#example)
- [Conclusion](#conclusion)

## Introduction
C++ provides an important Object Oriented Programming concept called Encapsulation. It binds data and the functions that operate on that data into a single unit called a class.
## Definition

**Encapsulation** is the process of binding data members and member functions together into a single unit called a class.
## Purpose
The main purpose of Encapsulation is to:
1. Keep data safe from direct access.
2. Allow controlled access to data through member functions.
## Access Specifiers
Access specifiers control access to class members.

C++ provides three access specifiers:
1. **Private:** Members can only be accessed from within the same class.
2. **Public:** Members can be accessed both inside and outside the class.
3. **Protected:** Members can be accessed within the class and its derived classes (Inheritance concept).

## Syntax
```cpp
class ClassName {
private:
    // Data members

public:
    // Member functions
};
```
### Diagram
```mermaid
flowchart TD
    A["class<br/><br>Creates a class"]
    A --> B["private<br/><br>Restricts access to members<br/>within the same class"]
    A --> C["public<br/><br>Allows access to <br>members<br/>from outside the class"]
  ```
  ## Example
  ``` cpp
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

    cout << s1.getAge();

    return 0;
}
```

  **Result**
  >Result is 20

<br>

**💡 Takeaway**
> Encapsulation allows private data to be accessed and modified through public member functions.

## Conclusion

Encapsulation combines data and related functions into a single class. It keeps data safe and allows access through public member functions.

---
Made with ❤️ by Muhammad Ali

  
  
