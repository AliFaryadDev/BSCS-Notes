36 — Operator Overloading

1. Introduction

Operator overloading is a feature of C++ that allows existing operators to work with class objects.

For example, the "+" operator normally adds two numbers. With operator overloading, it can also be used to add two objects.

2. Definition

Operator overloading allows programmers to give additional meanings to existing operators so they can perform operations on user-defined data types.

3. Purpose of Operator Overloading

It makes operations on objects easier and code more readable.

Main purposes:

1. Makes code easier to understand.
2. Simplifies operations on objects.
3. Provides natural syntax.
4. Allows operators to work with user-defined data types.

Example:

Without operator overloading:

result = obj1.add(obj2);

With operator overloading:

result = obj1 + obj2;

4. Syntax of Operator Overloading

return_type operator symbol(parameters)
{
    // Function body
}

Explanation:

- "return_type": Type of returned value.
- "operator": Keyword used for overloading.
- "symbol": Operator to be overloaded.
- "parameters": Values or objects passed to the function.

5. Working of Operator Overloading

When an overloaded operator is used with objects, the compiler calls its operator function.

Example:

obj3 = obj1 + obj2;

It works like:

obj3 = obj1.operator+(obj2);

This is the member-function form of operator overloading.

6. Rules of Operator Overloading

1. Only existing operators can be overloaded.
2. New operators cannot be created.
3. Operator precedence cannot be changed.
4. Operator associativity cannot be changed.
5. The number of operands cannot be changed.
6. At least one operand must be a user-defined data type.

7. Operators That Cannot Be Overloaded

Operator| Name
"::"| Scope Resolution
"."| Member Access
".*"| Pointer-to-Member
"?:"| Conditional Operator
"sizeof"| Size Operator
"typeid"| Type Identification
"alignof"| Alignment Operator

8. Advantages

1. Makes code easier to read.
2. Simplifies operations on objects.
3. Provides natural syntax.
4. Improves code readability.

9. Conclusion

Operator overloading allows existing operators to work with user-defined data types. It makes C++ programs simpler and easier to understand.

---

Next Topics:

- 37 — Overloading Binary Operators
- 38 — Overloading Unary Operators
- 39 — Overloading ++ Operator
- 40 — Overloading -- Operator