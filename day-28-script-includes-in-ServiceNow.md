# ♻️ Script Includes in ServiceNow

**Write Once, Reuse Everywhere!**  
Script Includes allow you to define reusable server-side functions in one place and call them across multiple parts of your ServiceNow instance.

---

## 🔍 What is a Script Include?

A **Script Include** is a server-side script in ServiceNow used to:

- Store reusable logic
- Be referenced across:
  - Business Rules
  - Scripted REST APIs
  - Workflows
  - UI Actions
  - Scheduled Jobs

---

## 🧩 Types of Script Includes

- ✅ **Global** – Accessible from any scope
- ✅ **Non-global** – Accessible only within its application scope
- ✅ **Client-callable** – Can be invoked from client-side scripts using `GlideAjax`

---

## ✅ Benefits of Using Script Includes

- Eliminate repeated logic across scripts
- Improve maintainability and readability
- Promote modular and testable code
- Enable client-server interaction via GlideAjax

---

## 🧠 Common Use Cases

- Reusable utility or helper functions
- Backend logic for Scripted REST APIs
- Calculations or processing logic used in multiple scripts
- Server logic invoked by Client Scripts

---

## 🚫 When *Not* to Use Script Includes

- For UI-only logic — use **Client Scripts** or **UI Policies**
- For simple one-off logic that doesn’t require reuse

---

## ⚙️ Best Practices

- Follow consistent naming conventions
- Keep your functions modular and focused
- Document every function and its purpose
- Use `gs.info()` for logging and debugging
- Always test in a sub-production environment

---

## 📌 Notes

Script Includes are one of the most powerful tools in ServiceNow for maintaining scalable, reusable server-side logic — essential for any ServiceNow Developer!

---

### 🔜 Coming Next:  
**Scripted REST APIs – Build Custom Endpoints like a Pro!**
