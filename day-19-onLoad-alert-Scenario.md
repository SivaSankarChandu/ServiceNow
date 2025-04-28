---

```
# ServiceNow onLoad Alert() Scripts

A collection of simple onLoad Client Scripts for ServiceNow forms that instantly alert users in key scenarios, improving data accuracy and user guidance.

## Scenarios

| #  | Scenario                       | File                                   |
|----|--------------------------------|----------------------------------------|
| 1  | Priority 1 Incident Alert      | `scripts/1-alert-priority1-incident.js` |
| 2  | Short Description Validation   | `scripts/2-validate-short-description.js` |
| 3  | Problem Record Notification    | `scripts/3-problem-record-notification.js` |
| 4  | Service Desk Role Verification | `scripts/4-service-desk-role-check.js` |

## Installation

1. Clone this repo:  
   ```bash
   git clone https://github.com/your-org/servicenow-onload-alerts.git
   ```
2. In ServiceNow, create four new Client Scripts (Type = onLoad) and paste the corresponding code from the `scripts/` folder.

## Usage

- **onLoad** – each script runs when the form loads.
- No additional libraries required—these use native `alert()` and `g_form` / `g_user` APIs.
```

---

### .gitignore  
```gitignore
metadata.xml
*.log
```

---

### scripts/1-alert-priority1-incident.js  
```javascript
// File: scripts/1-alert-priority1-incident.js
(function onLoad() {
  alert("High Priority Incident. Please handle carefully!");
})();
```

---

### scripts/2-validate-short-description.js  
```javascript
// File: scripts/2-validate-short-description.js
(function onLoad() {
  if (!g_form.getValue('short_description')) {
    alert("Please provide a Short Description.");
  }
})();
```

---

### scripts/3-problem-record-notification.js  
```javascript
// File: scripts/3-problem-record-notification.js
(function onLoad() {
  if (g_form.getTableName() === 'problem') {
    alert("Problem Ticket - Perform Root Cause Analysis.");
  }
})();
```

---

### scripts/4-service-desk-role-check.js  
```javascript
// File: scripts/4-service-desk-role-check.js
(function onLoad() {
  if (g_user.hasRole('service_desk')) {
    alert("You have Service Desk access.");
  } else {
    alert("You may not have all permissions.");
  }
})();
```

---
