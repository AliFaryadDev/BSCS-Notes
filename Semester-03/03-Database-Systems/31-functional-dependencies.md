
# Functional Dependencies
**Subject: Database Systems (CC-215)**

## Important Points

- [Introduction](#introduction)
- [Definition](#definition)
- [Basic Terminology](#basic-terminology)
- [Notation](#notation)
- [Types of Functional Dependencies](#types-of-functional-dependencies)
- [Determinant and Dependent](#determinant-and-dependent)
- [Armstrong's Axioms](#armstrongs-axioms)
- [Inference Rules](#inference-rules)
- [Attribute Closure](#attribute-closure)
- [Functional Dependency Closure](#functional-dependency-closure)
- [Candidate Key Using Closure](#candidate-key-using-closure)
- [Importance of Functional Dependencies](#importance-of-functional-dependencies)
- [Conclusion](#conclusion)

---

## Introduction

Functional Dependency is an important concept in relational database design.

It describes the relationship between attributes (columns) of a database table.

It helps us understand how one attribute determines the value of another attribute.

Functional Dependencies are also used in database normalization to identify keys and remove data redundancy.

## Definition

A Functional Dependency is a relationship between two sets of attributes in which one set of attributes determines the value of another set of attributes.

In simple words, one attribute or a group of attributes determines another attribute.

**Example:**

A Student ID determines the Student Name.

If we know the Student ID, we can find the name of that student.

## Basic Terminology

### 1. Attribute

An attribute is a column in a database table.

**Example:** Student_ID, Name, Department.

### 2. Functional Dependency (FD)

It is a relationship in which one attribute determines another attribute.

### 3. Determinant

The attribute or group of attributes on the left side of a functional dependency is called the determinant.

### 4. Dependent

The attribute or group of attributes on the right side of a functional dependency is called the dependent attribute.

### 5. Relation

A relation is a table in a relational database.

---

## 4. Notation

Functional Dependency is represented by an arrow (→).

**Notation:**

X → Y

Where:

- X = Determinant
- Y = Dependent
- → = Determines

**Example:**

Student_ID → Student_Name

It means Student_ID determines Student_Name.

If we know the Student_ID, we can identify the corresponding Student_Name.

---

## Types of Functional Dependencies

There are several types of Functional Dependencies.

### 1. Trivial Functional Dependency

A Functional Dependency is called trivial when the right-side attributes are already included in the left-side attributes.

**Example:**

{Student_ID, Name} → Name

Here, Name is already present on the left side.

Therefore, it is a Trivial Functional Dependency.

### 2. Non-Trivial Functional Dependency

A Functional Dependency is called non-trivial when the right-side attributes are not included in the left-side attributes.

**Example:**

Student_ID → Student_Name

Here, Student_Name is not present on the left side.

Therefore, it is a Non-Trivial Functional Dependency.

### 3. Completely Non-Trivial Functional Dependency

A Functional Dependency is completely non-trivial when the left-side and right-side attributes have no common attributes.

**Example:**

Student_ID → Department

Here, both sides have completely different attributes.

Therefore, it is a Completely Non-Trivial Functional Dependency.

### 4. Full Functional Dependency

A Functional Dependency is called full when the dependent attribute depends on the complete determinant, not on any smaller part of it.

**Example:**

(Student_ID, Course_ID) → Grade

Here, both Student_ID and Course_ID are required to determine the Grade.

Neither attribute alone determines the Grade.

Therefore, it is a Full Functional Dependency.

### 5. Partial Functional Dependency

A Functional Dependency is called partial when a dependent attribute depends on only a part of a composite determinant.

**Example:**

(Student_ID, Course_ID) → Student_Name

But:

Student_ID → Student_Name

Here, Student_Name depends only on Student_ID, not on the complete composite determinant.

Therefore, it is a Partial Functional Dependency.

### 6. Transitive Functional Dependency

A Functional Dependency is called transitive when one attribute determines another attribute through an intermediate attribute.

**Example:**

Student_ID → Department_ID

Department_ID → Department_Name

Therefore:

Student_ID → Department_Name

Here, Student_ID determines Department_Name through Department_ID.

Therefore, it is a Transitive Functional Dependency.

---

## Determinant and Dependent

In a Functional Dependency (X → Y):

- X is called the Determinant.
- Y is called the Dependent.

**Example:**

Employee_ID → Employee_Name

- Employee_ID = Determinant
- Employee_Name = Dependent

The determinant determines the value of the dependent attribute.

---

## Armstrong's Axioms

Armstrong's Axioms are a set of rules used to derive new Functional Dependencies from existing Functional Dependencies.

There are three basic Armstrong's Axioms.

### 1. Reflexivity Rule

If Y is a subset of X, then X determines Y.

**Rule:**

If Y ⊆ X, then X → Y.

**Example:**

(Student_ID, Name) → Name

### 2. Augmentation Rule

If X determines Y, then adding the same attribute set to both sides keeps the dependency valid.

**Rule:**

If X → Y, then XZ → YZ.

**Example:**

If:

Student_ID → Name

Then:

(Student_ID, Course_ID) → (Name, Course_ID)

### 3. Transitivity Rule

If X determines Y and Y determines Z, then X determines Z.

**Rule:**

If X → Y and Y → Z, then X → Z.

**Example:**

Student_ID → Department_ID

Department_ID → Department_Name

Therefore:

Student_ID → Department_Name

---

## Inference Rules

Inference rules are additional rules used to derive Functional Dependencies.

### 1. Union Rule

If X determines Y and X determines Z, then X determines both Y and Z.

**Rule:**

If X → Y and X → Z, then X → YZ.

### 2. Decomposition Rule

If X determines YZ, then X determines Y and X determines Z separately.

**Rule:**

If X → YZ, then:

X → Y

X → Z

### 3. Pseudotransitivity Rule

If X determines Y and WY determines Z, then WX determines Z.

**Rule:**

If X → Y and WY → Z, then WX → Z.

---

## Attribute Closure

Attribute Closure is the set of all attributes that can be determined by a given set of attributes using the available Functional Dependencies.

It is represented by X⁺ (X Closure).

**Purpose:**

- To find candidate keys.
- To check Functional Dependencies.
- To determine all attributes that can be identified using a given attribute set.

### Example

Consider the relation:

R(A, B, C, D)

Functional Dependencies:

A → B

B → C

C → D

Find A⁺.

**Step 1: Start with A**

A⁺ = {A}

**Step 2: Apply A → B**

A⁺ = {A, B}

**Step 3: Apply B → C**

A⁺ = {A, B, C}

**Step 4: Apply C → D**

A⁺ = {A, B, C, D}

**Final Answer:**

A⁺ = {A, B, C, D}

Therefore, A determines all attributes of the relation.

So, A is a Candidate Key if it is minimal.

---

## Functional Dependency Closure

Functional Dependency Closure is the set of all Functional Dependencies that can be logically derived from a given set of Functional Dependencies.

It is represented by F⁺.

**Example:**

Given:

F = { A → B, B → C }

Using the Transitivity Rule:

A → C

Therefore:

F⁺ includes:

- A → B
- B → C
- A → C
- Other dependencies that follow from the given rules.

**Important Difference:**

- Attribute Closure (X⁺) finds all attributes determined by X.
- Functional Dependency Closure (F⁺) finds all dependencies derived from F.

---

## Candidate Key Using Closure

A Candidate Key is a minimal set of attributes that can uniquely identify every record in a table.

Attribute Closure helps us find candidate keys.

### Example

Consider:

R(A, B, C, D)

Functional Dependencies:

A → B

B → C

C → D

Find the Candidate Key.

**Step 1: Find A⁺**

A⁺ = {A, B, C, D}

**Step 2: Check all attributes**

A⁺ contains all attributes of the relation.

**Step 3: Check minimality**

A is a single attribute, so it has no smaller non-empty subset.

**Final Answer:**

A is the Candidate Key.

---

## Importance of Functional Dependencies

Functional Dependencies are important because:

1. They describe relationships between attributes.
2. They help identify candidate keys.
3. They help maintain data integrity.
4. They help identify partial and transitive dependencies.
5. They are used in database normalization.
6. They help reduce data redundancy.
7. They improve database design.

---

## Conclusion

Functional Dependencies describe how one attribute or a group of attributes determines another attribute.

They are an important part of relational database design.

They help identify keys, understand attribute relationships, and perform normalization to create a well-organized database.
