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
* **Meaning:** Data aur files ke lifecycle aur access ko control karna.
* **Examples:** Creating, reading, updating, deleting (CRUD), renaming files, aur file permissions set karna.

### Organizes
* **Meaning:** Data ko logical hierarchy aur proper order mein arrange karna taake dhoondna aasan ho.
* **Examples:** Directories (folders) aur subdirectories (subfolders) banana, aur file paths assign karna (e.g., `C:\Users\Documents\notes.md`).

---

## 3. Key Components of a File System
* **Files:** Basic logical units of storage jin mein raw text, records, ya binary data mehfooz hota hai.
* **Directories (Folders):** Containers jo files aur doosre folders ko group karne ke liye istemal hote hain.
* **File Metadata:** File ke baare mein izafi maloomat (e.g., file name, size, creation date, file type/extension, aur access permissions).
* **Storage Allocation:** Disk par physical space track karna ke kaun si file kis sector ya block mein pari hai.

---

## 4. Traditional File Processing Approach
* **How it Works:** Purane (aur simple) software systems mein har department ya application apni alag files aur custom programs banati thi.
* **Example:** Ek university mein Accounts department ki apni `fees.txt` file hoti thi aur Examination department ki apni `results.txt` file, jinke liye alag-alag C/C++ programs likhe jate thay.
* **Focus:** Data storage ka structure seedha application code ke andar hardcode hota tha.

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
* **Purpose:** Provides a central, structured place to keep data so managing large amounts of records becomes fast and reliable.

---

## 2. What is a DBMS?
* **DBMS (Database Management System):** Software that allows users and applications to create, read, update, and manage a database (e.g., **MySQL**, PostgreSQL, Oracle).
* **How it Helps:** Unlike a traditional file system where you manually handle file layouts in your code, the DBMS engine automatically manages storage, structure, and access.
* **Query Language (SQL):** Instead of writing custom C/C++ loops for every search or update, you use simple commands (like `SELECT` or `INSERT`) to interact with your data.

---

## 3. File System vs. Database

| Feature | Traditional File System | Database System (DBMS) |
| :--- | :--- | :--- |
| **Data & Program Coupling** | Data structure is tightly hardcoded inside the application code | Data and application code are independent (Data Independence) |
| **Data Redundancy** | Same data is often duplicated across separate files | Redundancy is controlled and minimized |
| **Data Integrity & Consistency** | Higher risk of invalid data or file corruption | Built-in rules and constraints keep data accurate |
| **Querying & Searching** | Requires writing custom programs or loops | Fast access using structured queries (e.g., SQL) |
| **Multi-User Access** | Concurrent access and file locking must be coded manually | Built-in concurrency control and safe transactions |

---

## 4. Core Database Concepts
* **Schema:** The overall blueprint or logical structure of a database (tables, columns, and their data types).
* **Tables (Relations):** Data organized into rows (records/tuples) and columns (fields/attributes).
* **Keys (Primary Key & Foreign Key):** Special columns used to uniquely identify each row and link related tables together.
* **Normalization:** Organizing tables and columns to reduce duplicate data and prevent insert, update, or delete anomalies.

---

## 5. Simple SQL Example (MySQL)
Instead of hardcoding byte-by-byte file layouts inside your program, you define a table and run queries:

```sql
CREATE TABLE students (
    student_id INT PRIMARY KEY,
    full_name VARCHAR(100),
    email VARCHAR(100)
);

-- Adding a new column later is simple and safe:
ALTER TABLE students ADD COLUMN middle_name VARCHAR(50);

-- Retrieving data with a simple query:
SELECT student_id, full_name, middle_name FROM students;
```
