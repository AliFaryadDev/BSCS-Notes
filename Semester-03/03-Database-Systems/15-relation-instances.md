# 15 — Relation Instances

## Important Points

- [Introduction](#introduction)
- [Definition](#definition)
- [Relation Schema vs Relation Instance](#relation-schema-vs-relation-instance)
- [Characteristics](#characteristics)
- [Example](#example)
- [Conclusion](#conclusion)

---

## Introduction

A Relation Instance represents the actual data stored in a relation at a particular moment.

It can change whenever records are inserted, updated, or deleted.

## Definition

A Relation Instance is the set of tuples or records present in a relation at a specific point in time.

---

## Relation Schema vs Relation Instance

### Relation Schema

Describes the structure of a relation, including its name and attributes.

Example:

Student(Student_ID, Name, Age)

### Relation Instance

Represents the actual records stored in that relation at a particular time.

Example:

| Student_ID | Name | Age |
|---|---|---|
| 101 | Ali | 20 |
| 102 | Ahmed | 21 |

---

## Characteristics

- Contains actual records of a relation.
- Changes when data is inserted, updated, or deleted.
- Represents the current state of a relation.
- Contains tuples that follow the relation schema.
- Duplicate tuples are not allowed in the formal relational model.

---

## Example

Initially, the Student relation contains:

| Student_ID | Name |
|---|---|
| 101 | Ali |

After inserting another student:

| Student_ID | Name |
|---|---|
| 101 | Ali |
| 102 | Ahmed |

The relation instance has changed, but the relation schema remains the same.

---

## Conclusion

A Relation Schema defines the structure of a relation, while a Relation Instance represents the actual data stored in it at a specific time.