# 06 — Three-Level Schema Architecture

## Important Points

- [Introduction](#introduction)
- [Definition](#definition)
- [External Level](#external-level)
- [Conceptual Level](#conceptual-level)
- [Internal Level](#internal-level)
- [Working](#working-of-three-level-architecture)
- [Advantages](#advantages-of-three-level-schema-architecture)
- [Conclusion](#conclusion)

---

## Introduction

The Three-Level Schema Architecture is used to separate the user's view of data from the physical storage of data.

It makes database systems easier to manage and provides data independence.

## Definition

Three-Level Schema Architecture is a database architecture that divides a database into three levels: External Level, Conceptual Level, and Internal Level.

---

## 1. External Level (View Level)

### Definition

The External Level describes how individual users view and access the database.

### Features

- Provides different views for different users.
- Hides unnecessary information.
- Improves data security.
- Each user sees only relevant data.

### Example

In a college database:

- Students can view their marks.
- Teachers can view student records and marks.
- Accountants can view fee information.

---

## 2. Conceptual Level (Logical Level)

### Definition

The Conceptual Level describes the overall logical structure of the entire database, including entities, attributes, and relationships.

### Features

- Defines what data is stored.
- Defines relationships between data.
- Describes the complete logical database.
- Hides physical storage details.

### Example

A college database contains:

- Student (Student_ID, Name, Age)
- Teacher (Teacher_ID, Name)
- Course (Course_ID, Course_Name)

---

## 3. Internal Level (Physical Level)

### Definition

The Internal Level describes how data is physically stored and organized in storage devices.

### Features

- Defines physical data storage.
- Describes file organization.
- Defines indexes and access paths.
- Focuses on storage efficiency.

### Example

Student records are stored in database files on a hard drive or SSD, using suitable storage structures and indexes.

---

## Working of Three-Level Architecture

The three levels work together:

1. The External Level provides user-specific views.
2. The Conceptual Level defines the complete logical structure.
3. The Internal Level manages physical data storage.

### Simple Structure

External Level (View Level)
          |
Conceptual Level (Logical Level)
          |
Internal Level (Physical Level)
          |
     Stored Data

---

## Advantages of Three-Level Schema Architecture

- Provides data independence.
- Improves data security.
- Supports multiple user views.
- Separates logical and physical data details.
- Makes database maintenance easier.

---

## Conclusion

Three-Level Schema Architecture separates the database into External, Conceptual, and Internal levels. This separation improves security, flexibility, and data independence.