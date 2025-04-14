# ServiceNow ITSM Module

## 🧩 What is ITSM?

**ITSM (IT Service Management)** refers to the way organizations design, deliver, manage, and improve the IT services they provide to end users.  
ServiceNow provides a powerful ITSM module that automates and standardizes service delivery using a wide set of applications.

---

## 🚀 Core ITSM Applications in ServiceNow

### 1. 🛠️ Incident Management
- Tracks and resolves unplanned disruptions to services
- Helps restore normal operations as quickly as possible

### 2. 🔁 Problem Management
- Identifies and manages the root cause of recurring incidents
- Prevents future disruptions

### 3. 📦 Change Management
- Ensures standardized methods for managing change to minimize impact
- Tracks risk, approvals, and schedules

### 4. 🧾 Request Management
- Allows users to request goods and services via a service catalog
- Automates approvals and fulfillment workflows

### 5. 🧠 Knowledge Management
- Centralized repository for FAQs, solutions, and documentation
- Promotes self-service and reduces incident volume

---

## 🧠 Benefits of ITSM on ServiceNow

- Centralized platform for service delivery
- Workflow automation with approvals and escalations
- Real-time reporting and dashboards
- Enhanced user experience via self-service portal

---

## 🖥️ Tables Commonly Used

| Module             | Table Name         |
|--------------------|--------------------|
| Incident           | `incident`         |
| Problem            | `problem`          |
| Change Request     | `change_request`   |
| Request            | `sc_request`       |
| Requested Item     | `sc_req_item`      |
| Knowledge Base     | `kb_knowledge`     |

---

## 🧪 Use Case Example

> A user raises an incident through the portal.  
> The incident is assigned to a technician via auto-assignment rules.  
> If repeated incidents occur, a Problem is created to investigate the root cause.  
> A Change Request may follow to permanently resolve the issue.
