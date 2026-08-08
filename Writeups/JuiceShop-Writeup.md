## 1. SQL Injection (Authentication Bypass)
*   **Target:** OWASP Juice Shop Login Page
*   **Payload Used:** `' OR 1=1 --`
*   **Impact:** Exploited a flaw in the backend database query logic, allowing full access to the administrator account without credential verification.
*   **Remediation:** Implement parameterized queries on the backend to strictly separate user input from executable SQL commands.
