
# Object Composition

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
- [Conclusion](#conclusion)

## Introduction

Object Composition is an important concept in Object-Oriented Programming (OOP). It allows one class to contain an object of another class as its data member.

## Definition

Object Composition is a relationship in which one class contains an object of another class as a member to build a more complex object.

It represents a **Has-A Relationship**.

## Purpose

The main purposes of Object Composition are:

- To create complex objects using smaller objects.
- To improve code reusability.
- To organize code into separate classes.
- To make programs easier to manage.
- To represent real-world relationships.

## Relationship Between Objects

Object Composition represents a **Has-A Relationship**.

Example:

- A Car has an Engine.
- A House has Rooms.
- A Computer has a Processor.

In these examples, one object contains another object.

## Syntax

```cpp
class ClassA {
public:
    void display() {
        cout << "Class A Function";
    }
};

class ClassB {
private:
    ClassA obj;
};
```

Here, `ClassB` contains an object of `ClassA`.

## Example

```cpp
#include <iostream>
using namespace std;

class Engine {
public:
    void start() {
        cout << "Engine Started";
    }
};

class Car {
private:
    Engine engine;

public:
    void startCar() {
        engine.start();
        cout << "\nCar Started";
    }
};

int main() {
    Car myCar;

    myCar.startCar();

    return 0;
}
```

## Output

```text
Engine Started
Car Started
```

## Working

- `Engine` is a class that contains a `start()` function.
- `Car` is another class.
- The `Car` class contains an object of the `Engine` class.
- This creates a Has-A Relationship between Car and Engine.
- In `main()`, an object of the `Car` class is created.
- The `startCar()` function calls the `start()` function through the Engine object.
- Both messages are displayed on the screen.

## Advantages

- Promotes code reusability.
- Makes programs easier to organize.
- Reduces code duplication.
- Helps create complex objects.
- Improves maintainability.

## Conclusion

Object Composition allows one class to contain objects of other classes. It represents a Has-A Relationship and helps build complex programs using smaller, reusable objects.

---

**Prepared by:** Muhammad Ali  
**Subject:** Object Oriented Programming  
**Topic:** 26 — Object Composition
