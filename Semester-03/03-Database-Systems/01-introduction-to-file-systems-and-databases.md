# Introduction to File Systems

## Key Topics
* [1. Core Definition](#1-core-definition)
* [2. Core Functions (Manages vs. Organizes)](#2-core-functions-manages-vs-organizes)
* [3. Key Components of a File System](#3-key-components-of-a-file-system)
* [4. Traditional File Processing Approach](#4-traditional-file-processing-approach)

---

## 1. Core Definition
* **File System:** An Operating System (OS) component that controls how data is stored, organized, named, and retrieved on a storage device (like an HDD or SSD) using unstructured files and folders.
* **Purpose:** Without a file system, storage media would just be one large, unorganized block of data with no way to tell where one piece of information ends and another begins.

---

## 2. Core Functions (Manages vs. Organizes)

### Manages
* **Meaning:** Controlling the lifecycle of data and files, plus who can access them.
* **Examples:** Creating, reading, updating, deleting (CRUD), renaming files, and setting file permissions.

### Organizes
* **Meaning:** Arranging data in a logical hierarchy and clear order so it is easy to find.
* **Examples:** Creating directories (folders) and subdirectories (subfolders), and assigning file paths (e.g., `C:\Users\Documents\notes.md`).

---

## 3. Key Components of a File System
* **Files:** Basic logical units of storage that hold raw text, records, or binary data.
* **Directories (Folders):** Containers used to group files and other folders together.
* **File Metadata:** Extra information about a file (e.g., file name, size, creation date, file type/extension, and access permissions).
* **Storage Allocation:** Tracking physical space on a disk to know which sector or block holds which file.

---

## 4. Traditional File Processing Approach
* **How it Works:** In older (and simple) software systems, each department or application created its own separate files and custom programs.
* **Example:** In a university, the Accounts department might keep its own `fees.txt` file and the Examination department might keep its own `results.txt` file, with separate C/C++ programs written for each.
* **Focus:** The structure of stored data was hardcoded directly inside the application code.

---

# Introduction to Databases

## Key Topics (Databases)
* [1. What is a Database?](#1-what-is-a-database)
* [2. What is a DBMS?](#2-what-is-a-dbms)
* [3. File System vs. Database](#3-file-system-vs-database)
* [4. Core Database Concepts](#4-core-database-concepts)
* [5. Simple SQL Example (MySQL)](#5-simple-sql-example-mysql)

---

## 1. What is a Database?
* **Database:** An organized collection of structured data stored electronically so it can be easily **stored**, **retrieved**, **updated**, and **managed**.
* **Data:** Raw facts and figures without context (e.g., a student's name `"Ali"` or marks `85`).
* **Information:** Processed, organized, and meaningful data (e.g., `"Ali scored 85 marks"`).
* **Purpose:** Gives you a clean, structured place to keep data so working with many records is fast and dependable.

---

## 2. What is a DBMS?
* **DBMS (Database Management System):** Software that lets users and applications create, read, update, and manage a database (e.g., **MySQL**, PostgreSQL, Oracle).
* **How it Helps:** In a traditional file system, you manage file layouts inside your code; in a DBMS, the database engine handles storage, structure, and access automatically.
* **Query Language (SQL):** Instead of writing custom C/C++ loops for every search or update, you use simple commands (like `SELECT` or `INSERT`) to work with your data.

---

## 3. File System vs. Database

| Feature | Traditional File System | Database System (DBMS) |
| :--- | :--- | :--- |
| **Data & Program Coupling** | Data layout is tightly hardcoded inside the application code | Data and application code stay separate (Data Independence) |
| **Data Redundancy** | The same data is often repeated across different files | Duplicate data is controlled and kept low |
| **Data Integrity & Consistency** | Higher chance of bad data or file corruption | Rules and constraints keep data accurate |
| **Querying & Searching** | Needs custom programs or loops | Fast lookup using structured queries (e.g., SQL) |
| **Multi-User Access** | Shared access and file locking must be coded by hand | Built-in concurrency control and safe transactions |

---

## 4. Core Database Concepts
* **Schema:** The blueprint or overall structure of a database (tables, columns, and their data types).
* **Tables (Relations):** Data arranged into rows (records) and columns (fields/attributes).
* **Keys (Primary Key & Foreign Key):** Columns used to uniquely identify each row and connect related tables together.
* **Normalization:** Arranging tables and columns to cut down duplicate data and avoid insert, update, or delete problems.

---

## 5. Simple SQL Example (MySQL)
Instead of hardcoding byte-by-byte file layouts inside your program, you create a table and run queries:

```sql
CREATE TABLE students (
    student_id INT PRIMARY KEY,
    full_name VARCHAR(100),
    email VARCHAR(100)
);

-- Adding a new column later is easy and safe:
ALTER TABLE students ADD COLUMN middle_name VARCHAR(50);

-- Reading data with a simple query:
SELECT student_id, full_name, middle_name FROM students;
```
