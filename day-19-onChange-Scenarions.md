
## 📌 ServiceNow — onChange Client Script Scenarios

This repository showcases 4 practical `onChange` Client Script use cases in ServiceNow that enhance form interactivity, ensure data consistency, and improve user experience.

### 1️⃣ Category → Auto-Set Subcategory

**Scenario**: When "network" is selected as the category, auto-fill subcategory as "wireless".

```javascript
function onChange(control, oldValue, newValue, isLoading, isTemplate) {
  if (g_form.getValue('category') == 'network') {
    g_form.setValue('subcategory', 'wireless');
  }
}
```

---

### 2️⃣ Category → Prefill Description

**Scenario**: When category is "network", auto-fill the description to guide the user.

```javascript
function onChange(control, oldValue, newValue, isLoading, isTemplate) {
  if (g_form.getValue('category') == 'network') {
    g_form.setValue('description', 'Please describe your network issue in detail.');
  }
}
```

---

### 3️⃣ Priority → Toggle Description Visibility

**Scenario**: Show the description field only when priority is "1 - Critical".

```javascript
function onChange(control, oldValue, newValue, isLoading, isTemplate) {
  if (parseInt(g_form.getValue('priority'), 10) === 1) {
    g_form.setDisplay('description', true);
  } else {
    g_form.setDisplay('description', false);
  }
}
```

---

### 4️⃣ Service → Make Service Offering Mandatory

**Scenario**: Make `service_offering` field mandatory if a service is selected.

```javascript
function onChange(control, oldValue, newValue, isLoading, isTemplate) {
  if (!g_form.getValue('service')) {
    g_form.setMandatory('service_offering', true);
  } else {
    g_form.setMandatory('service_offering', false);
  }
}
```
