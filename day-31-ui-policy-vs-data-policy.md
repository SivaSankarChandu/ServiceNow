# UI Policy vs Data Policy in ServiceNow

Understanding the difference between **UI Policies** and **Data Policies** is crucial for building reliable, user-friendly, and compliant applications on the ServiceNow platform.

---

## ✅ UI Policy

A **UI Policy** is a *client-side* rule used to dynamically control form elements in the browser.

### 🔹 Key Features:
- Runs in the browser (client-side)
- Executes when the user interacts with a form
- Does not impact backend or imported data

### 🔹 Use Cases:
- Make a field **mandatory** when a condition is met
- Hide or show a field based on another field's value
- Make a field read-only

---

## ⚙️ Data Policy

A **Data Policy** is a *server-side* rule used to enforce data integrity at the database level.

### 🔹 Key Features:
- Executes during record **insert or update**
- Applies to:
  - UI forms
  - Data imports
  - Scripted APIs
- Ensures backend data quality regardless of input source

### 🔹 Use Cases:
- Enforce phone number format on all inputs
- Require specific fields during record import
- Prevent invalid data even if entered via API or script

---

## 🔍 Comparison Table

| Feature              | UI Policy             | Data Policy           |
|----------------------|------------------------|------------------------|
| Runs On             | Client-side (Browser) | Server-side (Platform) |
| Applies To          | UI Forms              | UI, APIs, Imports      |
| Purpose             | UX/Behavior Control   | Data Validation        |
| Real-time Response  | ✅ Yes                | ❌ No                  |
| Controlled Elements | Form Fields           | Record Data            |

---

## 💡 Best Practices

- Use **UI Policy** to improve the user experience by guiding users visually.
- Use **Data Policy** to ensure data rules are followed across all entry points.
- Always validate important fields on the server to avoid bypass via scripts or imports.

---

## 📌 Example Scenario

> Make the "Resolution Code" field mandatory **only** when:
> - **UI Policy**: State = Resolved (real-time on the form)
> - **Data Policy**: Ensure it remains mandatory for updates from APIs/imports
