# 04 — Database Approach vs. File-Based System

## Important Points

- [Introduction](#introduction)
- [File-Based System](#file-based-system)
- [Database Approach](#database-approach)
- [Major Differences](#major-differences)
- [Advantages of Database Approach](#advantages-of-database-approach)
- [Conclusion](#conclusion)

---

## Introduction

A File-Based System and a Database Approach are two different methods of storing and managing data.

A File-Based System stores data in separate files, while the Database Approach uses a DBMS to manage data in an organized way.

---

## File-Based System

### Definition

A File-Based System is a traditional method of storing and managing data in separate files using individual application programs.

### Characteristics

- Data is stored in separate files.
- Each application manages its own data.
- Data redundancy may occur.
- Data sharing is difficult.
- Security and backup are managed separately.

### Example

A college maintains separate files for student records, fee records, and examination results.

---

## Database Approach

### Definition

The Database Approach is a method of storing and managing related data through a Database Management System (DBMS).

### Characteristics

- Data is stored in a centralized or organized database.
- A DBMS manages the data.
- Reduces unnecessary data duplication.
- Supports data sharing.
- Provides security and access control.
- Supports backup and recovery.

### Example

A college uses one database to manage student information, fees, attendance, and examination results.

---

## Major Differences

| File-Based System | Database Approach |
|---|---|
| Data is stored in separate files. | Data is managed through a database. |
| Uses individual application programs. | Uses a DBMS. |
| High data redundancy may occur. | Reduces unnecessary data redundancy. |
| Data inconsistency is more likely. | Helps maintain data consistency. |
| Data sharing is difficult. | Supports data sharing. |
| Program-data dependence exists. | Provides data independence. |
| Security controls are limited. | Provides better security controls. |
| Backup and recovery are handled separately. | DBMS provides backup and recovery facilities. |
| Data retrieval may be difficult. | Data retrieval is easier through queries. |

---

## Advantages of Database Approach

- Reduces data redundancy.
- Improves data consistency.
- Provides better data security.
- Supports multiple users.
- Provides data independence.
- Makes data retrieval easier.
- Supports backup and recovery.

---

## Conclusion

The Database Approach is generally more suitable for managing large and complex amounts of data because it provides better security, data sharing, consistency, and data independence than traditional File-Based Systems.