# 14 — Attributes, Schemas, Tuples, and Domains

## Important Points

- [Introduction](#introduction)
- [Attributes](#attributes)
- [Schemas](#schemas)
- [Tuples](#tuples)
- [Domains](#domains)
- [Example](#example)
- [Conclusion](#conclusion)

---

## Introduction

Attributes, Schemas, Tuples, and Domains are fundamental concepts of the Relational Data Model.

They describe the structure of a relation and the values stored in it.

---

## Attributes

### Definition

An Attribute is a column in a relation that represents a property of an entity.

Example: Student_ID, Name, Age.

---

## Schemas

### Definition

A Relation Schema is the logical structure or design of a relation. It defines the relation name and its attributes.

### Example

Student(Student_ID, Name, Age)

Here:
- Student is the relation name.
- Student_ID, Name, and Age are attributes.

---

## Tuples

### Definition

A Tuple is a single row or record in a relation.

### Example

(101, Ali, 20)

This tuple represents one student record.

---

## Domains

### Definition

A Domain is the set of all valid values that an attribute can contain.

### Examples

- Age: Positive integer values within the defined range.
- Name: Character strings.
- Date_of_Birth: Valid date values.
- Email: Values following the defined email format.

---

## Example

**Student Relation**

| Student_ID | Name | Age |
|---|---|---|
| 101 | Ali | 20 |
| 102 | Ahmed | 21 |

In this relation:

- Relation: Student
- Attributes: Student_ID, Name, Age
- Tuples: (101, Ali, 20) and (102, Ahmed, 21)
- Domains: Valid values allowed for each attribute.
- Schema: Student(Student_ID, Name, Age)

---

## Conclusion

Attributes define columns, schemas define relation structures, tuples represent records, and domains define the valid values of attributes.