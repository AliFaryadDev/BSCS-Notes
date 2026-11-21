
# Inline Functions

**Subject:** Object Oriented Programming (OOP)  
**Language:** C++

## Important Points
- [Introduction](#introduction)
- [Definition](#definition)
- [Purpose](#purpose)
- [Syntax](#syntax)
- [Example](#example)
- [Working](#working)
- [Advantages](#advantages)
- [Disadvantages](#disadvantages)
- [Conclusion](#conclusion)

## Introduction

Inline Functions are a feature of C++ that can help reduce function call overhead. They are useful for small and simple functions.

## Definition

An Inline Function is a function declared with the `inline` keyword, suggesting that the compiler replace the function call with the function's code.

## Purpose

The main purposes of inline functions are:

- To reduce function call overhead.
- To improve performance for small functions.
- To make simple function calls more efficient.
- To avoid repeated function call operations.

## Syntax

```cpp
inline returnType functionName(parameters) {
    // Function body
}
```

## Example

```cpp
#include <iostream>
using namespace std;

inline int square(int x) {
    return x * x;
}

int main() {
    cout << square(5);

    return 0;
}
```

**Output:**
```text
25
```

## Working

- `inline` is a keyword used to declare an inline function.
- `square()` is an inline function.
- It takes an integer `x` as an argument.
- It returns the square of `x`.
- `square(5)` calls the function with value 5.
- The result 25 is displayed.
- The compiler may replace the function call with the function's code.

## Advantages

- Can reduce function call overhead.
- Useful for small and simple functions.
- May improve program performance.
- Makes frequently called small functions more efficient.

## Disadvantages

- May increase program size if used excessively.
- Not suitable for large and complex functions.
- The compiler may ignore the inline request.
- Excessive inlining can negatively affect performance.

## Conclusion

An Inline Function is a function declared with the `inline` keyword. It suggests that the compiler replace function calls with the function's code. It is generally useful for small and simple functions.

---

**Prepared by:** Muhammad Ali  
**Subject:** Object Oriented Programming  
**Topic:** 15 — Inline Functions
