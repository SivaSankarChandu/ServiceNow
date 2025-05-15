# Flow Designer: Trigger Types in ServiceNow

Flow Designer in ServiceNow allows users to automate processes with minimal coding.  
Triggers are essential components—they define **when** a flow should start.

---

## 🔹 Trigger Types

### 1. 🗂️ Record Trigger
- **Fires when**: A record is created, updated, or deleted.
- **Use Case**: Automatically assign an agent when an incident is created.

### 2. ⏰ Schedule Trigger
- **Fires when**: A specific time or recurring schedule is met.
- **Use Case**: Send daily reminders or generate weekly reports.

### 3. 🔧 Application Trigger
- **Fires when**: A specific ServiceNow application initiates an action.
- **Use Case**: Launch flows based on application-specific events.

### 4. 🌐 REST Trigger
- **Fires when**: A REST API call is made to ServiceNow.
- **Use Case**: External systems triggering ServiceNow processes (e.g., integration from third-party tools).

---

## ✅ Best Practices

- Use **conditions** with triggers to fine-tune when the flow executes.
- Combine **subflows** to modularize logic.
- Always test trigger conditions thoroughly to avoid unnecessary executions.

---

## Related Topics

- [Subflows in Flow Designer](#)
- [Best Practices for Flow Building](#)
- [Calling REST APIs from ServiceNow](#)

---

> **Note:** Triggers determine when your automation starts. Choosing the right type ensures your workflows run exactly when needed.
