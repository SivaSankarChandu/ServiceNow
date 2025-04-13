# Day 4: Users, Groups, and Roles in ServiceNow

## 👤 Users
A user is anyone who can log into the ServiceNow platform.

### Example:
- `sivasankarchandu@gmail.com`

Users are stored in the **sys_user** table.

---

## 👥 Groups
Groups are collections of users who share similar responsibilities.

### Example:
- `Change Management Group`
- `Incident Management Team`

Groups are stored in the **sys_user_group** table.

---

## 🔐 Roles
Roles determine access permissions within ServiceNow.

### Common Roles:
- `admin`: Full access
- `itil`: Standard ITSM access
- `approver_user`: Can approve records

Roles are stored in the **sys_user_role** table.

---

## 🔄 How They Work Together

- Users are added to **Groups**
- Groups are assigned **Roles**
- Users inherit the group's roles automatically

This structure supports RBAC (Role-Based Access Control) for secure and flexible system access.

---

## 📎 Use Case

Example:
- A user in the "Incident Management" group gets the `itil` role.
- They can now view, create, and modify incident records.

---
