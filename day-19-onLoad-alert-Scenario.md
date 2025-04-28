# 🚨 ServiceNow onLoad Alert Scripts

This repository demonstrates four self-invoking **onLoad** Client Scripts in ServiceNow. Each script fires automatically when a form loads, providing timely alerts to guide users, improve data quality, and enforce process rules.

---

## 📌 Overview

| Script                                    | Trigger                | Purpose                                                      |
|-------------------------------------------|------------------------|--------------------------------------------------------------|
| **Priority 1 Incident Alert**             | onLoad (all forms)     | Warn users when viewing/editing a P1 Incident                |
| **Short Description Validation**          | onLoad (Incident form) | Prompt if `short_description` is empty                       |
| **Problem RCA Reminder**                  | onLoad (Problem form)  | Remind to perform Root Cause Analysis on Problem records     |
| **Service Desk Role Check**               | onLoad (all forms)     | Confirm or warn based on `service_desk` role membership      |

---

## 🧑‍💻 Code

```javascript
/** 1. Priority 1 Incident Alert */
(function onLoadPriority1() {
  alert("High Priority Incident. Please handle carefully!");
})();

/** 2. Short Description Validation */
(function onLoadValidateShortDesc() {
  if (!g_form.getValue('short_description')) {
    alert("Please provide a Short Description.");
  }
})();

/** 3. Problem RCA Reminder */
(function onLoadProblemRCA() {
  if (g_form.getTableName() === 'problem') {
    alert("Problem Ticket – Perform Root Cause Analysis.");
  }
})();

/** 4. Service Desk Role Check */
(function onLoadRoleCheck() {
  if (g_user.hasRole('service_desk')) {
    alert("You have Service Desk access.");
  } else {
    alert("You may not have all permissions.");
  }
})();
