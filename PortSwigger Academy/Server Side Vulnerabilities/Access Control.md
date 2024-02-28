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

https://portswigger.net/web-security/images/access-control.svg

## Vertical Privilege Escalation
#vertical-previlege-escalation #previlege-escalation

If a user can gain access to functionality that they are not permitted to access then this is vertical privilege escalation. For example, if a non-administrative user can gain access to an admin page where they can delete user accounts, then this is vertical privilege escalation.

### Unprotected Functionality

Vertical prev-esc arises when an app does not enforce any protection for sensitive functionality.

a user might be able to access the administrative functions by browsing to the relevant admin URL.0For example, a website might host sensitive functionality at the following URL:

`https://insecure-website.com/admin`

This might be accessible by any user, not only administrative users who have a link to the functionality in their user interface. In some cases, the administrative URL might be disclosed in other locations, such as the `robots.txt` file:

`https://insecure-website.com/robots.txt`

Even if the URL isn't disclosed anywhere, an attacker may be able to use a wordlist to brute-force the location of the sensitive functionality.

> Lab Unprotected admin functionality SOLVED

**Security By Obscurity** is when a sensitive functionality is given a less predictable URL