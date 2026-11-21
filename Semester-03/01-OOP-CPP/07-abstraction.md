
# Abstraction

**Subject:** Object Oriented Programming (OOP)  
**Language:** C++

## Important Points
- [Introduction](#introduction)
- [Definition](#definition)
- [Purpose](#purpose)
- [Access to Abstraction](#access-to-abstraction)
- [Syntax](#syntax)
- [Example](#example)
- [Working](#working)
- [Advantages](#advantages)
- [Conclusion](#conclusion)

## Introduction

Abstraction is an important concept of Object-Oriented Programming. It hides unnecessary implementation details and shows only essential information to the user.

## Definition

Abstraction is the process of hiding implementation details and showing only essential features of an object.

## Purpose

The main purposes of abstraction are:

- To hide unnecessary details.
- To show only essential information.
- To reduce complexity.
- To make programs easier to use and understand.
- To improve security.

## Access to Abstraction

In C++, abstraction can be achieved using:

- **Classes:** They combine data and functions and provide controlled access to their members.
- **Access Specifiers:** Private and protected members help hide internal details.
- **Abstract Classes:** Classes containing at least one pure virtual function.

## Syntax

```cpp
class Example {
private:
    int data;

public:
    void show() {
        cout << "Hello";
    }
};
```

## Example

```cpp
#include <iostream>
using namespace std;

class Car {
private:
    int speed = 100;

public:
    void showSpeed() {
        cout << "Speed: " << speed;
    }
};

int main() {
    Car c;
    c.showSpeed();

    return 0;
}
```

## Working

- The `Car` class contains a private variable `speed`.
- The private variable cannot be accessed directly outside the class.
- The public function `showSpeed()` displays the speed.
- The user can access the required information without knowing the internal implementation.

## Advantages

- Reduces program complexity.
- Hides unnecessary implementation details.
- Improves code security.
- Makes code easier to maintain.
- Provides a simple interface to users.

## Conclusion

Abstraction hides unnecessary implementation details and shows only essential features. It makes programs simpler, easier to use, and maintain.

---

**Prepared by:** Muhammad Ali  
**Subject:** Object Oriented Programming  
**Topic:** 07 — Abstraction
