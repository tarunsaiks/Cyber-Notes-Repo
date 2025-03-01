The list of OWASP Top 10 vulnerabilities identified according to 2021.
1. [**A01:2021-Broken Access Control**](https://owasp.org/Top10/A01_2021-Broken_Access_Control/)
2. [**A02:2021-Cryptographic Failures**](https://owasp.org/Top10/A02_2021-Cryptographic_Failures/)
3. [**A03:2021-Injection**](https://owasp.org/Top10/A03_2021-Injection/)
4. [**A04:2021-Insecure Design**](https://owasp.org/Top10/A04_2021-Insecure_Design/)
5. Security Misconfiguration
6. Vulnerable and Outdated Components
7. Identification and Authentication Failures
8. Software and Data Integrity Failures
9. Security Logging & Monitoring Failures
10. Server-Side Request Forgery (SSRF)

![](../Pasted%20image%2020250301130321.png)
# Broken Access Control

In simple words,  only the site's admin user should be able to access a page to manage other users. If a website visitor can access protected pages they are not meant to see, then the access controls are broken.

A regular visitor being able to access protected pages can lead to the following:

- Being able to view sensitive information from other users
- Accessing unauthorized functionality

Simply put, broken access control allows attackers to bypass **authorization**, allowing them to view sensitive data or perform tasks they aren't supposed to.

## OWASP Definition - Broken Access Control

Access control enforces policy such that users cannot act outside of their intended permissions. Failures typically lead to unauthorized information disclosure, modification, or destruction of all data or performing a business function outside the user's limits. Common access control vulnerabilities include:

- Violation of the principle of least privilege or deny by default, where access should only be granted for particular capabilities, roles, or users, but is available to anyone.
- Bypassing access control checks by modifying the URL (parameter tampering or force browsing), internal application state, or the HTML page, or by using an attack tool modifying API requests.
- Permitting viewing or editing someone else's account, by providing its unique identifier (insecure direct object references)
- Accessing API with missing access controls for POST, PUT and DELETE.
- Elevation of privilege. Acting as a user without being logged in or acting as an admin when logged in as a user.
- Metadata manipulation, such as replaying or tampering with a JSON Web Token (JWT) access control token, or a cookie or hidden field manipulated to elevate privileges or abusing JWT invalidation.
- CORS (Cross-Origin Resource Sharing) misconfiguration allows API access from unauthorized/untrusted origins.
- Force browsing to authenticated pages as an unauthenticated user or to privileged pages as a standard user.

## How to Prevent
- Except for public resources, use default DENY ALL.
-  Implement Access control mechanisms once and re-use them throughout the application, including the minimal use of CORS.
- Model access controls should enforce record ownership rather than accepting the user can perform CRUD operations on any record.
- Unique application business limit requirements to be enforced by domain models.
- Disable web server directory listing and ensure file metadata (e.g., .git) and backup files are not present within web roots.
- Log access control failures, alert admins when appropriate (PROJECT IDEA - Write a Python script to check for repeated login failures or access failures within a timeframe say 5 mins.) #project-idea
- Rate-limit API and controller access to minimize the damage.
- Stateful session identifiers should be invalidated on the server after logout. Stateless [JSON Web Token (JWT)](https://www.geeksforgeeks.org/json-web-token-jwt/)should rather be short-lived so that the window of opportunity for an attacker is minimized. For longer lived JWTs it's highly recommended to follow the OAuth standards to revoke access.