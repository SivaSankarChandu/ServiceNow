# Business Rules in ServiceNow

Business Rules in ServiceNow are server-side scripts that execute when records are inserted, updated, deleted, or queried. These rules help automate processes, enforce data integrity, and trigger backend logic during database operations.

---

## What is a Business Rule?

A **Business Rule** is a server-side logic that runs automatically based on specific conditions in a record's lifecycle.

### Key Uses:
- Automating field updates or record changes
- Enforcing data validation
- Calling Script Includes or background scripts
- Ensuring consistent workflows

---

## Types of Business Rules

1. **Display**  
   - Executes before the form is presented to the user  
   - Often used to pass data from the server to the client

2. **Before**  
   - Executes before the record is saved to the database  
   - Common for validation or modifying values before insert/update

3. **After**  
   - Executes after the record is saved  
   - Useful for triggering events like sending notifications or logging

4. **Async**  
   - Runs in the background after the record is saved  
   - Best for long-running tasks like integrations or logging

---

## Best Practices

- Keep logic modular using **Script Includes**
- Use `gs.log()` or `gs.debug()` for debugging
- Ensure performance by avoiding unnecessary queries
- Test in sub-production before deploying

---

## Example Use Cases

- Set default priority based on impact and urgency
- Auto-assign tasks to specific groups
- Send notifications after a record update

---

## When **Not** to Use Business Rules

- For UI-specific logic → Use **Client Scripts**
- For repeated scheduling → Use **Scheduled Jobs**

---

## Summary

Business Rules are the backbone of automation in ServiceNow, enabling powerful backend logic without requiring manual intervention. Knowing when and how to use each type is crucial for building scalable and efficient apps.
