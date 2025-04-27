# 🚀 ServiceNow Scripting: onLoad Client Script

## Scenario 1: Show Info Message on Form Load in ServiceNow

In ServiceNow, the `onLoad` client script is a great way to guide users when they open a form.

### 📄 Script Example

```javascript
function onLoad() {
   // Display an informational message when the form loads
   g_form.addInfoMessage('Please review all mandatory fields before submitting.');
}
```

### 📌 Explanation
- **Purpose:** Display an info message when the form is loaded.
- **Benefit:** Reminds users to review all mandatory fields before submitting, reducing form errors and improving user experience.

---
