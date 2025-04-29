### 📁 `onLoad` Client Script - ServiceNow  
> A collection of essential `g_form` methods used in `onLoad` client scripts with short use-case examples.

---

## 🔧 Usage Overview

| **Method**        | **Purpose**                                         |
|:------------------|:-----------------------------------------------------|
| `setValue`         | Set default field values.                           |
| `getValue`         | Fetch current field value.                          |
| `setDisplay`       | Show/hide fields (keeps layout space).              |
| `setVisible`       | Fully hide/show fields (no space reserved).         |
| `addInfoMessage`   | Display informational messages.                     |
| `addErrorMessage`  | Display error messages.                             |
| `setReadOnly`      | Make a field read-only.                             |
| `showFieldMsg`     | Show field-level error or info message.             |
| `clearValue`       | Clear existing field data.                          |
| `isNewRecord`      | Check if the form is a new record.                  |

---

## ✅ Script Examples

### 1. `setValue`
```javascript
function onLoad() {
    g_form.setValue('priority', '3 - Moderate');
}
```

### 2. `getValue`
```javascript
function onLoad() {
    var caller = g_form.getValue('caller_id');
    if (!caller) {
        g_form.addInfoMessage('Please select a caller.');
    }
}
```

### 3. `setDisplay`
```javascript
function onLoad() {
    if (!g_form.getValue('service')) {
        g_form.setDisplay('service_offering', false);
    }
}
```

### 4. `setVisible`
```javascript
function onLoad() {
    if (g_user.hasRole('admin')) {
        g_form.setVisible('priority', true);
    }
}
```

### 5. `addInfoMessage`
```javascript
function onLoad() {
    g_form.addInfoMessage('Remember to save your work!');
}
```

### 6. `addErrorMessage`
```javascript
function onLoad() {
    if (!g_user.hasRole('itil')) {
        g_form.addErrorMessage('You do not have permission to edit this ticket.');
    }
}
```

### 7. `setReadOnly`
```javascript
function onLoad() {
    g_form.setReadOnly('impact', true);
}
```

### 8. `showFieldMsg`
```javascript
function onLoad() {
    g_form.showFieldMsg('assignment_group', 'Assignment group is mandatory', 'error');
}
```

### 9. `clearValue`
```javascript
function onLoad() {
    g_form.clearValue('description');
}
```

### 10. `isNewRecord`
```javascript
function onLoad() {
    if (g_form.isNewRecord()) {
        g_form.setValue('state', 'New');
    }
}
```

---

## 📌 Notes
- Use only one `onLoad()` function per client script.
- Avoid placing onChange-like logic inside onLoad.
- Always test scripts in dev or sub-prod environments before production use.

---
