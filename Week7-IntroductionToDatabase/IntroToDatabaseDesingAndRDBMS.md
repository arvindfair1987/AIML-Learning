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

