# 24 — Entity Sets

## Important Points

- [Introduction](#introduction)
- [Entity](#entity)
- [Entity Set](#entity-set)
- [Types of Entity Sets](#types-of-entity-sets)
- [Strong Entity Set](#strong-entity-set)
- [Weak Entity Set](#weak-entity-set)
- [Entity vs Entity Set](#entity-vs-entity-set)
- [Conclusion](#conclusion)

---

## Introduction

Entity Sets are an important concept in the Entity-Relationship (ER) Model. They represent collections of similar entities.

## Entity

### Definition

An Entity is a real-world object that can be uniquely identified and about which data is stored.

Example: A particular student named Ali.

---

## Entity Set

### Definition

An Entity Set is a collection of similar entities that share the same attributes.

Example: All students in a college form the Student entity set.

---

## Types of Entity Sets

### 1. Strong Entity Set

A Strong Entity Set contains entities that have their own key attribute and can exist independently.

Example: Student with Student_ID.

### 2. Weak Entity Set

A Weak Entity Set contains entities that cannot be uniquely identified by their own attributes alone and depend on an owner entity.

Example: Employee Dependents.

A weak entity is identified using its partial key together with the key of its owner entity.

---

## Entity vs Entity Set

| Entity | Entity Set |
|---|---|
| Represents one individual object. | Represents a collection of similar objects. |
| Example: Ali. | Example: All Students. |
| Is a single instance. | Contains multiple instances. |

---

## Conclusion

An Entity represents an individual real-world object, while an Entity Set represents a collection of similar entities.