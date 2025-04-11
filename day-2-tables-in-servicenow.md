# Day 2: Tables, Rows & Columns in ServiceNow

## 📊 Introduction
ServiceNow stores all data in **tables**, just like a database or spreadsheet. Each table contains **rows** (records) and **columns** (fields).

---

## 🧱 Table Types in ServiceNow

### 1. Base Tables
Foundational tables that other tables can extend.  
**Example:** `Task`, `CMDB`, `User`

### 2. Core Tables
Built-in default tables for standard modules.  
**Example:** `sys_user`, `incident`, `cmdb_ci`

### 3. Custom Tables
User-created tables tailored to specific needs.  
**Example:** `u_employee_approvals`

---

## 📌 Understanding Rows & Columns

### 🔹 Rows = Records
Each **row** is a unique record.  
For example, a new incident created in the `incident` table is one row.

### 🔹 Columns = Fields
Each **column** represents a specific piece of data.  
Example fields: `Number`, `State`, `Priority`, `Assigned to`

| Number | Short Description | Priority | Assigned To |
|--------|--------------------|----------|-------------|
| INC001 | VPN not working    | High     | John Smith  |

---

## 🧠 Why This Matters
- Understanding table structure is crucial for form design, scripting, and workflows.
- Helps in building custom reports and automations.
