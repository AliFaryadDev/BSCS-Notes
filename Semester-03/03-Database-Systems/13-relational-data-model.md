# 13 — Relational Data Model

## Important Points

- [Introduction](#introduction)
- [Definition](#definition)
- [Components](#components)
- [Characteristics](#characteristics)
- [Example](#example)
- [Advantages](#advantages)
- [Conclusion](#conclusion)

---

## Introduction

The Relational Data Model is one of the most widely used database models. It organizes data into tables and establishes relationships between them.

## Definition

The Relational Data Model is a database model that represents data in the form of tables consisting of rows and columns.

---

## Components

### 1. Relation

A Relation is a table that stores related data.

### 2. Tuple

A Tuple represents a single row or record in a relation.

### 3. Attribute

An Attribute represents a column or property of a relation.

### 4. Domain

A Domain is the set of permitted values for an attribute.

### 5. Keys

Keys identify records and establish relationships between relations.

### 6. Integrity Constraints

Integrity Constraints are rules that maintain the accuracy and validity of data.

---

## Characteristics

- Data is organized into tables.
- Each table has a unique name within its schema.
- Each row represents a record.
- Each column represents an attribute.
- Each cell contains a single value.
- Keys identify records.
- Relationships are established through keys.
- Integrity constraints maintain valid data.

---

## Example

**Student Table**

| Student_ID | Name | Age |
|---|---|---|
| 101 | Ali | 20 |
| 102 | Ahmed | 21 |

**Course Table**

| Course_ID | Course_Name |
|---|---|
| C01 | Database |
| C02 | Programming |

**Enrollment Table**

| Student_ID | Course_ID |
|---|---|
| 101 | C01 |
| 102 | C02 |

The Enrollment table connects students with their courses.

---

## Advantages

- Simple tabular structure.
- Easy data retrieval using SQL.
- Supports relationships between tables.
- Maintains data integrity.
- Reduces unnecessary data duplication through good database design.

---

## Conclusion

The Relational Data Model organizes data into tables and uses keys and constraints to manage relationships and maintain data accuracy.