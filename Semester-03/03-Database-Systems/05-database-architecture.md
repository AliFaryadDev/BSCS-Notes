# 05 — Database Architecture

## Important Points

- [Introduction](#introduction)
- [Definition](#definition)
- [Types of Database Architecture](#types-of-database-architecture)
- [One-Tier Architecture](#one-tier-architecture)
- [Two-Tier Architecture](#two-tier-architecture)
- [Three-Tier Architecture](#three-tier-architecture)
- [Advantages](#advantages-of-database-architecture)
- [Conclusion](#conclusion)

---

## Introduction

Database Architecture describes the structure and design of a database system. It explains how users, applications, and databases interact with each other.

## Definition

Database Architecture is the overall design and structure of a database system that defines how data is stored, accessed, and managed.

---

## Types of Database Architecture

Database Architecture is commonly divided into three types:

### 1. One-Tier Architecture

#### Definition

One-Tier Architecture is a database architecture in which the user, application, and database are located on the same system.

#### Working

- The user directly interacts with the database.
- Application and database operate on the same machine.
- No separate database server is required.

#### Example

A developer working directly with a local SQLite database.

---

### 2. Two-Tier Architecture

#### Definition

Two-Tier Architecture is a database architecture in which the client application communicates directly with the database server.

#### Components

- **Client:** Provides the user interface and sends requests.
- **Database Server:** Stores and manages data.

#### Working

1. The user interacts with the client application.
2. The client sends a request to the database server.
3. The database server processes the request.
4. The result is returned to the client.

#### Example

A desktop application directly connecting to a MySQL database server.

---

### 3. Three-Tier Architecture

#### Definition

Three-Tier Architecture is a database architecture that separates the system into three layers: Presentation Layer, Application Layer, and Database Layer.

#### Components

**1. Presentation Layer**

- Provides the user interface.
- Accepts user input.
- Displays results.

**2. Application Layer**

- Processes user requests.
- Applies business logic.
- Communicates with the database.

**3. Database Layer**

- Stores data.
- Retrieves and updates data.
- Manages database operations.

#### Working

1. The user interacts with the Presentation Layer.
2. The request goes to the Application Layer.
3. The Application Layer communicates with the Database Layer.
4. The database processes the request.
5. The result returns to the user through the Application Layer.

#### Example

An online shopping website:

- Presentation Layer: Website interface.
- Application Layer: Backend server.
- Database Layer: MySQL database.

---

## Advantages of Database Architecture

- Organizes database components.
- Improves system performance.
- Supports security.
- Makes system maintenance easier.
- Separates different responsibilities.
- Supports scalability.

---

## Conclusion

Database Architecture defines how different components of a database system communicate and work together. One-Tier, Two-Tier, and Three-Tier architectures are common architectural approaches.