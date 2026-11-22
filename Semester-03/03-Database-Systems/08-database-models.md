# 08 — Database Models

## Important Points

- [Introduction](#introduction)
- [Definition](#definition)
- [Types of Database Models](#types-of-database-models)
- [Hierarchical Database Model](#1-hierarchical-database-model)
- [Network Database Model](#2-network-database-model)
- [Relational Database Model](#3-relational-database-model)
- [Entity-Relationship Model](#4-entity-relationship-model)
- [Object-Oriented Database Model](#5-object-oriented-database-model)
- [Comparison of Database Models](#comparison-of-database-models)
- [Conclusion](#conclusion)

---

## Introduction

A Database Model defines how data is logically organized, stored, related, and accessed in a database.

Different database models provide different ways to represent and manage data.

## Definition

A Database Model is a logical structure that describes how data is organized, stored, and related within a database.

---

## Types of Database Models

### 1. Hierarchical Database Model

#### Definition

The Hierarchical Database Model organizes data in a tree-like structure in which each child record has only one parent record.

#### Features

- Organizes data in a tree structure.
- Uses parent-child relationships.
- Each child has one parent.
- Supports one-to-many relationships.

#### Example

A university has multiple departments, and each department has multiple students.

**Structure:**

University
  |
Departments
  |
Students

---

### 2. Network Database Model

#### Definition

The Network Database Model organizes data in a graph-like structure in which a record can have multiple parent and child records.

#### Features

- Organizes data in a network structure.
- Supports many-to-many relationships.
- A record can have multiple parents.
- Represents complex relationships.

#### Example

A student can enroll in multiple courses, and each course can have multiple students.

---

### 3. Relational Database Model

#### Definition

The Relational Database Model organizes data into tables consisting of rows and columns.

#### Features

- Stores data in tables.
- Rows represent records.
- Columns represent attributes.
- Uses primary keys to identify records.
- Uses foreign keys to establish relationships.
- SQL is commonly used to manage relational databases.

#### Example

**Student Table**

| Student_ID | Name | Age |
|---|---|---|
| 1 | Ali | 20 |
| 2 | Ahmed | 21 |
| 3 | Usman | 19 |

**Examples of Relational DBMS:**

- MySQL
- Oracle Database
- PostgreSQL
- Microsoft SQL Server

---

### 4. Entity-Relationship Model

#### Definition

The Entity-Relationship (ER) Model represents data using entities, attributes, and relationships.

#### Components

**1. Entity**

An Entity is a real-world object about which data is stored.

Example: Student, Teacher, Course.

**2. Attribute**

An Attribute is a property or characteristic of an entity.

Example: Student_ID, Name, Age.

**3. Relationship**

A Relationship describes the association between two or more entities.

Example: A Student enrolls in a Course.

#### Common ER Diagram Symbols

- Rectangle: Entity
- Oval: Attribute
- Diamond: Relationship
- Underlined Attribute: Key Attribute

---

### 5. Object-Oriented Database Model

#### Definition

The Object-Oriented Database Model stores data in the form of objects, similar to object-oriented programming.

#### Features

- Stores data as objects.
- Supports classes and objects.
- Supports inheritance.
- Supports encapsulation.
- Can represent complex data.

#### Example

A Student object may contain:

- Student_ID
- Name
- Age
- Methods

---

## Comparison of Database Models

| Database Model | Structure | Main Relationship |
|---|---|---|
| Hierarchical | Tree | One-to-Many |
| Network | Graph | Many-to-Many |
| Relational | Tables | Through Keys |
| Entity-Relationship | Diagram | Entities and Relationships |
| Object-Oriented | Objects | Object Relationships |

---

## Conclusion

Database Models define how data is organized and represented in a database. Common models include Hierarchical, Network, Relational, Entity-Relationship, and Object-Oriented models. Each model has its own structure and uses.