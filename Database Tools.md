# 📘 SQL (MySQL) vs NoSQL (MongoDB)

---

![SQL vs NoSQL Diagram](https://github.com/satishsalyal/Foundations-of-Data-Science/blob/main/sqlnosql.png)

## 🔹 What is SQL (MySQL)?

**SQL (Structured Query Language)** is the standard language used to interact with **Relational Database Management Systems (RDBMS)** such as **MySQL, PostgreSQL, Oracle, SQL Server**, etc.

SQL databases store data in **tables**, which consist of **rows** and **columns**, and tables are connected through **relationships**.

### **Characteristics**

* Data is **structured**
* Requires a **predefined schema**
* Supports **relationships**
* Uses SQL for queries
* Follows **ACID Properties**

---

### 🔸 Example – MySQL Table

**Employee Table**

| id | name | department_id | salary |
| -- | ---- | ------------- | ------ |
| 1  | John | 10            | 50000  |
| 2  | Sara | 20            | 60000  |

**Department Table**

| department_id | department_name |
| ------------- | --------------- |
| 10            | HR              |
| 20            | IT              |

---

### 🔸 Relationships Example

1. **One-to-One**
   One employee has one profile.

2. **One-to-Many**
   One department has many employees.

3. **Many-to-Many**
   Students can enroll in many courses; courses have many students.

4. **Self-Referencing**
   Employee table where *manager_id* refers to another *employee_id* in the same table.

---

### 🔸 SQL Query Example

```sql
SELECT name, salary
FROM Employee
WHERE department_id = 20;
```

This retrieves all employees from the IT department.

---

## 🔹 What is NoSQL (MongoDB)?

**NoSQL (Not Only SQL)** databases are used for storing **unstructured, semi-structured, or flexible** data. MongoDB is a popular **document-based NoSQL database**.

### **Characteristics**

* Data is stored in **collections** (similar to tables)
* Each collection contains **documents** (similar to records)
* Documents are stored in **BSON/JSON format**
* Schema is **flexible / dynamic**
* Horizontally scalable

---

### 🔸 Example – MongoDB Document

A MongoDB **document** from *employees* collection:

```json
{
  "_id": 1,
  "name": "John",
  "department": "IT",
  "skills": ["Java", "Node", "MongoDB"]
}
```

Another document can have **different fields**:

```json
{
  "_id": 2,
  "name": "Sara",
  "department": "HR",
  "experience": 5
}
```

Because MongoDB allows **dynamic schema**, it doesn’t force all documents to have the same structure.

---

### 🔸 MongoDB Query Example

```js
db.employees.find({ department: "IT" })
```

---

## 🔹 SQL (MySQL) vs NoSQL (MongoDB)

### **Major Differences**

| Feature        | SQL (MySQL)    | NoSQL (MongoDB)           |
| -------------- | -------------- | ------------------------- |
| Structure      | Tables         | Collections & Documents   |
| Schema         | Fixed          | Dynamic                   |
| Relationships  | Strong support | Limited / manual          |
| Query Language | SQL            | JSON-like Query           |
| Scalability    | Vertical       | Horizontal                |
| Data Type      | Structured     | Semi-Structured           |
| Best Use       | Transactions   | Big Data / Real-time Apps |

---

## 🔹 Examples of SQL and NoSQL

### **SQL Examples (MySQL)**

* Banking systems
* Railway reservations
* Inventory management
* Student records database

### **NoSQL Examples (MongoDB)**

* Real-time analytics
* Product catalogs (Amazon-like)
* Social networks (posts, comments)
* IoT device data
* User activity logs

---

## 🔹 Difference Between SQL & NoSQL — Detailed Explanation

### **1. Type of Database**

* **SQL** → Relational, table-based
* **NoSQL** → Non-relational (Document, Key-Value, Column, Graph)

---

### **2. Schema**

* **SQL** → Predefined, strict
* **NoSQL** → Dynamic, flexible

**Example:**
In MongoDB, you can add new fields anytime:

```json
{ "name": "Mike", "email": "mike@gmail.com" }
```

Later:

```json
{ "name": "Mike", "email": "mike@gmail.com", "age": 25 }
```

SQL does not allow this unless you alter table.

---

### **3. Database Categories**

| Type            | Examples              |
| --------------- | --------------------- |
| **Document**    | MongoDB, CouchDB      |
| **Key-Value**   | Redis, DynamoDB       |
| **Wide-Column** | Cassandra, HBase      |
| **Graph**       | Neo4j, Amazon Neptune |

---

### **4. Complex Queries**

**SQL** → Excellent for joins, aggregations, nested queries

**Example MySQL:**

```sql
SELECT employees.name, departments.department_name
FROM employees
JOIN departments ON employees.department_id = departments.id;
```

**NoSQL** → Poor for multi-table joins
MongoDB supports simple joins using `$lookup`.

---

### **5. Hierarchical Data Storage**

NoSQL stores data in JSON-like form, so hierarchical data fits naturally.

```json
{
  "employee": {
    "name": "John",
    "address": {
       "city": "Delhi",
       "pincode": 110001
    }
  }
}
```

SQL would require multiple tables.

---

### **6. Scalability**

* **SQL** → Vertical scaling (upgrade RAM, CPU)
* **NoSQL** → Horizontal scaling (add more servers)

Example:
MongoDB clusters scale easily with **sharding**.

---

### **7. Language**

* SQL → Uses **SQL**
* NoSQL → Uses **UnQL** (varies by DB)

---

### **8. Online Processing**

| SQL                       | NoSQL                      |
| ------------------------- | -------------------------- |
| OLTP (transactional apps) | OLAP (analytics, big data) |

Example:

* Bank money transfer → SQL
* Real-time traffic analytics → NoSQL

---

### **9. Base Properties**

### **SQL → ACID**

Ensures reliable transactions.

Example:
If a money transfer fails midway → entire transaction rolls back.

### **NoSQL → CAP**

Choose any two of:

* Consistency
* Availability
* Partition Tolerance

MongoDB often prioritizes **Availability + Partition Tolerance**.

---

### **10. External Support**

* SQL → Mature, 40+ years old
* NoSQL → Newer, community-driven

---

## 🔹 Demo: Insert Data Into Tables and Collections

### **MySQL (SQL) Insert Example**

```sql
INSERT INTO Employee (id, name, department_id, salary)
VALUES (1, 'John', 10, 50000);
```

---

### **MongoDB Insert Example**

```js
db.Employee.insertOne({
  _id: 1,
  name: "John",
  department: "IT",
  salary: 50000
});
```

---

# ✅ Final Summary Table

| Key Areas       | SQL (MySQL)  | NoSQL (MongoDB)      |
| --------------- | ------------ | -------------------- |
| Type            | Relational   | Non-Relational       |
| Schema          | Fixed        | Flexible             |
| Data Format     | Tables       | JSON-like documents  |
| Best For        | Transactions | Big Data / Real-time |
| Scalability     | Vertical     | Horizontal           |
| Query Language  | SQL          | Mongo Query          |
| Storage         | Row-Column   | BSON/JSON            |
| Complex Queries | Excellent    | Limited              |
| Base Model      | ACID         | CAP                  |
| Relationships   | Strong       | Weak                 |

---


