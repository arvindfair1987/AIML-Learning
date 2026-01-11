# 📘 Introduction to SQL

---

## 1️⃣ Background Recap

So far, you have learned about:

- Features of **Relational Database Management Systems (RDBMS)**
- The **relational model**
- **Entity–Relationship Diagrams (ERDs)**
- **Schemas** (star and snowflake)

With this foundation, you are now ready to **interact with databases directly** using **SQL**.

---

## 2️⃣ What Is SQL?

**SQL** stands for **Structured Query Language**.  
It is a **domain-specific language (DSL)** used to manage and manipulate data stored in an **RDBMS**.

SQL is the standard language used to communicate with relational databases.

---

## 3️⃣ What Can You Do with SQL?

SQL allows you to:

- **Create data** (tables, records)
- **Manipulate data** (insert, update)
- **Delete data**
- **Share and retrieve data** (queries, reports)

In short, SQL gives you **full control over relational data**.

---

## 4️⃣ Why Should You Learn SQL?

### 🔹 Language Agnostic
- SQL syntax is largely the same across databases
- Once learned, it works with **any RDBMS**

### 🔹 Universal Support
- Supported by all modern database systems:
  - Oracle
  - MySQL
  - SQL Server
  - PostgreSQL
  - and many more

### 🔹 Industry Standard
- SQL is the backbone of data-driven applications
- Essential for roles in data engineering, analytics, backend development, and ML

---

## 5️⃣ Popular RDBMS Platforms

Some of the **most widely used RDBMSes** are:

1. Oracle Database  
2. MySQL  
3. Microsoft SQL Server  
4. PostgreSQL  
5. Amazon Aurora  
6. MariaDB  
7. IBM Db2  
8. SAP HANA  
9. Amazon RDS  
10. Google Cloud SQL  

---

## 6️⃣ Why MySQL?

You will be working primarily with **MySQL** because:

- ✅ It is **open-source** (free to use)
- ✅ Supports all standard **RDBMS features**
- ✅ Has a **large community**, documentation, and tutorials
- ✅ Widely used in both industry and learning environments

---

## 7️⃣ Real-World Applications of RDBMS + SQL

### 🏦 Banking Sector
- Managing transactions between accounts
- Ensuring consistency using **ACID properties**
- Handling concurrent users safely

👉 RDBMSes are ideal for **transaction-heavy systems**

---

### 🛒 E-Commerce Websites
Examples: Amazon, Flipkart

- Product categorisation
- Order management
- User–product relationships
- Recommendation systems

👉 Relational databases store and manage **complex relationships** between products, users, and orders

---

### 🌐 Social Networking Sites
Example: Facebook

- User profiles
- Friend relationships
- Mutual friend suggestions

👉 Relationships between entities (users) are efficiently handled using **relational mapping**

---

## 8️⃣ SQL + RDBMS: A Powerful Combination

- **RDBMS** provides structured storage and integrity
- **SQL** provides the language to:
  - Query data
  - Modify data
  - Maintain consistency
  - Enforce constraints

Together, they form the **foundation of modern data systems**.

---

## 9️⃣ What’s Next?

Next, you will:

- Install **MySQL Server**
- Explore **MySQL Workbench**
- Start writing **real SQL queries**
- Perform hands-on data manipulation

---

## ✅ Key Takeaway

> **SQL is the universal language for interacting with relational databases, enabling efficient storage, retrieval, and management of structured data across industries.**

# 📘 Introduction to DDL Commands

---

## 1️⃣ SQL Command Categories

SQL commands are broadly divided into **two main subcategories** based on their purpose:

| Category | Full Form | Purpose |
|--------|-----------|---------|
| **DDL** | Data Definition Language | Defines and modifies the **structure** of the database |
| **DML** | Data Manipulation Language | Manipulates the **data inside** database tables |

---

## 2️⃣ Difference Between DDL and DML

| DDL (Data Definition Language) | DML (Data Manipulation Language) |
|--------------------------------|----------------------------------|
| Defines the **structure** of data | Modifies the **data itself** |
| Creates and alters database objects | Inserts, updates, or deletes records |
| Works on schema-level objects | Works on table-level data |
| Changes are usually **auto-committed** | Changes can be **rolled back** |

---

## 3️⃣ Common DDL Commands

The most commonly used **DDL commands** are:

- **CREATE**
- **ALTER**
- **DROP**

These commands define and control the structure of the database.

---

## 4️⃣ DDL Command Syntax and Usage

### 🔹 CREATE
Used to create:
- Databases
- Tables
- Columns
- Primary keys
- Foreign keys
- Constraints

