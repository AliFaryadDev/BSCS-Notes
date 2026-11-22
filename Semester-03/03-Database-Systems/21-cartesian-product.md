# 21 — Cartesian Product

## Important Points

- [Introduction](#introduction)
- [Definition](#definition)
- [Symbol](#symbol)
- [Syntax](#syntax)
- [Working](#working)
- [Example](#example)
- [Characteristics](#characteristics)
- [Conclusion](#conclusion)

---

## Introduction

Cartesian Product is a relational algebra operation that combines every tuple of one relation with every tuple of another relation.

## Definition

Cartesian Product is a binary relational algebra operation that produces all possible combinations of tuples from two relations.

---

## Symbol

Cartesian Product is represented by the multiplication symbol (×).

## Syntax

Relation_A × Relation_B

---

## Working

If Relation A contains M rows and Relation B contains N rows, the Cartesian Product produces:

M × N rows.

The result contains the columns of both relations.

---

## Example

**Student Table**

| Student_ID | Name |
|---|---|
| 1 | Ali |
| 2 | Ahmed |

**Course Table**

| Course_ID | Course_Name |
|---|---|
| C01 | Database |
| C02 | Programming |

Expression:

Student × Course

**Result:**

| Student_ID | Name | Course_ID | Course_Name |
|---|---|---|---|
| 1 | Ali | C01 | Database |
| 1 | Ali | C02 | Programming |
| 2 | Ahmed | C01 | Database |
| 2 | Ahmed | C02 | Programming |

---

## Characteristics

- Combines two relations.
- Produces all possible combinations.
- Is a binary operation.
- If the first relation has M rows and the second has N rows, the result has M × N rows.
- The result contains the columns of both relations.
- Can produce a large number of rows.

---

## Conclusion

Cartesian Product (×) combines every tuple of one relation with every tuple of another relation to produce all possible combinations.