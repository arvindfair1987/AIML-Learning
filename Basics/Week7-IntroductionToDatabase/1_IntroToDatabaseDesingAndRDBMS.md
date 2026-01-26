# 📘 Introduction to Business Data Usage and Decision-Making

Modern businesses rely heavily on **data-driven decision-making**.  
Data helps organisations understand customer behaviour, optimise operations, predict future trends, and make informed strategic decisions.

---

## 1️⃣ End-to-End Data-to-Decision Process

The overall process of extracting insights from data can be summarised in the following stages:

---

### 🔹 1. Data Source
Data is collected from multiple sources such as:
- Mobile applications
- Web applications
- Transactional systems
- IoT devices
- Sensors and logs

📌 **Example:**  
User clicks on an e-commerce website, app usage logs, purchase history.

---

### 🔹 2. Data Warehouse (Data Storage)
- Data from different sources is stored in a **centralised location**
- This location is commonly a **database** or **data warehouse**
- Data is stored **historically**, enabling long-term analysis

📌 **Purpose:**  
To store large volumes of data reliably for querying and analysis.

---

### 🔹 3. Data Mining / Data Analysis
- Data scientists and analysts explore the stored data
- Identify:
  - Patterns
  - Trends
  - Relationships
  - Anomalies

📌 **Techniques Used:**  
Statistics, SQL queries, machine learning, aggregations.

---

### 🔹 4. Reporting and Visualisation
- Insights are presented using:
  - Dashboards
  - Reports
  - Charts and graphs
- Tools such as **Tableau, Power BI**, etc., are used
- These tools are often directly connected to databases

📌 **Goal:**  
Make insights easy to understand for business stakeholders.

---

### 🔹 5. Decision-Making
- Business leaders use insights to:
  - Plan strategies
  - Improve processes
  - Allocate resources
  - Take corrective actions

📌 **Outcome:**  
Data-driven action plans.

---

## 2️⃣ Role of a Data Professional – Practical Example

### 🧠 Scenario: Data Scientist at Amazon

You are a data scientist at **Amazon**, tasked with predicting **next month’s sales** for electronic products.

---

### 🔍 Key Questions to Answer
- How much inventory should be stocked?
- Which products will sell more?
- How demand changes with seasonality?

---

### 📊 Data Required
To make accurate predictions, you would need:
- Historical sales data (last 5 years)
- Month-over-month and year-over-year trends
- Seasonal patterns (festive sales, discounts)
- Recent sales behaviour
- Regional and local demand patterns

---

### 📌 Importance of Patterns
Sales prediction is **multi-dimensional**, but one key factor is:
> **Understanding historical patterns**

Patterns reveal:
- Growth trends
- Seasonal spikes
- Declines in demand

---

### 🗄️ Role of Data Storage Layer
All the above insights are possible only when:
- Data is stored **historically**
- Data can be queried and aggregated
- A reliable **database or data warehouse** exists

➡ **Conclusion:**  
A data storage layer is fundamental for any prediction or analytics task.

---

## 3️⃣ Why Databases Are Essential for Data Science

As a data professional:
- You are expected to **extract insights from data**
- Companies store data centrally in **databases**
- Databases act as a **single source of truth**

📌 This allows:
- Easy data exploration
- Consistent reporting
- Reliable analytics

---

## 4️⃣ Roles of Databases in Businesses

Databases play three major roles:

---

### 🔹 1. Power Live Applications
- Used by applications like:
  - Instagram
  - Facebook
  - LinkedIn
- Handle real-time user traffic
- Store live operational data

---

### 🔹 2. Support Analytics and Reporting
- Business reports are generated directly from databases
- Dashboards are connected to databases
- Enables real-time and historical analysis

---

### 🔹 3. Maintain Data Relationships
- Databases maintain relationships between tables
- Ensures data consistency and integrity
- These are known as **relational databases**

---

## 5️⃣ Types of Databases

Databases can be broadly classified into two types:

---

### 🔹 SQL (Relational) Databases
- Store data in **rows and columns**
- Organised as **tables**
- Tables are connected using relationships
- Store **structured data**

📌 Examples of data:
- Names
- Addresses
- Credit card numbers
- Geolocation
- Transaction records

---

### 🔹 NoSQL (Non-Relational) Databases
- Store data in various formats:
  - Documents
  - Key-value pairs
  - Graphs
- Can store **unstructured and semi-structured data**

📌 Examples:
- Text
- Social media comments
- Images
- Logs

📌 Developed to handle:
- Large-scale data
- Diverse data formats
- High-speed applications

---

## 6️⃣ Importance of SQL Databases in Real-World Scenarios

SQL databases are widely used because:

- They handle **structured (tabular) data**
- Supported by big data tools like:
  - Spark
  - Hive
- Enable analytical reporting
- Ideal for **initial data exploration**
- Industry-standard for business analytics

---

## 7️⃣ Recall Quiz Insight

### 🧠 Question:
A pizza chain plans to open new outlets.  
Which attribute will **NOT** affect location choice?

✅ **Shape of outlet**

📌 Reason:  
Location decisions depend on demand, footfall, accessibility, and demographics—not physical shape.

