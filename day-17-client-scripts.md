# Different Types of Client Scripts in ServiceNow

Client Scripts are essential in ServiceNow to make forms dynamic, validate user inputs, and improve the overall user experience by running scripts directly in the browser.

---

## 📚 Overview

In ServiceNow, there are four types of Client Scripts:

| Client Script Type | When It Runs                     | Key Use Case Example                   |
|--------------------|-----------------------------------|----------------------------------------|
| `onLoad`            | When a form is loaded             | Hide a field based on user's role      |
| `onChange`          | When a field value changes        | Make a related field mandatory         |
| `onSubmit`          | When a form is submitted          | Prevent submission if validations fail |
| `onCellEdit`        | When a list cell is edited        | Auto-update another field on edit      |

---

## 📈 Use Case Diagram

```
                      +-------------------+
                      |   User Opens Form  |
                      +---------+---------+
                                |
                         (onLoad fires)
                                ↓
              +----------------+----------------+
              |                                 |
  +-----------+-----------+         +----------+----------+
  | User Changes Field     |         | User Edits List Cell |
  +-----------+------------+         +----------+----------+
              |                                  |
       (onChange fires)                   (onCellEdit fires)
              ↓                                  ↓
  +-----------+------------+         +----------+-----------+
  | User Submits the Form   |
  +-----------+------------+
              |
        (onSubmit fires)
```

---

## 💻 Code Snippets

```javascript
// onLoad Client Script
function onLoad() {
    g_form.setVisible('priority', false);
}

// onChange Client Script
function onChange(control, oldValue, newValue, isLoading) {
    if (newValue == 'High') {
        g_form.setMandatory('impact', true);
    }
}

// onSubmit Client Script
function onSubmit() {
    if (g_form.getValue('short_description') == '') {
        alert('Short Description is mandatory!');
        return false;
    }
    return true;
}

// onCellEdit Client Script
function onCellEdit(sysIDs, table, modifiedFields) {
    // Logic to handle list edits
}
```

---

## 🛠️ Why Use Client Scripts?

- 🔥 Improve user experience
- ⚡ Reduce server calls
- ✅ Validate data early
- 🎯 Create smart and interactive forms

---
