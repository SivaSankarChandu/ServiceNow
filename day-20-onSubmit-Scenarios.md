# 🚀 ServiceNow onSubmit() Client Script – Validation Scenarios

This repository contains an example of a **Client Script** in ServiceNow that performs common form-level validations using the `onSubmit()` function.

## 🔍 Objective

Enhance data integrity and user experience by preventing form submission under specific conditions using client-side logic.

---

## 🧠 Validation Scenarios Implemented

1. ✅ **Prevent submission if the Description field is empty**  
2. ⚠️ **Prompt confirmation if Priority is set to 'Critical'**  
3. 🚫 **Block submission if Category or Subcategory is empty**

---

## 🧾 Client Script Code (onSubmit)

```javascript
function onSubmit() {
  // 1. Prevent submission if Description is empty
  if (!g_form.getValue('description')) {
    g_form.showFieldMsg('description', 'Description is required.', 'error');
    return false;
  }

  // 2. Confirm when Priority is Critical
  var priority = g_form.getValue('priority');
  if (priority == '1') { // '1' usually represents Critical in ServiceNow
    var confirmCritical = confirm('Critical priority selected. Proceed?');
    if (!confirmCritical) {
      alert('Submission cancelled');
      return false;
    }
  }

  // 3. Require both Category & Subcategory
  if (!g_form.getValue('category') || !g_form.getValue('subcategory')) {
    if (!g_form.getValue('category'))
      g_form.showFieldMsg('category', 'Category is required.', 'error');
    if (!g_form.getValue('subcategory'))
      g_form.showFieldMsg('subcategory', 'Subcategory is required.', 'error');
    return false;
  }

  // All validations passed
  return true;
}
```

---

## 📌 Notes

- This script is intended for **Incident** or similar forms.
- Priority value `'1'` corresponds to **Critical** in most ServiceNow default configurations.
- Adjust field names as needed based on your specific form/table.

---

## 🛠️ Technologies Used

- ServiceNow
- GlideForm (g_form)
- JavaScript (Client Script)

---

## 📚 Learning Outcome

By implementing this, you’ll understand:

- How to write `onSubmit` client scripts in ServiceNow.
- How to use `g_form` to validate and block form submission.
- How to enhance form interaction using confirmation dialogs and field messages.

---
