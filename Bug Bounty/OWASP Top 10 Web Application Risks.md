# Broken Access Control 

## Access Control

Access Control enforces policies such that users cannot act outside their intended permissions. The differences between separate flaws really come down to the different ways in which this core defect is manifested and the different techniques you need to employ to detect it. They are vertical access control, horizontal access control, and context-dependent.

## Broken?

There are three main types of attacks against access controls, corresponding to the three categories of controls:

+ **Vertical privilege escalation** occurs when a user can perform functions that his assgined roles do not permit him to. Like a normal end user can perform adminstrative functions or below his user roles functions.
	+ A simple example would be that of student, teacher and principal. Teacher can mark student's attendance and Principal can mark teacher's attendance. If a student can mark teacher's or his/her own attendance, then its vertical privilege escalation.
+ **Horizontal privilege escalation** occurs when a user can view, modify resources to which he is not entitled. 
	+ `https://www.example.com/login/tarun` is a legit user's dashboard, if Tarun can get access to sai's dashboard `https://www.example.com/login/sai` and can modify data which is entitled to sai alone, then its is horizontal privilege escalation.
+ **Business logic exploitation** occurs when a user can exploit a flaw in application's state machine to gain access to a key resource.

-------------------------
According to OWASP blog, Common access control vulnerabilities include:

-   Violation of the principle of least privilege or deny by default, where access should only be granted for particular capabilities, roles, or users, but is available to anyone.1
-   Bypassing access control checks by modifying the URL (parameter tampering or force browsing), internal application state, or the HTML page, or by using an attack tool modifying API requests.  
-   Permitting viewing or editing someone else's account, by providing its unique identifier (insecure direct object references) #IDOR
-   Accessing API with missing access controls for POST, PUT and DELETE.
-   Elevation of privilege. Acting as a user without being logged in or acting as an admin when logged in as a user.
-   Metadata manipulation, such as replaying or tampering with a JSON Web Token (JWT) access control token, or a cookie or hidden field manipulated to elevate privileges or abusing JWT invalidation.
-   CORS misconfiguration allows API access from unauthorized/untrusted origins.
-   Force browsing to authenticated pages as an unauthenticated user or to privileged pages as a standard user.