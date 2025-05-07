# 🛠️ Fix Scripts in ServiceNow

## 📌 Overview
A **Fix Script** is a type of server-side script in ServiceNow used for one-time execution—typically to fix data or apply post-deployment changes.

---

## ✅ Key Use Cases
- Correcting data inconsistencies
- Mass updates after new field deployment
- Data migration logic during releases

---

## ⚙️ Characteristics
- Server-side only
- Executed manually or during updates
- Part of an Update Set
- Not meant for repeat usage

---

## ⚠️ When *Not* to Use
- Ongoing logic → use Business Rules  
- Timed execution → use Scheduled Jobs  
- Form validation → use Client Scripts

---

## 💡 Best Practices
- **Always test in lower environments**
- **Add logs to track behavior**
- **Document changes properly**
- **Run with caution in production**

---

## 🔗 Related Server-Side Tools
- [Business Rules](#)
- [Scheduled Jobs](#)
- [Script Includes](#)

---

📅 _Next: Business Rules - Driving Automation in Forms!_