📌 **Example usage**:
```sql
CREATE DATABASE demonstration;


🔹 ALTER

Used to change the structure of an existing table.

ALTER TABLE table_name ADD column_name datatype;

ALTER TABLE table_name DROP column_name;

ALTER TABLE table_name MODIFY column_name new_datatype;


🔹 DROP

Used to remove:

Tables
Columns
Entire databases

⚠️ Permanent operation – data cannot be recovered.
DROP TABLE table_name;

5️⃣ Defining Tables Using the CREATE Command
🗄️ Database Creation

You created a database named:
CREATE DATABASE demonstration;

📋 Table: customers
Column Name	Data Type	Constraints
ID	INT	NOT NULL
NAME	VARCHAR(32)	NOT NULL
time	TIMESTAMP	DEFAULT CURRENT_TIMESTAMP, NOT NULL
age	INT	—
address	VARCHAR(32)	—
salary	INT	—

INSERT INTO customers VALUES (...);
UPDATE customers SET salary = 50000 WHERE id = 1;
DELETE FROM customers WHERE id = 1;

DDL → CREATE, ALTER, DROP (structure)

DML → INSERT, UPDATE, DELETE (data)

Both are essential for working with SQL databases
```
---

````md
# 📘 SQL `LIKE` & `ESCAPE` — Complete Notes with Examples

---

## 1️⃣ `LIKE` Operator

The `LIKE` operator is used to **match text patterns** in SQL.

### Syntax

```sql
SELECT *
FROM table_name
WHERE column_name LIKE 'pattern';
````

---

## 2️⃣ Wildcards Used in `LIKE`

| Wildcard | Meaning                             |
| -------- | ----------------------------------- |
| `%`      | Matches **zero or more characters** |
| `_`      | Matches **exactly one character**   |

---

## 3️⃣ Basic Examples

### Example table: `suppliers`

| supplier_name |
| ------------- |
| G%Mart        |
| G_Mart        |
| Grocery       |
| Global        |

### Example 1: `%` wildcard

```sql
WHERE supplier_name LIKE 'G%';
```

✅ Matches:

* G%Mart
* G_Mart
* Grocery
* Global

---

### Example 2: `_` wildcard

```sql
WHERE supplier_name LIKE 'G_';
```

✅ Matches:

* GA
* G%
* G_

---

## 4️⃣ Problem with Wildcards

If `%` or `_` exist as **actual characters in the data**, `LIKE` treats them as wildcards, leading to **incorrect matches**.

---

## 5️⃣ `ESCAPE` Clause

The `ESCAPE` clause tells SQL to treat the next character **literally**, not as a wildcard.

### Syntax

```sql
LIKE 'pattern' ESCAPE 'escape_character'
```

* Escape character can be **any single character**
* Common choices: `!`, `#`, `^`

---

## 6️⃣ Using `ESCAPE` with `%`

### ❌ Without ESCAPE

```sql
WHERE supplier_name LIKE 'G%';
```

Matches all values starting with `G`

---

### ✅ With ESCAPE

```sql
WHERE supplier_name LIKE 'G!%' ESCAPE '!';
```

Meaning:

* `!%` → literal `%`

✅ Matches:

* G%Mart

---

## 7️⃣ Using `ESCAPE` with `_`

### ❌ Without ESCAPE

```sql
WHERE supplier_name LIKE 'G_';
```

Matches any single character after `G`

---

### ✅ With ESCAPE

```sql
WHERE supplier_name LIKE 'G!_' ESCAPE '!';
```

Meaning:

* `!_` → literal `_`

✅ Matches:

* G_

---

## 8️⃣ Backslash (`\`) vs `ESCAPE`

### Using backslash

```sql
LIKE 'G\%'
LIKE 'G\_'
```

⚠️ Behavior depends on the database.

| Database   | Result  |
| ---------- | ------- |
| MySQL      | Works   |
| PostgreSQL | Fails   |
| Oracle     | Fails   |
| SQL Server | Depends |

---

### ✅ Standard & Safe Method

```sql
LIKE 'G!%' ESCAPE '!'
LIKE 'G!_' ESCAPE '!'
```

✔ Works in **all SQL databases**

---

## 9️⃣ Comparison Summary

| Query                   | Standard | Portable |
| ----------------------- | -------- | -------- |
| `LIKE 'G\%'`            | ❌        | ❌        |
| `LIKE 'G!%' ESCAPE '!'` | ✅        | ✅        |
| `LIKE 'G\_'`            | ❌        | ❌        |
| `LIKE 'G!_' ESCAPE '!'` | ✅        | ✅        |

---

## 🔟 Complex Pattern Example (IMPORTANT)

