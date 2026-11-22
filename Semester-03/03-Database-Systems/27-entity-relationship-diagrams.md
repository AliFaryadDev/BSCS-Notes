# 27 — Entity-Relationship Diagrams

## Important Points

- [Introduction](#introduction)
- [Definition](#definition)
- [Components of ER Diagram](#components-of-er-diagram)
- [ER Diagram Symbols](#er-diagram-symbols)
- [Cardinality](#cardinality)
- [Participation](#participation)
- [Example](#example)
- [Advantages](#advantages)
- [Conclusion](#conclusion)

---

## Introduction

An Entity-Relationship Diagram (ERD) is a graphical representation of entities, attributes, and relationships in a database.

It is used during database design to visualize how data is organized and connected.

## Definition

An Entity-Relationship Diagram is a visual model that represents entities, their attributes, and the relationships between them.

---

## Components of ER Diagram

### 1. Entity

An Entity represents a real-world object about which data is stored.

Example: Student, Teacher, Course.

### 2. Attribute

An Attribute describes a property of an entity.

Example: Student_ID, Name, Age.

### 3. Relationship

A Relationship represents an association between entities.

Example: Student enrolls in Course.

---

## ER Diagram Symbols

| Symbol | Meaning |
|---|---|
| Rectangle | Entity |
| Double Rectangle | Weak Entity |
| Oval | Attribute |
| Underlined Attribute | Key Attribute |
| Double Oval | Multi-Valued Attribute |
| Dashed Oval | Derived Attribute |
| Diamond | Relationship |
| Double Diamond | Identifying Relationship |
| Line | Connection |
| Double Line | Total Participation |

---

## Cardinality

Cardinality defines the number of entities that can participate in a relationship.

Types:

- One-to-One (1:1)
- One-to-Many (1:N)
- Many-to-One (N:1)
- Many-to-Many (M:N)

---

## Participation

### Total Participation

Every entity must participate in the relationship.

It is represented by a double line.

### Partial Participation

Only some entities participate in the relationship.

It is represented by a single line.

---

## Example

A college database contains Student and Course entities.

**Student Entity:**
- Student_ID
- Name
- Age

**Course Entity:**
- Course_ID
- Course_Name

**Relationship:**

Student enrolls in Course.

A student can enroll in multiple courses, and a course can have multiple students.

Therefore, the relationship is Many-to-Many (M:N).

---

## Advantages of ER Diagrams

- Makes database design easier.
- Provides a visual representation of data.
- Shows relationships between entities.
- Helps identify entities and attributes.
- Improves communication between developers and users.
- Helps convert database requirements into a logical design.

---

## Conclusion

An ER Diagram visually represents entities, attributes, and relationships. It helps database designers understand and plan the structure of a database before implementation.