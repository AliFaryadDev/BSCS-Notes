# 25 — Entity Attributes

## Important Points

- [Introduction](#introduction)
- [Definition](#definition)
- [Types of Attributes](#types-of-attributes)
- [Simple Attribute](#simple-attribute)
- [Composite Attribute](#composite-attribute)
- [Single-Valued Attribute](#single-valued-attribute)
- [Multi-Valued Attribute](#multi-valued-attribute)
- [Derived Attribute](#derived-attribute)
- [Key Attribute](#key-attribute)
- [Conclusion](#conclusion)

---

## Introduction

Attributes describe the properties or characteristics of entities in an Entity-Relationship Model.

## Definition

An Entity Attribute is a property or characteristic that describes an entity.

Example:

A Student entity may have Student_ID, Name, Age, and Address attributes.

---

## Types of Attributes

### 1. Simple Attribute

A Simple Attribute cannot be divided into smaller meaningful parts.

Example: Age.

### 2. Composite Attribute

A Composite Attribute can be divided into smaller meaningful attributes.

Example:

Name:
- First_Name
- Middle_Name
- Last_Name

### 3. Single-Valued Attribute

A Single-Valued Attribute contains only one value for each entity.

Example: Date_of_Birth.

### 4. Multi-Valued Attribute

A Multi-Valued Attribute can contain multiple values for one entity.

Example: Phone_Numbers.

### 5. Derived Attribute

A Derived Attribute is calculated from another attribute.

Example: Age can be calculated from Date_of_Birth.

### 6. Key Attribute

A Key Attribute uniquely identifies an entity.

Example: Student_ID.

---

## ER Diagram Symbols

- Simple Attribute: Oval.
- Composite Attribute: Oval connected to smaller ovals.
- Multi-Valued Attribute: Double Oval.
- Derived Attribute: Dashed Oval.
- Key Attribute: Underlined Attribute Name.

---

## Conclusion

Entity Attributes describe the properties of entities. Common types include Simple, Composite, Single-Valued, Multi-Valued, Derived, and Key Attributes.