### Example table: `logs`

| log_id | log_message            |
| ------ | ---------------------- |
| 1      | START TEST%TEST123 END |
| 2      | TEST%TEST123           |
| 3      | TESTXTEST123           |
| 4      | ABC TEST%TEST123 XYZ   |
| 5      | TESTTEST123            |
| 6      | TEST%TEST124           |

---

### Query

```sql
SELECT *
FROM logs
WHERE log_message LIKE '%TEST!%TEST123%' ESCAPE '!';
```

---

### Pattern Breakdown

```
%TEST!%TEST123%
```

| Part      | Meaning               |
| --------- | --------------------- |
| `%`       | Any characters before |
| `TEST`    | Literal text          |
| `!%`      | Literal `%`           |
| `TEST123` | Literal text          |
| `%`       | Any characters after  |

---

### Rows MATCHED ✅

| log_id | log_message            |
| ------ | ---------------------- |
| 1      | START TEST%TEST123 END |
| 2      | TEST%TEST123           |
| 4      | ABC TEST%TEST123 XYZ   |

---

### Rows NOT MATCHED ❌

| log_message  | Reason        |
| ------------ | ------------- |
| TESTXTEST123 | Missing `%`   |
| TESTTEST123  | No `%`        |
| TEST%TEST124 | Text mismatch |

---

## 1️⃣1️⃣ When to Use `ESCAPE`

| Situation               | Use ESCAPE |
| ----------------------- | ---------- |
| Searching literal `%`   | ✅ Yes      |
| Searching literal `_`   | ✅ Yes      |
| Normal pattern matching | ❌ No       |
| Writing portable SQL    | ✅ Yes      |

---

## 🔑 Key Points (Exam Gold)

* `%` and `_` are **wildcards**
* `ESCAPE` converts them into **literal characters**
* Backslash escaping is **not standard**
* `ESCAPE` is **ANSI SQL compliant**
* Complex patterns can combine **wildcards + escaped literals**

---

## 📝 One-Line Exam Answer

> **The `ESCAPE` clause in SQL is used with the `LIKE` operator to treat wildcard characters (`%`, `_`) as literal characters during pattern matching.**

```

Perfect 👍
Below is **everything merged into ONE single, clean, exam-ready `.md` file**.
You can **copy–paste directly** into a file like `SQL_LIKE_ESCAPE_Complete.md`.

---

````md
# 📘 SQL `LIKE` & `ESCAPE` — Complete Notes with Examples

---

## 1️⃣ `LIKE` Operator

The `LIKE` operator is used to **match text patterns** in SQL.

### Syntax

```sql
SELECT *
FROM table_name
WHERE column_name LIKE 'pattern';
````

---

## 2️⃣ Wildcards Used in `LIKE`

| Wildcard | Meaning                             |
| -------- | ----------------------------------- |
| `%`      | Matches **zero or more characters** |
| `_`      | Matches **exactly one character**   |

---

## 3️⃣ Basic Examples

### Example table: `suppliers`

| supplier_name |
| ------------- |
| G%Mart        |
| G_Mart        |
| Grocery       |
| Global        |

### Example 1: `%` wildcard

```sql
WHERE supplier_name LIKE 'G%';
```

✅ Matches:

* G%Mart
* G_Mart
* Grocery
* Global

---

### Example 2: `_` wildcard

```sql
WHERE supplier_name LIKE 'G_';
```

✅ Matches:

* GA
* G%
* G_

---

## 4️⃣ Problem with Wildcards

If `%` or `_` exist as **actual characters in data**, `LIKE` treats them as wildcards, leading to **incorrect matches**.

---

## 5️⃣ `ESCAPE` Clause

The `ESCAPE` clause tells SQL to treat the next character **literally**, not as a wildcard.

### Syntax

```sql
LIKE 'pattern' ESCAPE 'escape_character'
```

* Escape character must be **one single character**
* Common choices: `!`, `#`, `^`

---

## 6️⃣ Using `ESCAPE` with `%`

### ❌ Without ESCAPE

```sql
WHERE supplier_name LIKE 'G%';
```

Matches all values starting with `G`

---

### ✅ With ESCAPE

```sql
WHERE supplier_name LIKE 'G!%' ESCAPE '!';
```

Meaning:

* `!%` → literal `%`

✅ Matches:

* G%Mart

---

## 7️⃣ Using `ESCAPE` with `_`

### ❌ Without ESCAPE

```sql
WHERE supplier_name LIKE 'G_';
```

Matches any single character after `G`

---

### ✅ With ESCAPE

```sql
WHERE supplier_name LIKE 'G!_' ESCAPE '!';
```

