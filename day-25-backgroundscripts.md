# 🔍 ServiceNow Scripting – Background Scripts


## 📘 What are Background Scripts?


Background Scripts are powerful tools in the ServiceNow platform used to execute server-side JavaScript directly against the ServiceNow database.


You can use them for:

- Bulk updating records

- Running one-time database fixes

- Validating business logic via GlideRecord

- Testing server-side APIs



> 📍 Navigation: System Definition → Scripts - Background



---



## 🧠 Sample Use Case


### Scenario:

Update all **Incident** records in "New" state that were created over 7 days ago, and move them to "In Progress".



### Script:



```javascript

var gr = new GlideRecord('incident');

gr.addQuery('state', 1); // New

gr.addQuery('sys_created_on', '<javascript:gs.daysAgoStart(7)');

gr.query();

while (gr.next()) {

  gr.state = 2; // In Progress

  gr.update();

}

⚠️ Caution

Background Scripts can change live production data. It’s strongly advised to:

Test your scripts in a development or test environment

Use conditions (addQuery) to filter precisely

Use gs.log() for debugging instead of mass updates

✅ Best Practices

Always preview the impact

Comment your scripts clearly

Avoid using in production unless absolutely necessary

📌 Next in the Series: Fix Scripts

 Trackable, version-controlled server-side scripts to fix data issues in a more controlled way.
