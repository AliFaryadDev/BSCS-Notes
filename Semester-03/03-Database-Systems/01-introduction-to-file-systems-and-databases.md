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
