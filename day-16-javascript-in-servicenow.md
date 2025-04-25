# 🚀 JavaScript in ServiceNow – The Invisible Engine

JavaScript is the powerhouse behind the scenes in ServiceNow. From building responsive forms to integrating with external systems, it enables developers and admins to automate, customize, and streamline business processes on the Now Platform.

## 🔍 Overview

This repository illustrates how JavaScript is used across different layers of ServiceNow:

- **Frontend** – Client-side interactivity using Client Scripts and UI Policies
- **Backend** – Server-side logic via Business Rules and Script Includes
- **Automation & Integration** – Extending platform capabilities through GlideSystem, Workflows, and REST APIs

---

## 🧩 Use Case Diagram (Text Representation)

```plaintext
                 ┌────────────────────────────┐
                 │     JavaScript in SNOW     │
                 └────────────┬───────────────┘
                              │
       ┌──────────────────────┼────────────────────────┐
       ▼                      ▼                        ▼
┌────────────┐       ┌────────────────┐        ┌────────────────────────┐
│ Frontend   │       │ Backend        │        │ Automation & APIs      │
│            │       │                │        │                        │
│ • Client   │       │ • Business     │        │ • GlideSystem          │
│   Scripts  │       │   Rules        │        │ • Workflows            │
│ • UI       │       │ • Script       │        │ • REST/SOAP APIs       │
│   Policies │       │   Includes     │        │                        │
└────────────┘       └────────────────┘        └────────────────────────┘

📌 Code Snippets
Frontend (Client Script)

g_form.setReadOnly('field_name', true); // Disables the field on form

Backend (Business Rule)

if (current.priority == 1) {
  current.assignment_group = 'Critical Team';
}

Automation (REST API)
GET /api/now/table/incident
