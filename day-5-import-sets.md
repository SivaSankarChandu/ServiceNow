# Day 5: Import Sets in ServiceNow

## 📥 What are Import Sets?

Import Sets allow you to bring data from external sources (CSV, Excel, JDBC, etc.) into ServiceNow via a temporary staging table.

---

## 🔄 Import Set Process

1. **Load Data**  
   - Upload a data file or connect via integration  
   - Data goes into a staging table (e.g., u_import_users)

2. **Transform Map**  
   - Maps fields from staging table to target table  
   - Contains optional scripts and conditions

3. **Run Transform**  
   - Moves data into the final destination table  
   - Example: From `u_import_users` to `sys_user`

---

## ⚙️ Components

- **Import Set Table** (Staging Table)
- **Transform Map**
- **Field Maps**
- **Transform Scripts**
- **Run History**

---

## 📎 Use Cases

- Importing user records  
- Bulk updating CMDB data  
- Migrating from legacy tools  

---

## 🧠 Tips

- Use test files for validation  
- Always review transform scripts before running  
- Monitor Run History for issues
