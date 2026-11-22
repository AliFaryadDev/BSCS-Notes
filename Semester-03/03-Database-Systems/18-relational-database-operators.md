# 18 — Relational Database Operators

## Important Points

- [Introduction](#introduction)
- [Definition](#definition)
- [Types of Relational Operators](#types-of-relational-operators)
- [Selection](#selection)
- [Projection](#projection)
- [Union](#union)
- [Set Difference](#set-difference)
- [Intersection](#intersection)
- [Cartesian Product](#cartesian-product)
- [Join](#join)
- [Rename](#rename)
- [Conclusion](#conclusion)

---

## Introduction

Relational Algebra is a procedural query language used to perform operations on relations in a relational database.

It provides a mathematical foundation for relational database operations.

## Definition

Relational Algebra is a formal query language that uses operators to retrieve and manipulate data from relations.

---

## Types of Relational Operators

### 1. Selection (σ)

Selection retrieves rows that satisfy a specified condition.

Example:

σ Age > 18 (Student)

Returns students whose age is greater than 18.

### 2. Projection (π)

Projection retrieves specific columns from a relation.

Example:

π Name, Age (Student)

Returns only Name and Age columns.

### 3. Union (∪)

Union combines tuples from two union-compatible relations and removes duplicates.

Example:

Student_A ∪ Student_B

### 4. Set Difference (−)

Set Difference returns tuples that exist in the first relation but not in the second.

Example:

Student_A − Student_B

### 5. Intersection (∩)

Intersection returns tuples that exist in both relations.

Example:

Student_A ∩ Student_B

### 6. Cartesian Product (×)

Cartesian Product combines every tuple of one relation with every tuple of another relation.

Example:

Student × Course

### 7. Join (⋈)

Join combines related tuples from two relations based on a specified condition.

Example:

Student ⋈ Student.Department_ID = Department.Department_ID Department

### 8. Rename (ρ)

Rename changes the name of a relation or its attributes in a relational algebra expression.

Example:

ρ S(Student) 

Renames Student as S.

---

## Conclusion

Relational Algebra provides operators such as Selection, Projection, Union, Difference, Intersection, Cartesian Product, Join, and Rename to retrieve and manipulate relational data.