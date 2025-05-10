# Scripted REST APIs in ServiceNow

**Scripted REST APIs** in ServiceNow provide developers with the flexibility to build custom RESTful web services that interact with external systems or expose internal data in a controlled and secure manner.

---

## 🔍 What is a Scripted REST API?

A Scripted REST API is a server-side integration point that allows you to:

- Create custom endpoints in ServiceNow
- Define how requests are handled and responses are returned
- Enable external applications to communicate with your instance

---

## ⚙️ Key Components

- **API Name & Version** – Logical grouping and versioning of your APIs
- **Resources** – Endpoints that represent specific actions (e.g., `/getIncidents`)
- **HTTP Methods** – Supported methods like `GET`, `POST`, `PUT`, `DELETE`
- **Script Logic** – Code that processes incoming requests and returns structured responses

---

## ✅ Why Use Scripted REST APIs?

- Customization beyond OOTB capabilities
- Full control over business logic and data manipulation
- Securely expose ServiceNow data to external platforms
- Role-based access control and OAuth integration

---

## 🧠 Common Use Cases

- Expose incident or catalog data to third-party applications
- Enable integrations with platforms like Jira, Slack, or custom web apps
- Mobile app communication with ServiceNow
- Automate external form submissions into ServiceNow tables

---

## 🚫 When Not to Use

- If no external communication is required → Use **Script Includes**, **Business Rules**
- If IntegrationHub or an existing Spoke meets the requirements

---

## 📌 Best Practices

- Validate and sanitize all user input
- Use `GlideRecord` carefully to avoid performance degradation
- Wrap logic in try-catch blocks for robust error handling
- Use `gs.info()` for logging during development
- Document each endpoint clearly for consumers

---

## 📚 References

- [ServiceNow Docs – Scripted REST APIs](https://developer.servicenow.com/dev.do#!/reference/api/orlando/server_apis/ScriptedRESTAPI/concept/c_ScriptedRESTAPI)
- [GlideRecord API Reference](https://developer.servicenow.com/dev.do#!/reference/api/orlando/server_apis/GlideRecord)

---
