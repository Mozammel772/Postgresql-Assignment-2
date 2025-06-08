# PostgreSQL Basics

## 01. What is PostgreSQL?

**PostgreSQL** is an open-source relational database management system (RDBMS) that supports both SQL (relational) and JSON (non-relational) querying. It offers powerful features like scalability, support for custom data types, extensibility, and strong security measures.

---

## 02. What is the purpose of a database schema in PostgreSQL?

A **schema** in PostgreSQL is a logical structure that organizes database objects such as tables, views, and functions. It helps separate data and functionality for different users or applications, allowing for better organization and avoiding naming conflicts in a shared environment.

---

## 03. Explain the Primary Key and Foreign Key concepts in PostgreSQL.

- **Primary Key**: A primary key uniquely identifies each record in a table. It must be both `UNIQUE` and `NOT NULL`, ensuring that no duplicate or null values exist in the key column(s).

- **Foreign Key**: A foreign key is a column or group of columns in one table that references the primary key in another table. It establishes a relationship between the two tables and helps maintain referential integrity.

---

## 04. What is the difference between the `VARCHAR` and `CHAR` data types?

- `VARCHAR(n)` is a variable-length string with a maximum length of **n**. It only uses as much space as the actual string content.

- `CHAR(n)` is a fixed-length string that always stores exactly **n** characters. If the input is shorter, it pads the remaining space with blanks.

**Example**:  
- `'Cat'` stored as `CHAR(5)` → `'Cat  '`  
- `'Cat'` stored as `VARCHAR(5)` → `'Cat'`

---

## 05. Explain the purpose of the WHERE clause in a SELECT statement.

The `WHERE` clause is used to filter rows in a `SELECT` query based on specified conditions. It allows you to retrieve only the records that meet certain criteria.

```sql
SELECT * FROM users WHERE user_id = 2;
