````markdown
# 🔒 ServiceNow onCellEdit Script – Prevent Unauthorized Inline Edits

## 📘 Scenario: Block List View Edits for Unauthorized Users

This `onCellEdit` client script is designed to **prevent users from editing records directly from list views** in ServiceNow. Instead of applying the change, the script cancels the edit and displays an alert.

---

## 💡 Use Case

In some environments, you may want to block inline edits for certain users (e.g., interns, contractors, or read-only roles) to prevent accidental or unauthorized changes in list view.

---

## 🧠 Script

```javascript
function onCellEdit(sysIDs, table, oldValues, newValue, callback) {
  var saveAndClose = false;
  // Block the edit and notify the user
  alert("You don't have access to edit data");
  callback(saveAndClose);
}
````

---

## ⚙️ How It Works

* Triggered when a user edits a cell in an editable list.
* Displays an **alert message** to the user.
* Prevents the update from being saved (`saveAndClose = false`).
* Can be extended to include role-based checks using `g_user.hasRole()`.

---

## ✅ Benefits

* Ensures data integrity by reducing unauthorized edits.
* Prevents inline updates without changing form-level permissions.
* Simple and effective client-side control.

---

## 📌 Notes

* This script only works in editable **list views** (not on forms).
* For more advanced restrictions, consider combining with server-side logic or ACLs.

---

## 🧩 Optional Enhancements

You can expand this logic to:

* Allow edits only for users with specific roles.
* Restrict edits to specific tables or fields.
* Display a custom modal or UI message instead of `alert()`.

---
