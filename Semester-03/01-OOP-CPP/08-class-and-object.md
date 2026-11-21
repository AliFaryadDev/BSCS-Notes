
# Class and Object

**Subject:** Object Oriented Programming (OOP)  
**Language:** C++

## Important Points
- [Introduction](#introduction)
- [Definition of Class](#definition-of-class)
- [Definition of Object](#definition-of-object)
- [Purpose of Class and Object](#purpose-of-class-and-object)
- [Syntax of Class](#syntax-of-class)
- [Creating an Object](#creating-an-object)
- [Example](#example)
- [Working](#working)
- [Difference Between Class and Object](#difference-between-class-and-object)
- [Advantages](#advantages)
- [Conclusion](#conclusion)

## Introduction

Class and Object are the basic concepts of Object-Oriented Programming. A class is a blueprint, while an object is an instance of a class.

## Definition of Class

A class is a user-defined data type that contains data members and member functions.

## Definition of Object

An object is an instance of a class that has its own data and can use the functions defined in that class.

## Purpose of Class and Object

The main purposes of class and object are:

- To organize data and functions.
- To represent real-world entities.
- To make programs easier to manage.
- To support code reusability.
- To improve code organization.

## Syntax of Class

```cpp
class ClassName {
public:
    int data;

    void display() {
        cout << data;
    }
};
```

## Creating an Object

An object is created by writing the class name followed by the object name.

**Syntax:**

```cpp
ClassName objectName;
```

## Example

```cpp
#include <iostream>
using namespace std;

class Student {
public:
    string name = "Ali";
    int age = 20;

    void display() {
        cout << name << endl;
        cout << age;
    }
};

int main() {
    Student s1;

    s1.display();

    return 0;
}
```

## Working

- `Student` is a class.
- `name` and `age` are data members.
- `display()` is a member function.
- `s1` is an object of the Student class.
- The dot (`.`) operator is used to access the object's members.
- `s1.display()` calls the display function.

## Difference Between Class and Object

| Class | Object |
|---|---|
| A class is a blueprint. | An object is an instance of a class. |
| It defines data members and functions. | It uses the data members and functions of a class. |
| It is a logical entity. | It is a physical entity in memory. |
| Memory for non-static data members is allocated when an object is created. | Each object has its own non-static data members. |

## Advantages

- Organizes data and functions.
- Makes code reusable.
- Represents real-world entities.
- Makes programs easier to maintain.
- Helps manage complex programs.

## Conclusion

A class is a blueprint that defines data members and member functions, while an object is an instance of that class. Both are fundamental concepts of Object-Oriented Programming.

---

**Prepared by:** Muhammad Ali  
**Subject:** Object Oriented Programming  
**Topic:** 08 — Class and Object
```