---

## 8️⃣ Key Takeaways

- Data-driven decision-making follows a structured pipeline
- Databases are the backbone of analytics
- Historical data enables pattern discovery and prediction
- SQL databases are foundational for business intelligence
- Data professionals rely on databases to extract meaningful insights

---

## 📝 Exam-Friendly Summary

> Business decisions are driven by data collected from multiple sources, stored in databases, analysed for patterns, visualised through reports, and finally used to make informed decisions.

---

# 📘 Challenges of Traditional Data Storage Systems & Introduction to DBMS

---

## 1️⃣ Challenges of Traditional (File-Based) Data Storage Systems

Think about how data is commonly stored on a personal computer:
- Separate folders for PDFs, images, documents, etc.
- The same file may exist in **multiple locations**

If you modify a file in one location and forget to update the other copy, **inconsistency arises**.

Because of such issues, traditional file-based systems are **not reliable for structured data management**.

---

### ❌ Key Disadvantages of File-Based Storage Systems

#### 1. Data Redundancy (Duplicate Data)
- Same data stored in multiple files or folders
- Leads to unnecessary duplication
- Makes updates and deletions difficult

---

#### 2. Data Inconsistency
- Multiple copies of the same data may not be updated together
- Results in conflicting or outdated information

---

#### 3. Scattered Data
- Data spread across many files
- Different formats (text files, CSVs, spreadsheets, etc.)
- Makes data retrieval and application development difficult

---

#### 4. Poor Data Security
- Difficult to enforce strong access control
- No centralized security policies
- Higher risk of unauthorized access

---

#### 5. Data Integrity Issues
- No built-in support for constraints (e.g., valid values, uniqueness)
- Hard to ensure correctness and quality of data

---

### ❗ Conclusion
> Traditional file-based systems are **not suitable** for managing large, structured, and shared data.

---

## 2️⃣ Why Do We Need Databases?

In almost **every industry**, data storage is essential:

- **Banking**: Customer accounts, balances, transactions
- **E-commerce**: Product catalogs, orders, user behavior
- **Social Media**: User profiles, interactions, preferences
- **Healthcare**: Patient records, reports
- **Education**: Student records, grades

➡ **No modern application can survive without a database**

---

## 3️⃣ Common Misconception: Are MySQL and Oracle Databases?

Many people believe:
> MySQL and Oracle are databases ❌

### ✅ Correct Understanding
- **Database**: The actual place where data is stored
- **DBMS (Database Management System)**: Software used to manage and interact with the database

➡ MySQL, Oracle, PostgreSQL, SQL Server, MongoDB are **DBMSs**, not databases themselves.

---

## 4️⃣ Database vs Database Management System (DBMS)

### 🔹 What Is a Database?
- The **physical storage layer**
- Stores data on disk
- Concerned only with **data storage**

---

### 🔹 What Is a DBMS?
A **DBMS** is a collection of programs or software that:
- Sits on top of the database
- Allows users and applications to:
  - Store data
  - Retrieve data
  - Update data
  - Delete data

---

### 🔁 How They Work Together

1. User/application sends a request
2. Request goes to the **DBMS**
3. DBMS translates it into database operations
4. Database stores or retrieves data
5. Result is returned to the user

➡ **Users never interact directly with the database**

---

## 5️⃣ Responsibilities of a DBMS

A DBMS ensures:

- **Data organization**
- **Data integrity** (valid and correct data)
- **Data consistency**
- **Data security**
- **Concurrency control** (multiple users at once)
- **Recovery** in case of failures
- **Efficient querying**

---

## 6️⃣ Relational Database Management Systems (RDBMS)

An **RDBMS** is a type of DBMS that:
- Stores data in **tables (relations)**
- Uses **rows and columns**
- Supports relationships between tables

---

### 🔹 Examples of Popular DBMS / RDBMS

- MySQL
- PostgreSQL
- Oracle Database
- Microsoft SQL Server
- MongoDB (NoSQL DBMS)

---

## 7️⃣ Key Takeaways

- File-based systems suffer from redundancy, inconsistency, and poor security
- Databases provide **structured and reliable data storage**
- DBMS is the **interface** between users/applications and the database
- MySQL and Oracle are **DBMSs**, not databases
- RDBMS helps manage **relationships between data**

---

➡ **Next Topic:**  
Understanding **relationships in databases** and how an **RDBMS** manages them efficiently.

# 📘 Improving Data Management with RDBMS

---

## 1️⃣ Why Do We Need RDBMS?

You now understand the difference between a **database** and a **database management system (DBMS)**.  
A natural next question is:

- How is data stored inside a database?
- What if data is **interlinked**?
- How do we avoid the problems of **file-based storage systems**?

The answer lies in **Relational Database Management Systems (RDBMS)**.

---

## 2️⃣ What Is an RDBMS?

An **RDBMS** is a type of DBMS that:
- Stores data in the form of **tables**
- Maintains **relationships** between those tables
- Uses a **relational model** to organise data

Each table represents a **real-world entity**, and tables are linked using **keys**.

---

## 3️⃣ Real-World Analogy: Office Setup

