# 🛠️ Real-Time Incident Creation with Jira + ServiceNow Integration

This project demonstrates how Jira and ServiceNow can be integrated to automate incident management workflows in real-time.

## 🔄 Overview

The integration ensures that any **bug ticket logged in Jira** is automatically converted into an **incident in ServiceNow**, and any updates made in ServiceNow are synchronized back to Jira, enabling end-to-end visibility and traceability.

---

## ✅ Workflow Steps

### 1. Bug Ticket Logged in Jira
- **Trigger**: A user creates a bug ticket in Jira  
- **Sample Data**:  
  - Priority: High  
  - Description: Application crash on login

### 2. Automatic Incident Creation in ServiceNow
- **Automation**: A ServiceNow incident is created using mapped fields  
- **Mapped Fields**:  
  - Priority  
  - Description

### 3. Sync Back to Jira
- **Bi-directional Sync**: Updates in ServiceNow sync back to Jira  
- **Benefit**: Ensures both Dev and IT teams are aligned

---

## 🧩 Tools & Technologies

- **Jira** – Bug/Issue Tracking
- **ServiceNow** – ITSM Platform
- **Webhook / REST API** – For Integration
- **Middleware (Optional)** – IntegrationHub, Zapier, or Custom Scripts

---

## 🚀 Benefits

- Eliminates manual coordination
- Accelerates incident resolution
- Enables visibility across platforms
- Strengthens DevOps collaboration

---

## 📊 Use Cases

- DevOps teams managing frequent releases
- ITSM operations handling large-scale incident volumes
- Enterprises using Jira (Dev) + ServiceNow (Support)
