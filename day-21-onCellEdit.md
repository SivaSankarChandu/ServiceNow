# 🔒 ServiceNow onCellEdit – Prevent Unauthorized Inline Edits

## 📘 Scenario: Block List View Edits for Unauthorized Users

This `onCellEdit` client script helps prevent users from editing records directly in **list view**. It alerts the user and cancels the edit operation, protecting the data from unauthorized changes.

---

## 💡 Use Case

In many enterprise ServiceNow environments, not all users should be allowed to perform **inline edits** directly from the list view.

For example:
- **Interns** or **trainees** should only have view access.
- **Contractors** should update data only through forms with validations.
- **Auditors** may have read-only roles but access to lists.

Using this script, you can cancel list cell edits and notify the user.

---

## 💻 Script

```javascript
function onCellEdit(sysIDs, table, oldValues, newValue, callback) {
  var saveAndClose = false;
  // Show alert and cancel the edit
  alert("You don't have access to edit data");
  callback(saveAndClose);
}


⚙️ How It Works
This script is triggered when a user makes an edit in a list view cell.

It sets saveAndClose = false, which tells ServiceNow not to save the changes.

The user sees an alert and their edit is discarded.

✅ Benefits
Prevents unauthorized changes directly from list views.

Easy to implement and lightweight.

Useful for environments where strict data control is required.

📌 Notes
This is a client-side script. It doesn’t rely on GlideRecord or server calls.

You can enhance it to check roles using g_user.hasRole('role_name').

🔗 Related Topics
onCellEdit vs onChange

Restricting field-level access with ACLs

Using UI Policies for form-level restrictions