Meaning:

* `!_` → literal `_`

✅ Matches:

* G_

---

## 8️⃣ Backslash (`\`) vs `ESCAPE`

### Using backslash

```sql
LIKE 'G\%'
LIKE 'G\_'
```

⚠️ Behavior depends on database.

| Database   | Result  |
| ---------- | ------- |
| MySQL      | Works   |
| PostgreSQL | Fails   |
| Oracle     | Fails   |
| SQL Server | Depends |

---

### ✅ Standard & Portable Method

```sql
LIKE 'G!%' ESCAPE '!'
LIKE 'G!_' ESCAPE '!'
```

✔ Works in **all SQL databases**

---

## 9️⃣ Comparison Summary

| Query                   | Standard | Portable |
| ----------------------- | -------- | -------- |
| `LIKE 'G\%'`            | ❌        | ❌        |
| `LIKE 'G!%' ESCAPE '!'` | ✅        | ✅        |
| `LIKE 'G\_'`            | ❌        | ❌        |
| `LIKE 'G!_' ESCAPE '!'` | ✅        | ✅        |

---

## 🔟 Complex Pattern Example (IMPORTANT)

### Example table: `logs`

| log_id | log_message            |
| ------ | ---------------------- |
| 1      | START TEST%TEST123 END |
| 2      | TEST%TEST123           |
| 3      | TESTXTEST123           |
| 4      | ABC TEST%TEST123 XYZ   |
| 5      | TESTTEST123            |
| 6      | TEST%TEST124           |

---

### Query

```sql
SELECT *
FROM logs
WHERE log_message LIKE '%TEST!%TEST123%' ESCAPE '!';
```

---

### Pattern Breakdown

```
%TEST!%TEST123%
```

| Part      | Meaning               |
| --------- | --------------------- |
| `%`       | Any characters before |
| `TEST`    | Literal text          |
| `!%`      | Literal `%`           |
| `TEST123` | Literal text          |
| `%`       | Any characters after  |

---

### Rows MATCHED ✅

| log_id | log_message            |
| ------ | ---------------------- |
| 1      | START TEST%TEST123 END |
| 2      | TEST%TEST123           |
| 4      | ABC TEST%TEST123 XYZ   |

---

### Rows NOT MATCHED ❌

| log_message  | Reason        |
| ------------ | ------------- |
| TESTXTEST123 | Missing `%`   |
| TESTTEST123  | No `%`        |
| TEST%TEST124 | Text mismatch |

---

## 1️⃣1️⃣ When to Use `ESCAPE`

| Situation               | Use ESCAPE |
| ----------------------- | ---------- |
| Searching literal `%`   | ✅ Yes      |
| Searching literal `_`   | ✅ Yes      |
| Normal pattern matching | ❌ No       |
| Writing portable SQL    | ✅ Yes      |

---

## 1️⃣2️⃣ What if `ESCAPE` is given a character that is NOT `%` or `_`?

### Short Answer

👉 **Nothing special happens unless that escape character is actually used.**

`ESCAPE` only defines **which character may escape `%` or `_`**.
If it is **not used**, it has **no effect**.

---

## 1️⃣3️⃣ Key Rule

* `%` and `_` are the **only wildcards**
* `ESCAPE` applies **only to these two**
* Escape character used elsewhere → **ignored**

---

## 1️⃣4️⃣ Escape Character Not Used

```sql
SELECT *
FROM suppliers
WHERE supplier_name LIKE 'G%' ESCAPE '#';
```

✔ Same result as:

```sql
LIKE 'G%'
```

📌 Because `#` is **never used**

---

## 1️⃣5️⃣ ESCAPE Before Normal Character

```sql
LIKE 'G#A' ESCAPE '#';
```

* `A` is not a wildcard
* `#A` has no meaning

✔ Matches only literal `G#A`

---

## 1️⃣6️⃣ ESCAPE Before Non-Wildcard

```sql
LIKE 'G!X' ESCAPE '!'
```

📌 `!X` is treated as **literal text**

ESCAPE has **no effect**

---

## 1️⃣7️⃣ Correct Usage (Only Time ESCAPE Matters)

### Escaping `%`

```sql
LIKE 'G!%' ESCAPE '!'
```

### Escaping `_`

```sql
LIKE 'G!_' ESCAPE '!'
```

---

## 1️⃣8️⃣ Invalid or Pointless Usage

### ❌ Pointless but valid

```sql
LIKE 'ABC' ESCAPE '!';
```

ESCAPE does nothing

---

### ❌ Invalid

```sql
ESCAPE '!!'
```

❌ Error — escape must be **exactly one character**

