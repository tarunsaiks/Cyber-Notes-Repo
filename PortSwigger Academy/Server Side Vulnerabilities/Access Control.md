Access control is the application of constraints on who or what is authorized to perform actions or access the resources.

In webapps, this access control is dependent on authentication and session management.

**Authentication** confirms that the user is who they claim to be.
**Session Management** establishes a session and subsequent HTTP requests that are made by the same user.
Access Controls determine if the access is allowed to access or perform operations/actions on the one's they are trying to perform.
## Broken Access Control
#access-controls #owasp #owasp-top-10

- Broken access control is the #1 security concern according to OWASP in 2021, moving from its #5 spot in 2017.
- There are several types of broken access control vulnerabilities, including inadequate access control, inconsistent access control, bypassing access control, insufficient authorization, and lack of access control management.
- Examples of attacks include **SQL injection**, **session fixation**, cross-site request forgery (**CSRF**), **privilege escalation**, and **path traversal**.

Broken Access control is the vulnerability in the access control system that allows unauthorized access to sensitive data or resources.

![]([https://portswigger.net/web-security/images/access-control.svg])

## Vertical Privilege Escalation
