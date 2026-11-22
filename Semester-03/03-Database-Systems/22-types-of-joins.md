# 22 — Types of Joins

## Important Points

- [Introduction](#introduction)
- [Definition](#definition)
- [Inner Join](#inner-join)
- [Theta Join](#theta-join)
- [Equi Join](#equi-join)
- [Natural Join](#natural-join)
- [Outer Join](#outer-join)
- [Left Outer Join](#left-outer-join)
- [Right Outer Join](#right-outer-join)
- [Full Outer Join](#full-outer-join)
- [Conclusion](#conclusion)

---

## Introduction

Join is a relational algebra operation used to combine related data from two or more relations.

## Definition

A Join is a relational algebra operation that combines tuples from two relations based on a specified condition.

---

## 1. Inner Join

### Definition

An Inner Join returns only those rows from two relations that satisfy the join condition.

### Example

Combining Student and Department records where Department_ID matches.

---

## 2. Theta Join

### Definition

A Theta Join combines tuples from two relations using a comparison condition such as =, <, >, <=, or >=.

### Example

Student.Age > Course.Minimum_Age

---

## 3. Equi Join

### Definition

An Equi Join is a type of Theta Join that uses only the equality (=) operator to combine relations.

### Example

Student.Department_ID = Department.Department_ID

---

## 4. Natural Join

### Definition

A Natural Join automatically combines two relations using columns with the same name and compatible domains.

It displays the common join column only once.

### Example

Student ⋈ Department

If both relations contain Department_ID, the join uses that common attribute.

---

## 5. Outer Join

### Definition

An Outer Join returns matching rows and also includes certain non-matching rows with NULL values for missing attributes.

### Types of Outer Join

**A. Left Outer Join**

Returns all rows from the left relation and matching rows from the right relation.

Non-matching right-side values are represented by NULL.

**B. Right Outer Join**

Returns all rows from the right relation and matching rows from the left relation.

Non-matching left-side values are represented by NULL.

**C. Full Outer Join**

Returns all rows from both relations.

Matching rows are combined, while non-matching values are represented by NULL.

---

## Conclusion

Joins combine related data from multiple relations. Common types include Inner Join, Theta Join, Equi Join, Natural Join, and Outer Join.