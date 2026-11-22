# 20 — Projection

## Important Points

- [Introduction](#introduction)
- [Definition](#definition)
- [Symbol](#symbol)
- [Syntax](#syntax)
- [Example](#example)
- [Characteristics](#characteristics)
- [Selection vs Projection](#selection-vs-projection)
- [Conclusion](#conclusion)

---

## Introduction

Projection is a relational algebra operation used to retrieve specific columns from a relation.

## Definition

Projection is a unary relational algebra operation that selects specified attributes or columns from a relation.

---

## Symbol

Projection is represented by the Greek letter Pi (π).

## Syntax

π Attribute1, Attribute2 (Relation)

Example:

π Name, Age (Student)

---

## Example

**Student Table**

| Student_ID | Name | Age |
|---|---|---|
| 101 | Ali | 20 |
| 102 | Ahmed | 21 |
| 103 | Usman | 19 |

Expression:

π Name, Age (Student)

**Result:**

| Name | Age |
|---|---|
| Ali | 20 |
| Ahmed | 21 |
| Usman | 19 |

---

## Characteristics

- Selects columns from a relation.
- Does not require a condition.
- Is a unary operation.
- Removes duplicate tuples in formal relational algebra.
- The number of result columns may be smaller.
- The result contains only selected attributes.

---

## Selection vs Projection

| Selection | Projection |
|---|---|
| Selects rows. | Selects columns. |
| Uses Sigma (σ). | Uses Pi (π). |
| Usually uses conditions. | Specifies required attributes. |
| Reduces the number of rows. | Reduces the number of columns. |

---

## Conclusion

Projection (π) retrieves specific attributes from a relation and removes duplicate tuples in formal relational algebra.