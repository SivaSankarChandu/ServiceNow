# Actions in Flow Designer – ServiceNow

In **ServiceNow Flow Designer**, **Actions** are the building blocks that execute logic and interact with records or systems. These actions help automate business processes with ease, speed, and consistency.

---

## 📌 What are Actions?

Actions are predefined or custom tasks performed during a flow execution. They are reusable and modular, helping streamline logic and reduce complexity.

---

## 🔹 Types of Actions

### 🔄 Core Actions
Basic flow logic tools built into ServiceNow, such as:
- Log
- Set Values
- If/Else
- Loop

### 🌐 ServiceNow Actions
Direct interactions with ServiceNow records:
- Create Record
- Update Record
- Delete Record

### 🛠️ Custom Actions
Reusable and organization-specific actions built to serve custom logic.

### 📤 Spoke Actions
IntegrationHub actions used to communicate with external systems like:
- Slack
- Microsoft Teams
- Jira
- Zoom

---

## 🚀 Key Benefits

- **Low-Code**: Easy to configure, even for non-developers.
- **Reusable**: Custom and spoke actions can be reused across multiple flows.
- **Integration-Ready**: Extend workflows beyond ServiceNow using IntegrationHub.
- **Efficient**: Save time and reduce manual effort in workflow design.

---

## ✅ Example Use Case

**Employee Leave Request Flow:**

| Step | Action Type | Description |
|------|-------------|-------------|
| Validate input | 🔄 Core | Ensure form data is correct |
| Create task | 🌐 ServiceNow | Add a new HR task record |
| Notify manager | 📤 Spoke | Send Teams notification |
| Assign owner | 🛠️ Custom | Use logic to assign task |

---

## 📘 Best Practices

- Keep actions **modular** and **reusable**.
- Use **naming conventions** for clarity.
- Leverage **Spoke Actions** for integration-heavy use cases.
- Debug using **Log** actions in development.

---