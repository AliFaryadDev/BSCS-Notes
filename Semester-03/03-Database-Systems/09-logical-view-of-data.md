# 09 — Logical View of Data

## Important Points

- [Introduction](#introduction)
- [Definition](#definition)
- [Levels of Data View](#levels-of-data-view)
- [Importance](#importance)
- [Example](#example)
- [Conclusion](#conclusion)

---

## Introduction

The Logical View of Data describes what data is stored in a database and how different data items are related to each other.

It focuses on the organization of data rather than its physical storage.

## Definition

Logical View of Data is the way users and database designers understand and organize data, including entities, attributes, and relationships.

---

## Levels of Data View

### 1. Physical View

Describes how data is physically stored in storage devices.

### 2. Logical View

Describes what data is stored and how data is related.

### 3. External View

Describes how individual users see and access specific parts of the database.

---

## Importance

- Makes data easier to understand.
- Defines relationships between data.
- Hides physical storage details.
- Helps database designers organize data.
- Supports data independence.

---

## Example

A college database may contain:

- Student (Student_ID, Name, Age)
- Course (Course_ID, Course_Name)
- Enrollment (Student_ID, Course_ID)

The logical view explains how these entities and their attributes are organized and related.

---

## Conclusion

Logical View of Data describes the structure and relationships of data without focusing on its physical storage.