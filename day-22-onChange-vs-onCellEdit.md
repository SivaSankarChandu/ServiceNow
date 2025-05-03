# 🔄 ServiceNow: onChange vs onCellEdit 🎯

Client-side scripts like `onChange` and `onCellEdit` play a crucial role in enhancing user experience and enforcing business rules in ServiceNow. Here's a clear comparison of when and how to use them.

---

## 🚀 `onChange` Client Script

### ⚙️ Trigger
Triggered when a **field value changes on a form**.

### 📍 Behavior
Executes **when the user changes a field** and **moves the focus away** (blur event).

### 🛠️ Common Use Cases
- 👉 Dynamic form behavior (e.g., show/hide fields)
- 👉 Field validation
- 👉 Auto-populating related values

### 💡 Example
```
function onChange(control, oldValue, newValue, isLoading) {
  if (isLoading || newValue === '') return;

  if (newValue === 'Resolved') {
    gForm.setVisible('resolution_code', true);
  }
}
```
---

## 🖱️ `onCellEdit` Client Script
### ⚙️ Trigger
Fires when a field is edited directly in the list (grid) view.

### 📍 Behavior
Runs only in the list view, not on the form.

### 🛠️ Common Use Cases
👉 Preventing unauthorized inline edits

👉 Real-time validation of grid edits

### 💡 Example
```
function onCellEdit(sysIDs, table, oldValues, newValue, callback) {
  var saveAndClose = false;
  alert("You don't have access to edit data.");
  callback(saveAndClose);
}
```
## ⚠️ Key Difference
Feature	onChange	onCellEdit
Scope	Form view	List (grid) view
Trigger	Field value changes on blur	Field edited in list
Use Cases	Dynamic UI, validation, show/hide	Block unauthorized list edits

## ✅ Conclusion
Choose the right client script based on your use case.
Let the platform work smart 💡
