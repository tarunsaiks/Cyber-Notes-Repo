SQLi - Attackers interfere with queries to view data that they are normally able to retrieve. 

In some cases, an attacker can modify, delete data causing persistent changes to application's functionality and disrupting data integrity.


## How to detect SQL Injection vulnerabilities??

Testing must be done against every possible entry point in the application by submitting

- The single quote character `'` and look for errors or other anomalies.
- Some SQL-specific syntax that evaluates to the base (original) value of the entry point, and to a different value, and look for systematic differences in the application responses.
- Boolean conditions such as `OR 1=1` and `OR 1=2`, and look for differences in the application's responses.
- Payloads designed to trigger time delays when executed within a SQL query, and look for differences in the time taken to respond.

**Out-of-band application security testing (OAST)** is a process that can be used to identify and exploit vulnerabilities in web applications and APIs. OAST is typically performed by identifying and exploiting vulnerabilities in the communication channel between the web application and its backend systems.

OAST can be used to identify vulnerabilities that are not detectable using traditional penetration testing techniques. These include things like **blind SQL injection (SQLi), blind cross-site scripting (XSS), and blind command injection vulnerabilities**.

- OAST (Out of band application security testing) payloads designed to trigger an out-of-band network interaction when executed within a SQL query, and monitor any resulting interactions.

## SQL injection in different parts of the query

Most SQL Injection vulns occur within WHERE clause of a SELECT query. But can also occur within different query types.

- In `UPDATE` statements, within the updated values or the `WHERE` clause.
- In `INSERT` statements, within the inserted values.
- In `SELECT` statements, within the table or column name.
- In `SELECT` statements, within the `ORDER BY` clause.