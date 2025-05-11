# 🚀 25+ Must-Know Server-Side Methods in ServiceNow

Mastering server-side scripting in ServiceNow is key to building powerful and scalable applications. Below is a well-organized cheat sheet of essential **GlideRecord** and **GlideSystem (gs)** methods used across Script Includes, Business Rules, Scheduled Jobs, and more.

---

## 🔍 Querying & Record Navigation

| Method | Description |
|--------|-------------|
| 🧩 `addQuery(field, operator, value)` | Add a condition to filter records |
| 🧩 `addEncodedQuery(query)` | Add encoded query (e.g., `active=true^priority=1`) |
| ▶️ `query()` | Execute the query |
| ➡️ `next()` | Move to the next record |
| 🔁 `hasNext()` | Check if another record exists |
| ⬆️ `orderBy(field)` | Sort ascending |
| ⬇️ `orderByDesc(field)` | Sort descending |
| 🔢 `setLimit(n)` | Limit number of results |

---

## 📄 Field Operations

| Method | Description |
|--------|-------------|
| 📥 `getValue(field)` | Get raw database value |
| 📤 `setValue(field, value)` | Set a field’s value |
| 🎨 `getDisplayValue(field)` | Get display-friendly value |
| ✅ `isValidField(field)` | Check if a field exists |
| 🧪 `isValidRecord()` | Check if the record is valid |
| 🆕 `isNewRecord()` | Is the record new and unsaved? |
| 🔍 `changes(field)` | Did a field change? |
| ↩️ `getPreviousValue(field)` | Get old value before update |

---

## 🛠️ CRUD (Create, Read, Update, Delete)

| Method | Description |
|--------|-------------|
| 🧾 `insert()` | Insert a new record |
| 💾 `update()` | Save changes to DB |
| 🗑️ `deleteRecord()` | Delete the current record |
| 🧼 `initialize()` | Prepare a clean record |
| 📄 `newRecord()` | Create a new empty record |
| 🔕 `setWorkflow(false)` | Disable business rules/workflows |
| 🔧 `autoSysFields(false)` | Skip auto sys fields |
| 🆔 `setNewGuid()` | Assign a new Sys ID |

---

## 👤 User & System Context (`gs` methods)

| Method | Description |
|--------|-------------|
| 🧑‍💻 `gs.getUserID()` | Get current user’s sys_id |
| 🆔 `gs.getUserName()` | Get current username |
| 👥 `gs.getUser()` | GlideUser object |
| 🛡️ `gs.hasRole('role')` | Check if user has a role |
| ⚙️ `gs.getProperty('name')` | Get a system property |

---

## 💡 Why It Matters

These methods form the foundation of server-side logic in ServiceNow. By mastering them, you can:

- Build clean, efficient business logic
- Avoid performance issues
- Maintain readable, scalable code

---
