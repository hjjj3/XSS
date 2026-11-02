# Module 00 - Exercise 00: Cross-Site Scripting (XSS)

## What is OWASP?
OWASP stands for Open Worldwide Application Security Project. It is a nonprofit foundation dedicated to improving software security. It is widely recognized for the "OWASP Top 10", a document highlighting the most critical security vulnerabilities affecting web applications.

## What is XSS (Cross-Site Scripting)?
Cross-Site Scripting (XSS) is a security vulnerability that allows attackers to inject malicious JavaScript (or other client-side scripts) into web pages viewed by other users. This happens when an application includes untrusted user input without proper validation or output encoding.

## Exploitation Scenarios
1. **Scenario 1 (Reflected XSS):** An attacker crafts a malicious URL containing a JavaScript payload and sends it to a victim. When the victim clicks the link, the server reflects the input in the HTTP response without sanitization, executing the script in the victim's browser to steal session tokens.
2. **Scenario 2 (Stored XSS):** A user submits a comment or profile update containing malicious JavaScript. The server stores this payload permanently in the database. Whenever another user or administrator views the page, the script executes automatically in their browser.
