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
## Broken Access Control

In simple words,  only the site's admin user should be able to access a page to manage other users. If a website visitor can access protected pages they are not meant to see, then the access controls are broken.

A regular visitor being able to access protected pages can lead to the following:

- Being able to view sensitive information from other users
- Accessing unauthorized functionality

Simply put, broken access control allows attackers to bypass **authorization**, allowing them to view sensitive data or perform tasks they aren't supposed to.