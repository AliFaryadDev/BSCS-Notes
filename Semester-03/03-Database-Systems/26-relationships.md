# 26 — Relationships

## Important Points

- [Introduction](#introduction)
- [Definition](#definition)
- [Degree of Relationship](#degree-of-relationship)
- [Unary Relationship](#unary-relationship)
- [Binary Relationship](#binary-relationship)
- [Ternary Relationship](#ternary-relationship)
- [Cardinality Ratios](#cardinality-ratios)
- [Participation Constraints](#participation-constraints)
- [Conclusion](#conclusion)

---

## Introduction

Relationships describe how two or more entities are associated with each other in an Entity-Relationship Model.

## Definition

A Relationship is an association between two or more entities.

Example: A Student enrolls in a Course.

---

## Degree of Relationship

The Degree of a Relationship refers to the number of entity types participating in that relationship.

### 1. Unary Relationship

A Unary Relationship involves one entity type related to itself.

Example: An Employee supervises another Employee.

### 2. Binary Relationship

A Binary Relationship involves two entity types.

Example: A Student enrolls in a Course.

### 3. Ternary Relationship

A Ternary Relationship involves three entity types.

Example: A Supplier supplies a Product to a Project.

---

## Cardinality Ratios

Cardinality describes how many entities can participate in a relationship.

### 1. One-to-One (1:1)

One entity is related to only one entity of another type, and vice versa.

Example: One person has one passport.

### 2. One-to-Many (1:N)

One entity can be related to multiple entities of another type.

Example: One department has many employees.

### 3. Many-to-One (N:1)

Multiple entities are related to one entity of another type.

Example: Many employees work in one department.

### 4. Many-to-Many (M:N)

Multiple entities can be related to multiple entities of another type.

Example: Many students enroll in many courses.

---

## Participation Constraints

Participation describes whether every entity must participate in a relationship.

### 1. Total Participation

Every entity in an entity set must participate in the relationship.

Example: Every employee must belong to a department, according to a particular business rule.

### 2. Partial Participation

Some entities may participate in the relationship, while others may not.

Example: Not every employee supervises another employee.

---

## Conclusion

Relationships connect entities in an ER Model. They are described through degree, cardinality ratios, and participation constraints.