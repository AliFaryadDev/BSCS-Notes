# 17 — Integrity Constraints

## Important Points

- [Introduction](#introduction)
- [Definition](#definition)
- [Types of Integrity Constraints](#types-of-integrity-constraints)
- [Domain Constraint](#domain-constraint)
- [Key Constraint](#key-constraint)
- [Entity Integrity](#entity-integrity)
- [Referential Integrity](#referential-integrity)
- [Other Constraints](#other-constraints)
- [Conclusion](#conclusion)

---

## Introduction

Integrity Constraints are rules applied to a database to maintain the accuracy, validity, and consistency of stored data.

## Definition

Integrity Constraints are rules that ensure data entered into a database is accurate, valid, and consistent.

---

## Types of Integrity Constraints

### 1. Domain Constraint

A Domain Constraint ensures that an attribute contains only values from its defined domain.

Example:

Age must contain valid integer values within the specified range.

### 2. Key Constraint

A Key Constraint ensures that key values uniquely identify records.

Example:

Two students cannot have the same Student_ID if it is a primary key.

### 3. Entity Integrity Constraint

Entity Integrity ensures that a primary key cannot contain NULL values.

Example:

Student_ID cannot be NULL in the Student table when it is the primary key.

### 4. Referential Integrity Constraint

Referential Integrity ensures that a foreign key value matches an existing candidate key value in the referenced table, or is NULL when permitted.

Example:

A Department_ID in the Employee table must refer to an existing Department_ID in the Department table.

---

## Other Database Constraints

### NOT NULL

Ensures that a column cannot contain NULL values.

### UNIQUE

Ensures that values in a column or combination of columns are unique.

### CHECK

Ensures that values satisfy a specified condition.

Example:

Age >= 18

### DEFAULT

Provides a default value when no value is supplied for a column.

---

## Conclusion

Integrity Constraints maintain data accuracy and consistency. Important types include Domain, Key, Entity Integrity, and Referential Integrity Constraints.