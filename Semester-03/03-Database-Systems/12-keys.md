# 12 — Keys

## Important Points

- [Introduction](#introduction)
- [Definition](#definition)
- [Primary Key](#primary-key)
- [Candidate Key](#candidate-key)
- [Super Key](#super-key)
- [Alternate Key](#alternate-key)
- [Foreign Key](#foreign-key)
- [Composite Key](#composite-key)
- [Unique Key](#unique-key)
- [Conclusion](#conclusion)

---

## Introduction

Keys are important components of relational databases. They help uniquely identify records and establish relationships between tables.

## Definition

A Key is an attribute or a combination of attributes used to identify records and establish relationships between tables.

---

## Types of Keys

### 1. Primary Key

A Primary Key is an attribute or combination of attributes that uniquely identifies each record in a table.

**Features:**
- Must contain unique values.
- Cannot contain NULL values.
- Only one primary key constraint is defined per table.

Example: Student_ID.

### 2. Candidate Key

A Candidate Key is a minimal attribute or combination of attributes that can uniquely identify each record.

Example: Student_ID and Email, if both are unique.

### 3. Super Key

A Super Key is any attribute or combination of attributes that uniquely identifies a record.

Example:
- Student_ID
- Student_ID + Name

### 4. Alternate Key

An Alternate Key is a candidate key that is not selected as the primary key.

Example:

If Student_ID is the primary key, Email may be an alternate key.

### 5. Foreign Key

A Foreign Key is an attribute or combination of attributes that references a candidate key, usually the primary key, in another or the same table.

Example: Department_ID in the Employee table references Department_ID in the Department table.

### 6. Composite Key

A Composite Key is a key consisting of two or more attributes used together to uniquely identify a record.

Example: Student_ID + Course_ID in an Enrollment table.

### 7. Unique Key

A Unique Key is a database constraint that ensures values in a column or combination of columns are unique.

Note: NULL handling for UNIQUE constraints depends on the DBMS.

---

## Conclusion

Keys help identify records, prevent unwanted duplication, and establish relationships between tables. Common types include Primary, Candidate, Super, Alternate, Foreign, and Composite Keys.