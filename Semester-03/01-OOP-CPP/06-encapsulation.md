# Encapsulation 
**Subject: OOP** | **Language: C++**
## 📄 Important Point
- [Definition](#definition)
- [Purpose](#purpose)
- [Syntax](#syntax)
- [Example](#example)
- [Conclusion](#conclusion)

## Definition

> **Encapsulation** is the process of binding data members and member functions together into a single unit called a class.
## Purpose
The main purpose of Encapsulation is to:
1. Keep data safe from direct access.
2. Allow controlled access to data through member functions.

## Syntax
```cpp
class ClassName {
private:
    // Data members

public:
    // Member functions
};

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

## Result
  >Result is 20

## Conclusion

Encapsulation combines data and related functions into a single class. It keeps data safe and allows access through public member functions.

---
Made with ❤️ by Muhammad Ali

  
  
