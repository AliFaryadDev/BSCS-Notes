# 01 — Introduction to File Systems and Databases

## Important Points

- [Introduction](#introduction)
- [File System](#file-system)
- [Database](#database)
- [Database Management System (DBMS)](#database-management-system-dbms)
- [Characteristics of Database](#characteristics-of-database)
- [Advantages of Database System](#advantages-of-database-system)
- [Disadvantages of Database System](#disadvantages-of-database-system)
- [File System vs Database System](#file-system-vs-database-system)
- [Basic Database Operations (CRUD)](#basic-database-operations-crud)
- [Applications of Databases](#applications-of-databases)
- [Conclusion](#conclusion)

---

## Introduction

A **File System** is an operating system component of storing and organizing data in files and folders,while a **database** is a structured system that organizes data into tables to allow querying and management.


**Examples:**
- File System: Storing student information in a `student.txt` file.
- Database: Storing student information in MySQL or Oracle.

---

## File System

### Definition

A File System is a method used by an operating system to store, organize, manage, and retrieve data in files and folders.

### Functions

- **Create:** Creates new files.
- **Store:** Stores data in files.
- **Retrieve:** Reads and accesses stored data.
- **Update:** Modifies existing data.
- **Delete:** Removes files and data.

### Example

A college stores student information in separate files:

- `students.txt`
- `teachers.txt`
- `courses.txt`

---

## Database

### Definition

A Database is an organized collection of related data that is stored electronically and can be easily accessed, managed, and updated.

### Functions

- **Store:** Stores large amounts of data.
- **Retrieve:** Retrieves required information.
- **Insert:** Adds new records.
- **Update:** Modifies existing records.
- **Delete:** Removes unwanted records.

### Example

A college database stores information about:

- Students
- Teachers
- Courses
- Results
- Attendance

---

## Database Management System (DBMS)

### Definition

A Database Management System (DBMS) is software that allows users to create, store, manage, retrieve, and update data in a database.

### Functions

- **Data Management:** Manages stored data.
- **Data Retrieval:** Retrieves required information.
- **Data Security:** Protects data from unauthorized access.
- **Data Integrity:** Maintains accuracy and consistency of data.
- **Backup and Recovery:** Helps restore data after failures.

### Examples

- MySQL
- Oracle Database
- Microsoft SQL Server
- PostgreSQL
- SQLite

---

## Characteristics of Database

- **Organized Data:** Data is stored in a structured and organized way.
- **Data Sharing:** Multiple authorized users can access data.
- **Data Security:** Protects data from unauthorized access.
- **Data Integrity:** Maintains data accuracy and consistency.
- **Reduced Redundancy:** Helps minimize unnecessary duplication of data.
- **Easy Retrieval:** Allows users to find required information easily.

---

## Advantages of Database System

- Reduces unnecessary data duplication.
- Improves data security.
- Provides easy data access and retrieval.
- Supports data sharing among multiple users.
- Maintains data accuracy and consistency.
- Provides backup and recovery facilities.

---

## Disadvantages of Database System

- **High Cost:** Database software and hardware can be expensive.
- **Complexity:** Requires technical knowledge to manage.
- **Maintenance:** Needs regular maintenance and administration.
- **Security Risks:** Unauthorized access can expose large amounts of data.
- **System Failure:** Database failure may affect multiple users and applications.

---

## File System vs Database System

| File System | Database System |
|---|---|
| Stores data in files and folders. | Stores data in an organized database. |
| Data management is mostly handled by applications and the operating system. | Data management is handled through a DBMS. |
| Data redundancy can be high. | Helps reduce data redundancy. |
| Data sharing is more difficult. | Supports easier data sharing. |
| Security and access control are more limited. | Provides centralized security and access control. |
| Data retrieval may require manual processing. | Provides efficient data retrieval using queries. |
| Backup and recovery are often handled separately. | DBMS provides backup and recovery facilities. |

---

## Basic Database Operations (CRUD)

CRUD represents the four basic operations performed on database records.

- **Create:** Adds new data.
- **Read:** Retrieves existing data.
- **Update:** Modifies existing data.
- **Delete:** Removes existing data.

### Example

In a student database:

- Create: Add a new student.
- Read: View student information.
- Update: Change student marks.
- Delete: Remove a student record.

---

## Applications of Databases

- **Education:** Stores student records, results, and attendance.
- **Banking:** Manages customer accounts and transactions.
- **Hospitals:** Stores patient records and medical information.
- **Airlines:** Manages flight schedules and reservations.
- **E-Commerce:** Stores products, customers, and orders.
- **Libraries:** Manages books, members, and issued books.

---

## Conclusion

File Systems and Databases are both used to store and manage data. However, databases provide more advanced features for data management, security, sharing, and retrieval through a Database Management System (DBMS).