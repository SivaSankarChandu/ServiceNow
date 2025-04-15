# Day 6: Understanding Coalesce in ServiceNow

## What is Coalescing?

Coalescing is the process of selecting one or more fields as a unique key when importing data into ServiceNow using Import Sets. 

This tells ServiceNow whether to:
- **Update** an existing record (if the key matches an existing value)
- **Insert** a new record (if no match is found)

## Why is Coalesce Important?

Without coalescing, each import may create duplicate records. With coalescing, ServiceNow updates the correct existing record, maintaining data integrity.

## Example:

| Record ID | Action  | Email                  |
|-----------|---------|------------------------|
| 001       | Update  | john@example.com       |
| 001       | →       | john.smith@example.com |

- With coalesce: Record is updated based on the matching email.
- Without coalesce: A new duplicate record is created.

## Key Use Cases
- Importing Users
- Updating CI data
- Syncing external databases with ServiceNow

---

📌 Ensure you always test coalesce settings in a sub-production instance to avoid accidental data overwrite.
