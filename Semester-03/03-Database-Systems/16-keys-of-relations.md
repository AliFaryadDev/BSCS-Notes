# 16 — Keys of Relations

## Important Points

- [Introduction](#introduction)
- [Definition](#definition)
- [Super Key](#super-key)
- [Candidate Key](#candidate-key)
- [Primary Key](#primary-key)
- [Alternate Key](#alternate-key)
- [Foreign Key](#foreign-key)
- [Composite Key](#composite-key)
- [Example](#example)
- [Conclusion](#conclusion)

---

## Introduction

Keys of Relations are used in the Relational Data Model to identify tuples uniquely and establish relationships between relations.

## Definition

A Key of a Relation is an attribute or combination of attributes used to uniquely identify tuples in a relation.

---

## Types of Keys

### 1. Super Key

A Super Key is any set of one or more attributes that uniquely identifies a tuple.

Example: Student_ID or Student_ID + Name.

### 2. Candidate Key

A Candidate Key is a minimal super key. It uniquely identifies a tuple without unnecessary attributes.

Example: Student_ID or Email, if both are unique.

### 3. Primary Key

A Primary Key is the candidate key selected to uniquely identify tuples in a relation.

Features:
- Unique values.
- No NULL values.
- One primary key constraint per table.

### 4. Alternate Key

An Alternate Key is a candidate key that is not selected as the primary key.

Example: Email, when Student_ID is selected as the primary key.

### 5. Foreign Key

A Foreign Key is an attribute or set of attributes that references a candidate key in another or the same relation.

Example: Department_ID in Employee references Department_ID in Department.

### 6. Composite Key

A Composite Key consists of two or more attributes that together uniquely identify a tuple.

Example: Student_ID + Course_ID in Enrollment.

---

## Example

**Student Table**

| Student_ID | Email | Name |
|---|---|---|
| 101 | ali@email.com | Ali |
| 102 | ahmed@email.com | Ahmed |

In this table:
- Super Keys: Student_ID, Email, Student_ID + Name.
- Candidate Keys: Student_ID, Email.
- Primary Key: Student_ID.
- Alternate Key: Email.

---

## Conclusion

Keys of Relations help uniquely identify tuples and establish relationships between different relations. They are essential for maintaining database integrity.