Consider a simple office environment:

- **Employees** work in an organisation
- Every employee belongs to **one department**

Here, we have two real-world objects:
- Employee
- Department

These objects are **related**:
> Every employee is associated with a department.

An RDBMS helps us store:
- The employee data
- The department data
- The **relationship** between employees and departments

---

## 4️⃣ Tables in an RDBMS

### 🔹 Key Characteristics of Tables
- Every table has a **name**
- Data is stored in **rows and columns**
- The first row defines the **fields (attributes)**
- Each subsequent row represents a **record**

---

## 5️⃣ Example: Employee and Department Tables

### 📋 EMPLOYEE Table

| EMP_ID | NAME   | D_ID | SALARY |
|------|--------|------|--------|
| 1    | VISHWA | D01  | 55000  |
| 2    | MOHAN  | D02  | 60000  |
| 3    | SHIVA  | D03  | 72000  |

---

### 📋 DEPARTMENT Table

| D_ID | D_NAME  |
|----|----------|
| D01 | ACCOUNT  |
| D02 | HR       |
| D03 | SALES    |

---

### 🔍 Column Meanings
- **EMP_ID**: Employee ID  
- **D_ID**: Department ID  
- **D_NAME**: Department Name  

---

## 6️⃣ Entity in RDBMS

### 🔹 Definition
An **entity** is a real-world object that is represented as a table in a database.

### 🔹 Examples
- EMPLOYEE → Employee entity
- DEPARTMENT → Department entity

Each table corresponds to **one entity**.

---

## 7️⃣ Relationship Between Tables

### 🔗 How Are Relationships Built?

- The **EMPLOYEE** table contains a column `D_ID`
- The **DEPARTMENT** table also contains `D_ID`
- This common column links the two tables

➡ This relationship indicates **which department each employee belongs to**.

---

### 🔹 Relationship Explanation
- An employee **references** a department using `D_ID`
- This avoids duplication of department names
- Any update to department data is done **only once**

---

## 8️⃣ How RDBMS Solves File-System Problems

| File-Based System Issue | How RDBMS Solves It |
|------------------------|---------------------|
| Data redundancy | Data stored once, referenced using keys |
| Data inconsistency | Single source of truth |
| Scattered data | Centralised tables |
| Poor security | Role-based access control |
| No integrity constraints | Enforced via keys and rules |

---

## 9️⃣ Advantages of Relational Model

- Structured data storage
- Clear relationships between entities
- Reduced redundancy
- Improved consistency
- Easy querying using SQL
- Strong data integrity and security

---

##  🔑 Key Takeaways

- RDBMS stores data in **tables**
- Tables represent **entities**
- Relationships are maintained using **common keys**
- RDBMS overcomes major limitations of file-based systems
- Real-world relationships are preserved naturally

---

➡ **Next Topic:**  
How to **uniquely identify rows** in a table using **keys** (Primary Key, Foreign Key).

# 📘 Primary Key in RDBMS

---

## 1️⃣ Why Do We Need a Primary Key?

In any database table, there can be **hundreds or thousands of rows**, each representing a **distinct record** of an entity.

For example, in an **EMPLOYEE** table, each row represents a **different employee**.

### 📋 EMPLOYEE Table

| EMP_ID | NAME   | D_ID | SALARY |
|------|--------|------|--------|
| 1    | VISHWA | D01  | 55000  |
| 2    | MOHAN  | D02  | 60000  |
| 3    | SHIVA  | D03  | 72000  |

To **search**, **update**, or **delete** a specific employee record efficiently, the database must be able to **uniquely identify each row**.  
This is where the **primary key** becomes essential.

---

## 2️⃣ What Is a Primary Key?

A **primary key** is a special attribute (or a combination of attributes) in a table that is used to **uniquely identify each row (record)** in that table.

### 🔹 Definition
> A primary key uniquely identifies every record in a table and ensures data integrity.

---

## 3️⃣ Properties of a Primary Key

A primary key enforces an **entity constraint**, which ensures that each entity (row) is uniquely identifiable.

### ✅ Key Properties

#### 1. **Uniqueness**
- No two rows can have the same primary key value

#### 2. **Non-nullability**
- Primary key columns **cannot contain NULL values**
- Every record must have an identifier

Together, these properties guarantee that **each row is distinct**.

---

## 4️⃣ Example: Primary Key in EMPLOYEE Table

In the **EMPLOYEE** table:

- `EMP_ID` uniquely identifies each employee
- No two employees share the same `EMP_ID`
- `EMP_ID` cannot be NULL

➡ Therefore, **EMP_ID is the primary key** of the EMPLOYEE table.

---

## 5️⃣ Primary Key and Relationships Between Tables

Primary keys are not only used to identify rows **within a table**, but they are also critical for **establishing relationships between tables**.

### 📋 DEPARTMENT Table

| D_ID | D_NAME  |
|----|----------|
| D01 | ACCOUNT  |
| D02 | HR       |
| D03 | SALES    |

- `D_ID` is the **primary key** in the **DEPARTMENT** table
- The **EMPLOYEE** table also contains a `D_ID` column

