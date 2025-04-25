
# Introduction to Databases

Databases are organized systems for storing, managing, and retrieving data. They are essential in virtually all areas of IT, from websites and mobile apps to large enterprise systems and cybersecurity operations.

---

## 1. Relational Databases (RDBMS)

A **relational database** stores information in tables made up of rows and columns, similar to a spreadsheet. It uses **SQL** to organise, search, and manage data, especially good for relating data across different tables.
### Basic Properties:

- Store data in **tables** (rows and columns).
- Use **Structured Query Language (SQL)**.
- Emphasise **data consistency** and **relationships** (via primary/foreign keys).
- Require a **predefined schema**.

A **predefined schema** in relational databases is a formal structure that defines how data is organised before any data is stored. It specifies:

- The tables that will exist in the database
- The columns each table will contain
- The data type for each column (integer, text, date, etc.)
- Constraints like **primary keys**, **foreign keys**, and not-null requirements

This schema must be established before data can be inserted, and any changes to the structure require the schema to be updated. This provides strong data consistency but less flexibility compared to schema-less database models.

#### SQL Keys: The Foundation of Relational Databases

Keys establish relationships between tables and ensure data integrity in relational databases:

- **Primary Key**: A column (or combination of columns) that uniquely identifies each row in a table; each table has exactly one primary key designation, though it may contain many unique values
- **Composite Primary Key**: A primary key consisting of multiple columns whose combined values uniquely identify each row
- **Foreign Key**: A column that references a primary key in another table, creating relationships between tables and enforcing referential integrity
- **Relationship Example**: When `customer_id` appears in the Customers table, it's a primary key; when the same ID appears in the Orders table, it's a foreign key connecting orders to their customers


### Data Consistency in Relational Databases

In any relational database it is important to ensure that all data follows defined rules and constraints, maintaining accuracy and reliability across transactions. This is crucial for applications where incorrect or contradictory information could lead to serious business, financial, or legal consequences.

#### ACID Compliance 

**ACID** compliance is a framework for ensuring data consistency. It is a set of properties that ensure reliable processing of database transactions. **ACID** stands for:

#### A — Atomicity
Each transaction is **all or nothing**. If any part fails, the whole transaction is rolled back. No partial updates.

#### C — Consistency
A transaction brings the database from one **valid state** to another **valid state**. It maintains database rules, like constraints and relationships.

#### I — Isolation
Transactions are **executed independently**, even if they run at the same time. This prevents interference and ensures consistent results.

#### D — Durability
Once a transaction is committed, its **changes are permanent** — even in case of a crash or power failure.

Without **ACID**, a database can become **unreliable, inconsistent, or even lose data**, especially during errors or power failures.

### Common Use Cases

- Social media platforms managing **massive unstructured** content and **rapid scaling**.
- IoT companies collecting **high-volume**, **real time** sensor data.
- Gaming companies requiring **low-latency data access** from **many clients** all over the world.
- Media delivery networks handling distributed caching and flexible content types
#### Common Relational Databases:
- **SQL Server** (Microsoft): Microsoft's enterprise solution widely used in corporate environments with strong integration across Microsoft's ecosystem.
- **Oracle Database** (Oracle): Robust and scalable system favoured by large enterprises, financial institutions, and mission-critical applications.
- **MySQL** (Open Source): Popular open-source option for web applications and content management systems like WordPress.
- **PostgreSQL** (Open Source): More Advanced open-source system known for reliability, complex query handling, and strong standards compliance.

#### Primary Keys in SQL:

- Unique identifier for each row in a table
- Cannot contain NULL values
- Only one primary key table
- Example: `customer_id` in a Customers table uniquely identifies each customer

##### Foreign Keys in SQL:

- Column(s) that reference a primary key in another table
- Creates relationships between tables
- Enforces referential integrity (prevents orphaned records)
- Example: `customer_id` in an Orders table references the Customers table, connecting each order to its customer

---
## 2. NoSQL Databases

A **NoSQL database** stores data in flexible formats like documents, key-value pairs, graphs, or wide columns, making it easier to handle large volumes of unstructured or rapidly changing data. Unlike relational databases, NoSQL systems are designed to scale out across many servers and prioritise performance, availability, and flexibility over strict structure.

### Basic Properties:

- Non-relational - no fixed schema required.
- Handle **unstructured or semi-structured** data.
- Optimised for **scalability** and **flexibility**.
- Use diverse data models: **document**, **key-value**, **graph**, **wide-column**.

### Types and Examples of NoSQL Databases:

| Type        | Description                        | Examples               |
| ----------- | ---------------------------------- | ---------------------- |
| Document    | Stores data in JSON-like documents | MongoDB                |
| Key-Value   | Simple key and value storage       | Redis, Amazon DynamoDB |
| Graph       | Nodes and edges to represent data  | Neo4j, Amazon Neptune  |
| Wide-Column | Tables with dynamic columns        | Apache Cassandra       |

---

## Data Format Examples

### SQL (Structured Query Language)

Query language used to interact with relational databases.

```sql
SELECT name, email FROM users WHERE active = 1;
```

### JSON (JavaScript Object Notation)

Lightweight, human-readable. Used in many NoSQL systems.

```json
{
  "name": "Maiks Zusevics",
  "email": "maiks@example.com",
  "roles": ["admin", "editor"]
}
```

### XML (eXtensible Markup Language)

Structured, verbose markup language used in legacy and enterprise systems.

```xml
<user>
  <name></name>
  <email>maiks@example.com</email>
</user>
```

---

## Overview of Key Database Systems

### SQL Server (Microsoft)
- Enterprise-grade **RDBMS**
- Uses T-SQL (Transact-SQL)
- Tight integration with Windows systems

### Oracle Database
- High-performance **RDBMS**
- Uses PL/SQL
- Widely used in finance, telecom, and government

### MongoDB
- Document-based NoSQL, uses **JSON-like BSON documents**
- Great for rapidly changing data structures
- Relatively **simple and user friendly**

### Redis
- Keeps **data in memory** for fast access
- Powers features like shopping carts, user sessions, and real-time dashboards

### Neo4j
- Specialised database that focuses on **relationships between data points**
- Excellent for recommendation engines, fraud detection

### Apache Cassandra
- Wide-column NoSQL database designed for **scalability**
- Handles massive amounts of data for applications that need **high availability** 

---

## Security & Maintenance

- **Authentication & Roles**: Restrict who can access or modify data.
- **Backups**: Regular backups to prevent data loss.
- **Indexing**: Improves performance of queries.
- **Monitoring & Logging**: Track usage, performance, and errors.

---
## Summary

- **Relational databases** are used when data integrity, complex queries, and transactional support are priorities.

- **NoSQL databases** are used when working with large volumes of unstructured data, requiring scalability or low-latency responses.

---

## Resources

- [MongoDB Documentation](https://www.mongodb.com/docs/)
- [SQL Server Docs](https://learn.microsoft.com/en-us/sql/sql-server/)
- [Oracle Database Docs](https://docs.oracle.com/en/database/)
- [Redis Docs](https://redis.io/docs/)
- [Neo4j Docs](https://neo4j.com/docs/)
- [Cassandra Docs](https://cassandra.apache.org/doc/latest/)
