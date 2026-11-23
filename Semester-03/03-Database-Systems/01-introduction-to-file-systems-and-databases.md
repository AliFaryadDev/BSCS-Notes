# Introduction to File Systems and Databases

## Key Topics
* [1. Core Definitions](#1-core-definitions)
* [2. Key Differences for Exam Recall](#2-key-differences-for-exam-recall)
* [3. Core Operations](#3-core-operations)

---

## 1. Core Definitions

* **File System:** An OS component that manages, organizes, and stores data in unstructured files and folders.
* **Database:** A structured system that organizes data into tables to facilitate efficient querying and management.

### Manages
- **Meaning:** Data ko control karna.
- **Example:** Create, delete, rename files.

### Organizes
- **Meaning:** Data ko proper order mein arrange karna.
- **Example:** Creating folders and subfolders.


## 2. Key Differences for Exam Recall

* **Structure:** File systems lack a unified schema; databases enforce strict structural rules.
* **Data Redundancy:** File systems allow duplicate data across files; databases minimize redundancy.
* **Data Integrity (data ki durustagi):** Databases use constraints to prevent invalid data entry, unlike file systems.
* **Concurrency:** Databases safely manage simultaneous access by multiple users.

## 3. Core Operations

* **Querying:** Searching and retrieving specific data efficiently.
* **Management:** Performing CRUD operations (Create, Retrieve, Update, Delete) while maintaining data consistency.







# Database vs DBMS vs Database System

## 1. File System vs DBMS
* **File System:** Sirf files, folders, aur permissions ko dekhta hai; data ke andar ke integrity rules ya relationships ko enforce nahi karta. Plain files ya Notepad mein galat/duplicate data aane se **data integrity** kharab hoti hai aur **storage** ka ziyaa ho sakta hai.
* **DBMS:** Data ke structure, constraints (`PRIMARY KEY`, `FOREIGN KEY`, `NOT NULL`, `CHECK`), aur queries ko sambhalta hai.
* **Core Principle:** Baad mein safai karne ke bajaye **data aate waqt hi check karna** (*prevent at entry*) zyada mehfooz aur saaf tareeqa hai. Rules table banate waqt (`CREATE TABLE`) ya baad mein (`ALTER TABLE`) set kiye ja sakte hain, aur DBMS unhein har entry/update par check karta hai.

## 2. Database vs. DBMS vs. Database System
* **Database:** Organized data aur uska structure/schema (jahan data store hota hai).
* **DBMS:** Woh software engine (jaise MySQL) jo data ko store, manage, query, aur secure karta hai.
* **Database System:** Mukammal real-world nizam (aam guftagu mein aksar DBMS ke tor par bhi aata hai, lekin broader/exam context mein poora setup hota hai).

## 3. Database System Equation
**Database System = Hardware + DBMS (Software) + Database + Users + Rules of Organization**

* **Hardware:** Servers, storage disks, RAM, aur network.
* **DBMS (Software):** Data management aur rule enforcement engine.
* **Database:** Stored structured data aur schema.
* **Users:** Admins, end-users, aur applications.
* **Rules of Organization:** Idare ke operational procedures, policies, aur workflows (jaise backup schedules, recovery SOPs, aur access approvals), jabke technical data rules DBMS ke andar hote hain.
