# 11 — Tables and Their Characteristics

## Important Points

- [Introduction](#introduction)
- [Definition](#definition)
- [Rows](#rows)
- [Columns](#columns)
- [Characteristics of Tables](#characteristics-of-tables)
- [Example](#example)
- [Conclusion](#conclusion)

---

## Introduction

In a relational database, data is stored in tables. Each table represents an entity or a specific type of information.

## Definition

A Table is a collection of related data organized into rows and columns in a relational database.

---

## Rows

A Row represents a single record in a table.

Example: Information about one student.

A row is also called a Tuple.

## Columns

A Column represents a specific property or attribute of the data.

Example: Student_ID, Name, Age.

A column is also called an Attribute.

---

## Characteristics of Tables

- Each table has a unique name within its database schema.
- Each column has a unique name within its table.
- Each column contains values of a defined domain or data type.
- Each cell contains a single value in the relational model.
- Each row represents one record.
- The order of rows is not important.
- The order of columns is not important.
- Duplicate rows are not allowed in a formal relation.
- A key can uniquely identify each row.

---

## Example

| Student_ID | Name | Age |
|---|---|---|
| 101 | Ali | 20 |
| 102 | Ahmed | 21 |
| 103 | Usman | 19 |

In this table:

- Table Name: Student
- Rows: 3 student records
- Columns: Student_ID, Name, Age
- Student_ID: Identifies each student.

---

## Conclusion

Tables are the basic structures of relational databases. They organize data into rows and columns for easy storage and retrieval.