This allows:
- Each employee to be linked to a department
- Data to be stored **without redundancy**

---

## 6️⃣ Candidate Keys and Alternate Keys

### 🔹 Candidate Key
A **candidate key** is a **minimal set of attributes** that can uniquely identify a row in a table.

- A table may have **multiple candidate keys**
- One candidate key is chosen as the **primary key**

### 🔹 Alternate Key
- Candidate keys **not selected** as the primary key
- These are called **alternate keys**

---

### 🧠 Example
If both `EMP_ID` and `EMAIL_ID` can uniquely identify employees:
- Both are **candidate keys**
- If `EMP_ID` is chosen as primary key
- `EMAIL_ID` becomes an **alternate key**

---

## 7️⃣ Why Primary Keys Are Important

Primary keys ensure:

- Efficient data retrieval
- Accurate updates and deletions
- Prevention of duplicate records
- Reliable table relationships
- Strong data integrity

---

## 8️⃣ Summary

| Concept | Description |
|------|-------------|
| Primary Key | Uniquely identifies each row |
| Uniqueness | No duplicate values allowed |
| Non-null | NULL values not allowed |
| Entity Constraint | Ensures row-level identity |
| Relationship Support | Enables table linking |
| Candidate Key | Possible primary keys |
| Alternate Key | Candidate keys not chosen |

---

## ✅ Key Takeaway

> A **primary key** is the backbone of a relational database—it guarantees **uniqueness, integrity, and meaningful relationships** between tables.

---

➡ **Next Topic:**  
How **primary keys and foreign keys** work together to enforce relationships in RDBMS.

# 📘 Foreign Key and Constraints in RDBMS

---

## 1️⃣ Why Do We Need Foreign Keys?

In a **relational database**, data is often spread across **multiple tables** to:

- Reduce data redundancy
- Improve organization
- Maintain consistency

However, once data is distributed, we must be able to **relate records across tables** meaningfully.  
This is achieved using **foreign keys**.

---

## 2️⃣ What Is a Foreign Key?

A **foreign key** is an attribute (or a set of attributes) in one table that **references the primary key of another table**.

### 🔹 Definition
> A foreign key is used to establish and enforce a **referential integrity constraint** between two related tables.

---

## 3️⃣ Example: EMPLOYEE and DEPARTMENT Tables

### 📋 DEPARTMENT Table

| D_ID | D_NAME |
|----|--------|
| D01 | ACCOUNT |
| D02 | HR |
| D03 | SALES |

- `D_ID` is the **primary key**

### 📋 EMPLOYEE Table

| EMP_ID | NAME   | D_ID | SALARY |
|------|--------|------|--------|
| 1    | VISHWA | D01  | 55000 |
| 2    | MOHAN  | D02  | 60000 |
| 3    | SHIVA  | D03  | 72000 |

- `EMP_ID` → Primary key of EMPLOYEE
- `D_ID` → **Foreign key** referencing `DEPARTMENT(D_ID)`

➡ Each employee is linked to a **valid department**.

---

## 4️⃣ Characteristics and Functions of a Foreign Key

### ✅ 1. Referential Integrity
- Every value in the foreign key column must:
  - Match a value in the referenced primary key **OR**
  - Be `NULL`

### ✅ 2. Data Consistency
- Prevents **orphan records**
- Example:
  - ❌ Employee assigned to a non-existent department
  - ✅ Only valid departments allowed

### ✅ 3. Relational Navigation
- Enables meaningful **JOIN operations**
- Allows querying data across multiple tables

### ✅ 4. Optional Relationships
- Foreign key columns **can allow NULL values**
- Represents optional relationships  
  (e.g., employee not yet assigned to a department)

---

## 5️⃣ What Are Constraints?

**Constraints** are rules enforced on columns to ensure **data validity and integrity**.

Besides **entity constraints** (primary keys) and **referential constraints** (foreign keys), we also have **domain constraints**.

---

## 6️⃣ Domain Constraints

Domain constraints restrict the **type and range** of values allowed in a column.

### 🔹 1. Data Type Constraint
- Ensures values match a specific data type
- Examples:
  - `INT`
  - `VARCHAR`
  - `DATE`

---

### 🔹 2. CHECK Constraint
- Restricts values based on a condition

