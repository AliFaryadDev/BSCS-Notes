
# Overloaded Operators of Standard Library

**Subject:** Object Oriented Programming (OOP)  
**Language:** C++

## Important Points
- [Introduction](#introduction)
- [Definition](#definition)
- [Purpose](#purpose)
- [Common Operators](#common-operators)
- [Examples](#examples)
- [Working](#working)
- [Advantages](#advantages)
- [Conclusion](#conclusion)

## Introduction

Operator Overloading is a feature of C++ that allows operators to perform specific operations on objects. The C++ Standard Library also provides overloaded operators for its built-in classes and types.

## Definition

Overloaded Operators of the Standard Library are operators that have predefined overloaded implementations for standard library types, allowing objects to be used with familiar operators.

## Purpose

The main purposes of overloaded operators are:

- To perform operations on standard library objects.
- To make code easier to read.
- To provide familiar ways to work with objects.
- To support operations such as comparison and concatenation.
- To simplify programming.

## Common Operators

Some common examples of overloaded operators in the C++ Standard Library are:

| Operator | Purpose | Example |
|---|---|---|
| `+` | String concatenation | `s1 + s2` |
| `==` | Equality comparison | `s1 == s2` |
| `!=` | Inequality comparison | `s1 != s2` |
| `<` | Less-than comparison | `a < b` |
| `[]` | Element access | `v[0]` |
| `<<` | Output stream | `cout << x` |
| `>>` | Input stream | `cin >> x` |

## Examples

### Example 1: String Concatenation

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string first = "Hello ";
    string second = "Ali";

    string result = first + second;

    cout << result;

    return 0;
}
```

**Output:**

```text
Hello Ali
```

### Example 2: String Comparison

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string a = "Ali";
    string b = "Ali";

    if (a == b) {
        cout << "Strings are equal";
    }

    return 0;
}
```

**Output:**

```text
Strings are equal
```

### Example 3: Vector Element Access

```cpp
#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> numbers = {10, 20, 30};

    cout << numbers[0];

    return 0;
}
```

**Output:**

```text
10
```

## Working

- The C++ Standard Library provides classes such as `string` and `vector`.
- These classes support overloaded operators.
- The `+` operator joins two strings.
- The `==` operator compares two strings.
- The `[]` operator accesses an element of a vector.
- These operators make working with standard library objects easier.

## Advantages

- Improves code readability.
- Makes operations easier to perform.
- Provides familiar operator syntax.
- Reduces complex function calls.
- Makes standard library classes easier to use.

## Conclusion

The C++ Standard Library provides overloaded operators for many standard types and classes. These operators make operations such as string concatenation, comparison, and element access simple and readable.

---

**Prepared by:** Muhammad Ali  
**Subject:** Object Oriented Programming  
**Topic:** 35 — Overloaded Operators of Standard Library