---

## 1️⃣9️⃣ Summary Table

| Situation                 | Result        |
| ------------------------- | ------------- |
| ESCAPE char not used      | No effect     |
| ESCAPE before normal char | No effect     |
| ESCAPE before `%` or `_`  | Makes literal |
| ESCAPE char = `%` or `_`  | ❌ Invalid     |
| ESCAPE length > 1         | ❌ Invalid     |

---

## 📝 One-Line Exam Answer

> **The `ESCAPE` clause in SQL affects only `%` and `_`; if the escape character is unused or precedes a non-wildcard character, it has no effect.**

```

---

Below are **clear examples with sample data, queries, and results** for **each situation** you listed.
(All examples use simple tables so the behavior is easy to see.)

---

# ✅ Table used in examples

```sql
CREATE TABLE suppliers (
    supplier_name VARCHAR(50)
);
```

### Sample data

| supplier_name |
| ------------- |
| Global        |
| Grocery       |
| G%Mart        |
| G_Mart        |
| G#A           |
| G!%           |
| G!X           |

---

## 1️⃣ ESCAPE character **not used** → **No effect**

### Query

```sql
SELECT *
FROM suppliers
WHERE supplier_name LIKE 'G%' ESCAPE '#';
```

### Explanation

* `%` is still a wildcard
* `#` is defined as escape but **never used**

### Result

| supplier_name |
| ------------- |
| Global        |
| Grocery       |
| G%Mart        |
| G_Mart        |
| G#A           |
| G!%           |
| G!X           |

📌 Same result as:

```sql
WHERE supplier_name LIKE 'G%';
```

---

## 2️⃣ ESCAPE before a **normal character** → **No effect**

### Query

```sql
SELECT *
FROM suppliers
WHERE supplier_name LIKE 'G#A' ESCAPE '#';
```

### Explanation

* `A` is **not** a wildcard
* `#A` is treated as literal `#A`
* ESCAPE does nothing special here

### Result

| supplier_name |
| ------------- |
| G#A           |

---

## 3️⃣ ESCAPE before `%` or `_` → **Makes them literal**

### a) Escaping `%`

```sql
SELECT *
FROM suppliers
WHERE supplier_name LIKE 'G!%' ESCAPE '!';
```

### Explanation

* `!%` → literal `%`

### Result

| supplier_name |                                                             |
| ------------- | ----------------------------------------------------------- |
| G%Mart        |                                                             |
| G!%           | ❌ (does NOT match, because name starts with `G!`, not `G%`) |

✔ Correct match:

| supplier_name |
| ------------- |
| G%Mart        |

---

### b) Escaping `_`

```sql
SELECT *
FROM suppliers
WHERE supplier_name LIKE 'G!_' ESCAPE '!';
```

### Explanation

* `!_` → literal `_`

### Result

| supplier_name |
| ------------- |
| G_Mart        |

---

## 4️⃣ ESCAPE character = `%` or `_` → ❌ **Invalid**

### Query

```sql
SELECT *
FROM suppliers
WHERE supplier_name LIKE 'G%%' ESCAPE '%';
```

### Result

❌ **ERROR**

Typical database error:

```
Invalid escape character
```

📌 Reason:

* Escape character **cannot be `%` or `_`**
* They are already wildcards

---

## 5️⃣ ESCAPE character length > 1 → ❌ **Invalid**

### Query

```sql
SELECT *
FROM suppliers
WHERE supplier_name LIKE 'G!%' ESCAPE '!!';
```

### Result

❌ **ERROR**

Typical database error:

```
ESCAPE must be a single character
```

📌 Reason:

* SQL allows **only one character** as ESCAPE

---

# 📌 Final Summary Table (with outcomes)

| Situation                 | Example                 | Result                |
| ------------------------- | ----------------------- | --------------------- |
| ESCAPE char not used      | `LIKE 'G%' ESCAPE '#'`  | Works, no effect      |
| ESCAPE before normal char | `LIKE 'G#A' ESCAPE '#'` | Works, no effect      |
| ESCAPE before `%`         | `LIKE 'G!%' ESCAPE '!'` | `%` treated literally |
| ESCAPE before `_`         | `LIKE 'G!_' ESCAPE '!'` | `_` treated literally |
| ESCAPE char = `%` or `_`  | `ESCAPE '%'`            | ❌ Error               |
| ESCAPE length > 1         | `ESCAPE '!!'`           | ❌ Error               |

---

## 📝 One-line exam answer

> **The `ESCAPE` clause only affects `%` and `_`; if unused or applied to non-wildcards it has no effect, and it must be a single character other than `%` or `_`.**


---