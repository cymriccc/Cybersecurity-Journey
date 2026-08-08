## 1. SQL Injection (Authentication Bypass)
*   **Target:** OWASP Juice Shop Login Page
*   **Payload Used:** `' OR 1=1 --`
*   **Impact:** Exploited a flaw in the backend database query logic, allowing full access to the administrator account without credential verification.
*   **Remediation:** Implement parameterized queries on the backend to strictly separate user input from executable SQL commands.

## 2. DOM-Based Cross-Site Scripting (XSS)
*   **Target:** OWASP Juice Shop Search Bar
*   **Payload Used:** `<iframe src="javascript:alert('xss')">`
*   **Impact:** Exploited a lack of input sanitization on the client-side search routing. An attacker could use this to execute malicious scripts in a victim's browser, potentially stealing session tokens or hijacking accounts.
*   **Remediation:** Strictly sanitize and encode all user-supplied data before rendering it in the DOM. Avoid rendering raw HTML directly from user input.
