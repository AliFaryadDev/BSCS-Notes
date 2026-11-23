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


# Introduction to Databases (Database Systems ka Taaruf)

## 1. Database Kya Hai?
**Database** organized (tarteeb diya hua) data ka aik aisa collection hai jo electronic tor par store kiya jata hai taake usay aasani se **store**, **retrieve (nikalna)**, **update** aur **manage** kiya ja sake.

- **Data:** Raw facts ya figures (jaise kisi student ka naam `"Ali"` ya marks `85`).
- **Information:** Processed aur meaningful data (jaise `"Ali ke 85 marks hain"`).
- **Database:** Wo jagah jahan structured tareeqe se data rakha jata hai taake bar bar kaam aasan ho.

---

## 2. DBMS Kya Hai? (Database Management System)
**DBMS** aik software system hai jo users aur applications ko database ke sath interact karne ki sahulat deta hai (jaise **MySQL**, PostgreSQL, Oracle).

- **Aasan lafzon mein:** File system mein aap khud file ka layout aur code sambhalte thay; DBMS mein ye kaam engine khud manage karta hai.
- **Query Language (jaise SQL):** Aap simple commands likh kar data nikal ya badal sakte hain—har choti baat ke liye naya C/C++ program likhne ki zaroorat nahi rehti.

---

## 3. File System vs. Database (Key Differences)

| Feature | Traditional File System | Database System (DBMS) |
| :--- | :--- | :--- |
| **Data & Program Coupling** | Data structure aksar code ke sath tightly bound hota hai | Data aur application code alag-alag rehte hain (Data Independence) |
| **Redundancy (Duplicate Data)** | Alag files mein wohi data repeat ho sakta hai | Controlled aur minimize hoti hai |
| **Data Integrity & Consistency** | Ghalat data ya corruption ka risk zyada hota hai | Rules/constraints se data accurate rehta hai |
| **Querying / Searching** | Custom code ya loop likhna parta hai | Structured queries (e.g., `SELECT`) se fast access milta hai |
| **Multi-User Access** | Concurrent access aur locking khud handle karni parti hai | Built-in concurrency control aur transactions hotay hain |

---

## 4. Core Concepts Jo Aap Aage Parhenge
- **Schema:** Database ka blueprint ya structure (tables, columns, aur unki data types).
- **Tables / Relations:** Rows (records) aur columns (fields/attributes) ki form mein data.
- **Keys (Primary Key, Foreign Key):** Har record ko uniquely pehchanne aur tables ko aapas mein jorne ke liye.
- **Normalization:** Data ko aise organize karna ke redundancy kam ho aur anomalies (insert/update/delete problems) na aayen.

---

## 5. Chhoti Si SQL Misaal (MySQL Style)
File layout ko byte-by-byte code mein fix karne ke bajaye, aap table define aur query karte hain:

```sql
CREATE TABLE students (
    student_id INT PRIMARY KEY,
    full_name VARCHAR(100),
    email VARCHAR(100)
);

-- Baad mein naya column add karna aasan hai:
ALTER TABLE students ADD COLUMN middle_name VARCHAR(50);

-- Data dekhna:
SELECT student_id, full_name, middle_name FROM students;

