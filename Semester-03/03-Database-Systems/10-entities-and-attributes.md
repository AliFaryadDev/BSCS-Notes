# 10 — Entities and Attributes

## Important Points

- [Introduction](#introduction)
- [Entity](#entity)
- [Types of Entities](#types-of-entities)
- [Attribute](#attribute)
- [Types of Attributes](#types-of-attributes)
- [Example](#example)
- [Conclusion](#conclusion)

---

## Introduction

Entities and Attributes are basic concepts of database design. They help describe real-world objects and their properties.

---

## Entity

### Definition

An Entity is a real-world object, person, place, or thing about which data is stored in a database.

### Examples

- Student
- Teacher
- Course
- Employee
- Department

### Types of Entities

**1. Strong Entity**

A Strong Entity has its own primary key and can exist independently.

Example: Student with Student_ID.

**2. Weak Entity**

A Weak Entity cannot be uniquely identified by its own attributes alone and depends on another entity for identification.

Example: Dependent of an Employee.

---

## Attribute

### Definition

An Attribute is a property or characteristic that describes an entity.

### Example

For a Student entity:

- Student_ID
- Name
- Age
- Address
- Email

### Types of Attributes

**1. Simple Attribute**

Cannot be divided into smaller meaningful parts.

Example: Age.

**2. Composite Attribute**

Can be divided into smaller attributes.

Example: Name can be divided into First_Name and Last_Name.

**3. Single-Valued Attribute**

Has only one value for each entity.

Example: Date_of_Birth.

**4. Multi-Valued Attribute**

Can have multiple values for one entity.

Example: Phone_Numbers.

**5. Derived Attribute**

Its value can be calculated from another attribute.

Example: Age can be calculated from Date_of_Birth.

**6. Key Attribute**

Uniquely identifies an entity.

Example: Student_ID.

---

## Conclusion

An Entity represents a real-world object, while an Attribute describes its properties. Both are essential for designing a database.