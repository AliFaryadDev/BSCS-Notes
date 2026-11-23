# 02 — A File System Critique

## Important Points

- [Traditional File Processing System](#traditional-file-processing-system)
- [Limitations of File System](#limitations-of-file-system)
- [Data Redundancy](#data-redundancy)
- [Data Inconsistency](#data-inconsistency)
- [Data Isolation](#data-isolation)
- [Data Dependence](#data-dependence)
- [Limited Data Sharing](#limited-data-sharing)
- [Security Problems](#security-problems)
- [Integrity Problems](#integrity-problems)
- [Concurrent Access Problems](#concurrent-access-problems)
- [Conclusion](#conclusion)

---

## Traditional File Processing System

### Definition

A Traditional File Processing System is a method in which data is stored and managed in separate files using individual application programs.

### Example

A college may maintain separate files for:

- Student Information
- Teacher Information
- Fee Records
- Examination Results

Each department manages its own files and programs.

---

## Limitations of File System

A traditional File System has the following limitations:

### 1. Data Redundancy

**Definition:**

Data Redundancy occurs when the same data is stored in multiple files or locations unnecessarily.

**Example:**

A student's name and address may be stored separately in admission, examination, and fee records.

**Problem:** It wastes storage space and makes data management difficult.

### 2. Data Inconsistency

**Definition:**

Data Inconsistency occurs when the same data has different values in different files.

**Example:**

A student's address is updated in the admission file but remains unchanged in the fee file.

**Problem:** Different files contain conflicting information.

### Data Isolation

**Definition:**

Data Isolation occurs when data is stored in separate files and different formats, making it difficult to access and combine.

**Example:**

Student information is stored in one file, while examination results are stored in another file.

**Problem:** Retrieving related information becomes difficult.

### Data Dependence

**Definition:**

Data Dependence occurs when application programs depend on the structure and format of stored files.

**Example:**

If the structure of a student file changes, the application program may also need to be modified.

**Problem:** Changes in file structure require changes in application programs.

### 5. Limited Data Sharing

**Definition:**

Limited Data Sharing occurs when data is not easily accessible to multiple users or departments.

**Example:**

The examination department may have difficulty accessing student information maintained by the admission department.

**Problem:** Sharing information becomes difficult.

### 6. Security Problems

**Definition:**

Security Problems occur when a File System does not provide sufficient control over who can access or modify data.

**Example:**

An unauthorized person may access or modify student records.

**Problem:** Important information may be exposed or changed without permission.

### 7. Integrity Problems

**Definition:**

Integrity Problems occur when it is difficult to maintain the accuracy and validity of stored data.

**Example:**

A student's marks may accidentally be entered as 150 out of 100.

**Problem:** Incorrect or invalid data may be stored.

### 8. Concurrent Access Problems

**Definition:**

Concurrent Access Problems occur when multiple users access or modify the same data at the same time without proper coordination.

**Example:**

Two employees update the same student's fee record simultaneously.

**Problem:** Data may be overwritten or become incorrect.

---

## Conclusion

The traditional File System has several limitations, including data redundancy, data inconsistency, data isolation, data dependence, and security problems. These limitations make data management difficult and create the need for a Database Management System (DBMS).