#### 🧠 Example
```sql
CHECK (age >= 18)

# 📘 Data Structure in the Relational Model

---

## 1️⃣ Relational Model Overview

In an **RDBMS (Relational Database Management System)**, data is organised using the **relational model**.  
This model is the conceptual foundation on which all relational databases are built.

The relational model consists of **three major components**:

1. **Data Structure**
2. **Data Integrity**
3. **Data Manipulation**

In this section, we focus on the **first component: Data Structure**.

---

## 2️⃣ What Is Data Structure in the Relational Model?

The **data structure** defines **how data is stored and organised** in a relational database.

➡ In the relational model, **data is stored in the form of tables**, which are also called **relations**.

---

## 3️⃣ Tables (Relations)

A **relation (table)** is a structured arrangement of data in **rows and columns**.

Each table represents an **entity** from the real world (e.g., Employee, Department).

A relation consists of **two main parts**:

1. **Relation Heading**
2. **Relational Body**

---

## 4️⃣ Relation Heading (Schema)

The **relation heading** describes the **structure of the table**.

It includes:
- Column names (attributes)
- Data types for each column

### 🧾 Example: Relation Heading

| NAME        | DATATYPE |
|------------|---------|
| ID         | INTEGER |
| NAME       | STRING  |
| DEPARTMENT | STRING  |

### 🔹 Key Points
- Each column has a **unique name**
- Each column has a **defined data type**
- The heading defines **what kind of data** can be stored

---

## 5️⃣ Relational Body (Instance)

The **relational body** contains the **actual data** stored in the table.

- Each **row** represents a **record (tuple)**
- Each **cell** holds a **single atomic value**
- Values conform to the data types defined in the relation heading

### 🧾 Example: Relational Body

| ID | NAME   | DEPARTMENT |
|----|--------|------------|
| 1  | VISHWA | ACCOUNT    |
| 2  | MOHAN  | HR         |
| 3  | SHIVA  | SALES      |

---

## 6️⃣ Important Characteristics of Relational Data Structure

### ✅ Tabular Format
- Data is stored in rows and columns
- Easy to understand and manage

### ✅ Atomic Values
- Each cell contains a **single, indivisible value**
- No multi-valued or nested attributes

### ✅ Fixed Schema
- Structure (columns and data types) is predefined
- Ensures consistency across all records

### ✅ Uniform Rows
- Every row follows the same structure
- Each row represents one instance of the entity

---

## 7️⃣ Why Is Data Structure Important?

The relational data structure:

- Provides a **clear and standardised format** for storing data
- Makes data easy to **search, update, and maintain**
- Serves as the **foundation for relationships, constraints, and queries**
- Enables reliable implementation of **data integrity rules**
- Supports efficient **data manipulation operations**

---

## 8️⃣ Summary

| Component | Description |
|--------|------------|
| Table (Relation) | Stores data in rows and columns |
| Relation Heading | Defines column names and data types |
| Relational Body | Stores actual records (rows) |
| Cell | Contains a single atomic value |

---

## ✅ Key Takeaway

> In the relational model, **data structure defines how data is stored**—in the form of tables with clearly defined columns and rows. This structured organisation forms the backbone of all relational database operations.

---

➡ **Next Topic:**  
**Data Integrity in the Relational Model** – rules and constraints that ensure accuracy, validity, and consistency of data.

# 📘 Data Integrity in the Relational Model

---

## 1️⃣ What Is Data Integrity?

**Data integrity** ensures that the data stored in a relational database is:

- **Accurate**
- **Valid**
- **Consistent**
- **Reliable over time**

In an RDBMS, data integrity is maintained using a set of **rules and constraints** defined as part of the relational model.

---

## 2️⃣ Components of Data Integrity

The relational model ensures data integrity through **three major types of integrity constraints**:

1. **Attribute Integrity**
2. **Entity Integrity**
3. **Referential Integrity**

Each plays a distinct role in maintaining correctness and consistency.

---

## 3️⃣ Attribute Integrity

### 📌 Definition
**Attribute integrity** ensures that every attribute (column) in a table:

- Has a **defined name**
- Has a **defined data type**
- Accepts only values that match its data type and domain

### 🔹 How It Is Enforced
- Data type constraints (INTEGER, STRING, DATE, etc.)
- Domain constraints (allowed value ranges)
- NOT NULL constraints (when applicable)

### 🧾 Example

| ATTRIBUTE | DATATYPE |
|--------|---------|
| EMP_ID | INTEGER |
| NAME | STRING |
| SALARY | INTEGER |

✔ `SALARY = 55000` → valid  
❌ `SALARY = "High"` → invalid (datatype mismatch)

---

## 4️⃣ Entity Integrity

### 📌 Definition
**Entity integrity** ensures that **each row (entity)** in a table is **uniquely identifiable**.

This prevents duplicate or ambiguous records.

### 🔹 How It Is Enforced
- **Primary Key**
- **Composite Primary Key** (if a single column is insufficient)

### 🔑 Primary Key Rules
- Must be **unique**
- Must be **NOT NULL**

### 🧾 Example

**EMPLOYEE Table**

| EMP_ID (PK) | NAME | D_ID |
|-----------|------|------|
| 1 | VISHWA | D01 |
| 2 | MOHAN | D02 |

✔ EMP_ID uniquely identifies each employee  
❌ Duplicate EMP_ID values are not allowed

---

## 5️⃣ Referential Integrity

### 📌 Definition
**Referential integrity** ensures that **relationships between tables remain consistent**.

It guarantees that a foreign key value in one table:
- Exists as a primary key value in another table, **or**
- Is NULL (if allowed)

### 🔹 How It Is Enforced
- **Foreign Keys**

### 🧾 Example

**DEPARTMENT Table**

| D_ID (PK) | D_NAME |
|--------|--------|
| D01 | ACCOUNT |
| D02 | HR |

**EMPLOYEE Table**

| EMP_ID | NAME | D_ID (FK) |
|------|------|-----------|
| 1 | VISHWA | D01 |
| 2 | MOHAN | D02 |

✔ Valid relationship: D_ID exists in DEPARTMENT  
❌ D_ID = D99 → violates referential integrity

---

## 6️⃣ Why Data Integrity Matters

Maintaining data integrity helps to:

- Prevent incorrect or inconsistent data
- Avoid duplicate or orphan records
- Preserve relationships across tables
- Ensure trustworthy query results
- Support reliable decision-making

---

## 7️⃣ Summary Table

| Integrity Type | Ensures | Enforced By |
|-------------|--------|------------|
| Attribute Integrity | Valid column values | Data types, domain, NOT NULL |
| Entity Integrity | Unique rows | Primary / Composite keys |
| Referential Integrity | Consistent relationships | Foreign keys |

---

## ✅ Key Takeaway

> Data integrity in the relational model ensures that **data is valid at the attribute level, uniquely identifiable at the entity level, and consistently related across tables**.

---

➡ **Next Topic:**  
**Data Manipulation in the Relational Model** – operations such as inserting, updating, deleting, and querying data.

# 📘 Data Manipulation in the Relational Model

---

## 1️⃣ What Is Data Manipulation?

**Data manipulation** is the third core component of the **relational model**, after:

1. Data Structure  
2. Data Integrity  
3. **Data Manipulation** ✅

It focuses on **how data stored in relational tables can be retrieved, combined, and transformed** to produce meaningful results.

In simple terms:

> **Data manipulation allows users to perform operations on one or more tables (relations) to generate new tables (relations).**

---

## 2️⃣ Role of Data Manipulation in RDBMS

Data manipulation enables us to:

- Retrieve required data
- Insert new data
- Update existing data
- Combine data from multiple tables
- Transform existing data into new results

These operations form the basis of **querying and analytics** in relational databases.

---

## 3️⃣ Relational Algebra: The Foundation

Data manipulation in the relational model is based on **relational algebra**, which works similarly to **set operations** in mathematics.

### 🔹 Key Idea
- Tables are treated as **sets of rows**
- Operations are applied on one or more tables
- The **result is always another table (relation)**

---

## 4️⃣ Common Relational Algebra Operations

| Operation | Description |
|--------|------------|
| **Union (∪)** | Combines rows from two tables |
| **Intersection (∩)** | Returns common rows |
| **Difference (−)** | Rows in one table but not in another |
| **Cartesian Product (×)** | Combines every row of one table with every row of another |
| **Selection (σ)** | Filters rows based on conditions |
| **Projection (π)** | Selects specific columns |
| **Join (⨝)** | Combines related tables based on keys |

---

## 5️⃣ Example: Intersection Operation

### 🔹 Input Relations

**TABLE 1: EMPLOYEE_A**

| EMP_ID | NAME | D_ID |
|------|------|------|
| 1 | VISHWA | D01 |
| 2 | MOHAN | D02 |
| 3 | SHIVA | D03 |

**TABLE 2: EMPLOYEE_B**

| EMP_ID | NAME | D_ID |
|------|------|------|
| 3 | SHIVA | D03 |
| 4 | RAVI | D01 |

---

### 🔹 Intersection Result

**EMPLOYEE_A ∩ EMPLOYEE_B**

| EMP_ID | NAME | D_ID |
|------|------|------|
| 3 | SHIVA | D03 |

✔ Only **SHIVA** appears in both tables  
✔ Result is a **new relation**

---

## 6️⃣ Key Characteristics of Data Manipulation

- Operates on **relations (tables)**
- Uses **set-based operations**
- Output is **always another relation**
- Does **not modify original data directly**
- Forms the theoretical basis for SQL queries

---

## 7️⃣ Relation to SQL (Practical View)

Relational algebra concepts map directly to SQL:

| Relational Algebra | SQL Equivalent |
|------------------|---------------|
| Selection | `WHERE` |
| Projection | `SELECT columns` |
| Union | `UNION` |
| Intersection | `INTERSECT` |
| Difference | `EXCEPT` |
| Join | `JOIN` |

---

## 8️⃣ Why Data Manipulation Is Important

- Enables powerful querying
- Allows combining data from multiple tables
- Helps extract insights from stored data
- Preserves consistency through relational operations
- Supports decision-making and reporting

---

## 9️⃣ Summary

| Component | Purpose |
|--------|--------|
| Data Structure | Defines how data is stored |
| Data Integrity | Ensures correctness & consistency |
| **Data Manipulation** | Enables retrieval & transformation |

---

## ✅ Key Takeaway

> **Data manipulation allows us to apply relational algebra operations on one or more tables to generate new meaningful relations without violating data integrity.**

---

➡ **Next Topic:**  
**Entity-Relationship Diagrams (ERDs)** – understanding the physical and conceptual design of relational databases.

# 📘 Entity–Relationship Diagrams (ERDs)

---

## 1️⃣ Why Do We Need ERDs?

Imagine designing a database for a company that stores information about:

- Employees  
- Departments  
- Roles  
- Salary / Account details  
- Projects, customers, orders, etc.

When multiple tables exist, **understanding how they relate to each other becomes difficult** if we only look at table definitions.

👉 **Entity–Relationship Diagrams (ERDs)** help by providing a **visual blueprint** of the database before actual implementation.

---

## 2️⃣ What Is an ERD?

An **Entity–Relationship Diagram (ERD)** is a **visual representation** of:

- Entities (tables)
- Attributes (columns)
- Relationships between entities
- Cardinality (how many records relate)

> ERDs help database designers **plan, communicate, and validate** database structure.

---

## 3️⃣ Core Components of an ERD

### 🔹 1. Entity
An **entity** represents a real-world object stored as a table.

Examples:
- EMPLOYEE
- DEPARTMENT
- ROLE
- SALARY_ACCOUNT

Each entity:
- Has a unique name
- Contains attributes (columns)
- Has a primary key

---

### 🔹 2. Attributes
Attributes describe properties of an entity.

**EMPLOYEE**
- EMP_ID (Primary Key)
- NAME
- D_ID (Foreign Key)

**DEPARTMENT**
- D_ID (Primary Key)
- D_NAME

---

### 🔹 3. Relationships
Relationships describe **how entities interact**.

Example:
- An employee belongs to a department
- An employee has a salary account
- An employee performs roles

---

## 4️⃣ Cardinality in ERDs

**Cardinality** defines the **numerical relationship** between entities.

### 🔹 Types of Cardinality

---

### ✅ 1. One-to-One (1 : 1)

**Definition:**  
One record in Entity A corresponds to exactly one record in Entity B.

**Example:**  
- One employee ↔ One salary account

**Meaning:**
- Each employee has exactly one salary account
- Each salary account belongs to exactly one employee

---

### ✅ 2. One-to-Many (1 : N)

**Definition:**  
One record in Entity A corresponds to multiple records in Entity B.

**Example:**  
- One department → Many employees

**Meaning:**
- A department can have many employees
- Each employee belongs to **zero or one** department

---

### ✅ 3. Many-to-One (N : 1)

**Mirror of One-to-Many**

**Example:**  
- Many employees → One department

**Meaning:**
- Multiple employees can belong to the same department

---

### ✅ 4. Many-to-Many (M : N)

**Definition:**  
Multiple records in Entity A correspond to multiple records in Entity B.

**Example:**  
- Employees ↔ Roles

**Meaning:**
- One employee can have many roles
- One role can be assigned to many employees

⚠️ **Important:**  
Many-to-many relationships are implemented using a **junction (bridge) table**.

Example:

EMPLOYEE_ROLE

EMP_ID (FK)
ROLE_ID (FK)


---

## 5️⃣ Example ERD Relationships (Company Database)

### 🔹 Entities Involved
- EMPLOYEE
- DEPARTMENT
- SALARY
- ROLE

---

### 🔹 Relationship Summary

| Entity A | Relationship | Entity B |
|-------|-------------|---------|
| EMPLOYEE | Many-to-One | DEPARTMENT |
| EMPLOYEE | One-to-One | SALARY |
| EMPLOYEE | Many-to-Many | ROLE |

---

## 6️⃣ Optional Relationships (0 or 1)

Some relationships allow **NULL values**.

Example:
- A newly joined employee **may not yet be assigned** a department

This is shown as:
- Minimum: 0
- Maximum: 1

---

## 7️⃣ Why ERDs Are Important

✔ Help visualise complex schemas  
✔ Prevent design mistakes early  
✔ Improve communication between teams  
✔ Serve as documentation  
✔ Make database scalable and maintainable  

---

## 8️⃣ ERD vs Tables

| ERD | Tables |
|----|-------|
| Conceptual design | Physical implementation |
| Visual | Text-based |
| Used during planning | Used during execution |

---

## 9️⃣ Summary

- ERDs visually represent database structure
- Entities represent tables
- Relationships show how tables interact
- Cardinality defines numerical constraints
- ERDs are created **before writing SQL**

---

## ✅ Key Takeaway

> **An ERD is a blueprint of the database that shows entities, their attributes, and the relationships between them—making complex systems easy to understand and design.**

---

➡ **Next Topic:**  
**Identifying Rows Using Primary Keys and Understanding Weak Entities**


# 📘 Schema in Relational Databases

---

## 1️⃣ What Is a Schema?

You already learned about **Entity–Relationship Diagrams (ERDs)**, which visually show tables and their interactions.  
A **schema** provides a **logical view** of the database structure and explains:

- What tables exist
- What fields (columns) they contain
- Data types of fields
- How tables are related to each other

👉 A schema helps us **understand, design, and optimise** a relational database.

---

## 2️⃣ Facts vs Dimensions

In real-world datasets (often stored initially as flat files), we usually have two kinds of data:

### 🔹 Facts
- Numerical / quantitative values
- Used for analysis and aggregation

**Examples:**
- Sale amount
- Profit
- Quantity sold
- Price

---

### 🔹 Dimensions
- Descriptive / contextual data
- Provide meaning to facts

**Examples:**
- Customer name
- Order ID
- Product details
- Address
- Date

A **well-designed schema separates facts and dimensions** into structured tables instead of keeping everything in one flat file.

---

## 3️⃣ Common Schema Designs

The two most common dimensional modelling schemas are:

1. **Star Schema**
2. **Snowflake Schema**

---

## ⭐ Star Schema

### 🔹 Definition
The **star schema** is the simplest and most widely used schema design.

- A **central fact table** stores measurable data
- Multiple **dimension tables** surround it
- Each dimension connects **directly** to the fact table
- The layout resembles a ⭐ star

---

### 🔹 Structure


---

### 🔹 Example (Sales Schema)

**Fact Table: SALES_FACT**
- sale_id
- order_id
- user_id
- item_id
- sale_amount
- sale_profit
- item_price

**Dimension Tables:**
- Customer
- Order
- Product
- Time / Store (optional)

---

### 🔹 Advantages
✔ Simple design  
✔ Fast query performance  
✔ Easy to understand and use  

⚠️ Disadvantage:
- Some redundancy in dimension tables

---

## ❄️ Snowflake Schema

### 🔹 Definition
The **snowflake schema** is a more **normalised** version of the star schema.

- Dimension tables are broken into **sub-dimensions**
- Structure resembles a ❄️ snowflake
- Reduces redundancy

---

### 🔹 Example

Instead of a single Customer table:

- CUSTOMER (customer_id, name)
- ADDRESS (address_id, city, state)
- REGION (region_id, country)


---

### 🔹 Advantages
✔ Reduced redundancy  
✔ Better data integrity  
✔ Efficient storage  

⚠️ Disadvantages:
- More joins required
- Slightly slower query performance
- More complex design

---

## 4️⃣ Normalisation (Why Snowflake Exists)

**Normalisation** is the process of:
- Dividing large tables into smaller related tables
- Reducing redundancy and dependency
- Improving consistency

Snowflake schema applies **normalisation to dimension tables**.

---

## 5️⃣ Problem with the Given Flat Table

### ❌ Original Flat Table (Issues)

| id | order_id | user_id | user_name | user_address | sale_id | sale_amount | sale_profit | item_id | item_name | item_price |
|----|---------|---------|-----------|--------------|--------|-------------|-------------|---------|-----------|------------|
| 1 | Ord_101 | user_xxx | usr_name_xxx | usr_add | sale_xx | sale_amt_xx | sale_pft_xx | item_xxx | item_name_xxx | item_price_xxx |
| 2 | Ord_102 | user_xxx | usr_name_xxx | usr_add | sale_xx | sale_amt_xx | sale_pft_xx | item_xxx | item_name_xxx | item_price_xxx |
| 3 | Ord_103 | user_xxx | usr_name_xxx | usr_add | sale_xx | sale_amt_xx | sale_pft_xx | item_xxx | item_name_xxx | item_price_xxx |

### ❌ Problems
- Massive data redundancy
- User and item data repeated
- Difficult to update
- Poor scalability

---

## 6️⃣ Fixed Design Using ⭐ Star Schema

### ✅ Fact Table

#### SALES_FACT

| sale_id | order_id | user_id | item_id | sale_amount | sale_profit | item_price |
|-------|---------|--------|--------|-------------|-------------|------------|
| S01 | Ord_101 | U01 | I01 | 1200 | 200 | 400 |
| S02 | Ord_102 | U01 | I01 | 1200 | 180 | 400 |
| S03 | Ord_103 | U01 | I01 | 1200 | 220 | 400 |

---

### ✅ Dimension Tables

#### USER_DIMENSION

| user_id | user_name | user_address |
|-------|-----------|--------------|
| U01 | Alice | Bangalore |

---

#### ORDER_DIMENSION

| order_id | order_details |
|--------|---------------|
| Ord_101 | Online |
| Ord_102 | Online |
| Ord_103 | Store |

---

#### ITEM_DIMENSION

| item_id | item_name | item_price | item_details |
|-------|----------|------------|--------------|
| I01 | Laptop | 400 | Electronics |

---

#### SALES_DIMENSION

| sale_id | sale_amount | sale_profit |
|-------|-------------|-------------|
| S01 | 1200 | 200 |
| S02 | 1200 | 180 |
| S03 | 1200 | 220 |

---

## 7️⃣ Facts and Dimensions (Final Summary)

### 🔹 Facts
- sale_id
- order_id
- user_id
- item_id
- sale_amount
- sale_profit
- item_price

---

### 🔹 Dimensions
- **User Dimension:** (user_id, user_name, user_address)
- **Order Dimension:** (order_id, order_details)
- **Item/Product Dimension:** (item_id, item_name, item_price, item_details)
- **Sales Dimension:** (sale_id, sale_amount, sale_profit)

---

## 8️⃣ Key Takeaways

- A **schema** is the logical blueprint of a database
- **Star schema** prioritises simplicity and speed
- **Snowflake schema** prioritises storage efficiency and integrity
- Separating facts and dimensions improves:
  - Performance
  - Maintainability
  - Scalability
- Flat files are transformed into structured schemas for analytics

---

## ✅ Final One-Liner

> **A schema organises raw data into meaningful fact and dimension tables, enabling efficient querying, consistency, and scalable analytics.**
