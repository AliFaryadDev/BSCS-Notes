# 19 — Selection

## Important Points

- [Introduction](#introduction)
- [Definition](#definition)
- [Symbol](#symbol)
- [Syntax](#syntax)
- [Conditions](#conditions)
- [Example](#example)
- [Characteristics](#characteristics)
- [Conclusion](#conclusion)

---

## Introduction

Selection is a relational algebra operation used to retrieve specific rows from a relation based on a condition.

## Definition

Selection is a unary relational algebra operation that selects tuples from a relation that satisfy a specified condition.

---

## Symbol

Selection is represented by the Greek letter Sigma (σ).

## Syntax

σ Condition (Relation)

Example:

σ Age > 18 (Student)

---

## Conditions

Selection can use comparison operators:

- = : Equal to
- != : Not equal to
- > : Greater than
- < : Less than
- >= : Greater than or equal to
- <= : Less than or equal to

Logical operators:

- AND (∧)
- OR (∨)
- NOT (¬)

---

## Example

**Student Table**

| Student_ID | Name | Age |
|---|---|---|
| 101 | Ali | 20 |
| 102 | Ahmed | 17 |
| 103 | Usman | 22 |

Expression:

σ Age > 18 (Student)

**Result:**

| Student_ID | Name | Age |
|---|---|---|
| 101 | Ali | 20 |
| 103 | Usman | 22 |

---

## Characteristics

- Selects rows from a relation.
- Uses specified conditions.
- Does not remove columns.
- Is a unary operation.
- The number of result columns remains the same.
- The number of result rows may be smaller.

---

## Conclusion

Selection (σ) retrieves only those tuples that satisfy a given condition.