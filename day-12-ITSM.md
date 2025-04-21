# 🧰 ITSM for Beginners – Illustrated Walkthrough

Welcome! This project uses a **comic-style visual** to explain IT Service Management (ITSM) in the simplest way possible. Perfect for newcomers, trainees, and non-technical stakeholders.

---

## 🎨 Visual Breakdown (3-Panel Summary)

**1. Request** – User reports: *"My laptop crashed!"*  
**2. Process** – IT logs, prioritizes, and investigates via ServiceNow  
**3. Outcome** – Resolution delivered: *"Fixed in 2 hours!"* ✅

---

## 🧠 Key Concepts Simplified

| Term      | Meaning                        | Analogy                      |
|-----------|--------------------------------|------------------------------|
| Incident  | IT emergency                   | Like calling 911 🚨          |
| Problem   | Root cause investigation       | Playing IT detective 🔍      |
| Change    | Scheduled upgrade/improvement  | Planned menu update 📅       |

---

## 📌 Use Case

This visual is ideal for:
- Onboarding IT support staff  
- Training sessions on ITIL & ServiceNow  
- Explaining ITSM to business units  
- Simplifying workflows for documentation or presentations  

---

## 📊 Mermaid Diagram – Basic ITSM Use Case Flow

```
flowchart TD
    A[User Reports Issue] --> B[Incident Created in ServiceNow]
    B --> C[IT Assesses & Prioritizes]
    C --> D[Assigned to Technician]
    D --> E[Issue Resolved]
    E --> F[User Informed + SLA Met ✅]
