## 🚒 Incident vs. Problem vs. Change – Explained Like a Fire Department

A fun and effective analogy to explain ITSM concepts using real-world firefighting roles.  
Perfect for **ServiceNow trainers**, **ITIL educators**, and **tech professionals** who want to make complex concepts **clear and memorable**.

---

### 📌 Use Case

> **As a** ServiceNow or ITSM educator  
> **I want** to explain the differences between Incident, Problem, and Change Management using simple analogies  
> **So that** beginners quickly grasp the roles and flow of ITSM processes

---

### 📘 What’s Inside

#### 🔥 Incident Management ➜ **Firefighters**
- 🚒 A fire breaks out (a server is down!)
- Goal: Restore service *immediately* (a workaround is fine)
- Focus: **Minimize impact fast**

#### 🕵️ Problem Management ➜ **Detective**
- 🔍 Find out *why* the fire happened (root cause = faulty wiring)
- Goal: Prevent recurrence by solving the underlying issue
- Focus: **Cause analysis & prevention**

#### 🏗️ Change Management ➜ **Construction Crew**
- 👷 Implement a proper fix (upgrade faulty wiring)
- Goal: Deploy a safe, controlled solution
- Focus: **Planned improvement**

#### 🔄 Flow  
Incident ➜ Problem ➜ Change  
Symptom ➜ Cause ➜ Cure

---

### 🧩 Use Case Diagram

```plaintext
+-----------------+
|     End User    |
+-----------------+
         |
         v
  +-------------------+        ➜ Fire starts
  | Incident (INC)    |--------+
  | "Fix ASAP"        |         \
  +-------------------+          \
         |                         ➜ ➜ Temporary fix / work-around
         v
  +-------------------+        ➜ Find the root cause
  | Problem (PRB)     |--------+
  | "Why it happened" |         \
  +-------------------+          \
         |                         ➜ ➜ RCA documented
         v
  +-------------------+        ➜ Permanent resolution
  | Change (CHG)      |--------+
  | "Plan & Deploy"   |         \
  +-------------------+          ➜ Controlled fix with approvals
```

---

