# support-examples
#sql-production

# SQL Production Support Examples

This repository contains SQL queries used in production support troubleshooting.

## Example 1: Find Failed Login Attempts

SELECT *
FROM login_logs
WHERE status = 'failed';

Purpose:
Identify users experiencing login failures.

---

## Example 2: Find Duplicate Users

SELECT email, COUNT(*)
FROM users
GROUP BY email
HAVING COUNT(*) > 1;

Purpose:
Detect duplicate accounts causing authentication issues.

---

## Example 3: Validate User Access

SELECT *
FROM users
WHERE email = 'user@email.com';

Purpose:
Verify user exists and has correct access.

---

Author:
Nava Nasseh
Production Support Analyst

