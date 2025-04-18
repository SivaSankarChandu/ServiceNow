# 🚀 ServiceNow Update Sets Guide

This repository provides a comprehensive guide and example assets for working with **Update Sets** in ServiceNow. Update Sets are essential tools for capturing and promoting configuration changes across environments (Dev → Test → Prod) in a secure, controlled manner.

---

## 📘 What Are Update Sets?

An **Update Set** is a collection of configuration changes made in a ServiceNow instance. These changes can be exported and imported into another instance, enabling a streamlined DevOps lifecycle within the ServiceNow platform.

Update Sets allow developers and administrators to:

- Track and package configuration changes
- Migrate updates between instances
- Support collaboration and team development
- Enable version control and rollback (to a degree)

> ⚠️ Update Sets only track configuration changes — **not data**, such as records or CMDB entries.

---

## 🧠 Why Use Update Sets?

Using Update Sets ensures a reliable and repeatable process for:
- Migrating customizations from **Development → Testing → Production**
- Avoiding manual rework or reconfiguration
- Auditing changes made during development
- Collaborating with multiple developers on a single release cycle

---

## 📦 Common Items Tracked in Update Sets

| Change Type       | Tracked? | Notes |
|-------------------|----------|-------|
| Business Rules     | ✅        | Full logic tracked |
| Script Includes    | ✅        | Reusable backend scripts |
| UI Policies        | ✅        | Client-side form logic |
| Client Scripts     | ✅        | Browser-based logic |
| Workflows          | ✅        | Workflow editor changes |
| Form Layouts       | ✅        | Fields and sections |
| ACLs               | ⚠️ Partial | Requires manual review |
| Data Records       | ❌        | Not tracked — use import sets or scripts |
| Dictionary Entries | ✅        | Tracked when manually modified |

---

## 🔄 Dev to Prod Lifecycle Diagram (Mermaid)

```mermaid
flowchart LR
    DEV[Development Instance]
    TEST[Test / QA]
    PROD[Production Instance]
    EXPORT[Export Update Set]
    IMPORT[Import Update Set]

    DEV -->|Capture Config Changes| EXPORT
    EXPORT -->|XML File| IMPORT
    IMPORT -->|Validate + Test| TEST
    TEST -->|Approved Changes| PROD
