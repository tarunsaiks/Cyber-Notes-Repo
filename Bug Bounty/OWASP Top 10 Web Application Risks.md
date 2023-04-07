# Broken Access Control 

## Access Control

Access Control enforces policies such that users cannot act outside their intended permissions. The differences between separate flaws really come down to the different ways in which this core defect is manifested and the different techniques you need to employ to detect it. They are vertical access control, horizontal access control, and context-dependent.

## Broken?

There are three main types of attacks against access controls, corresponding to the three categories of controls:

+ **Vertical privilege escalation** occurs when a user can perform functions that his assgined roles do not permit him to. Like a normal end user can perform adminstrative functions or below his user roles functions.
	+ A simple example would be that of student, teacher and principal. Teacher can mark student's attendance and Principal can mark teacher's attendance. If a student can mark teacher's or his/her own attendance, then its vertical privilege escalation.
+ **Horizontal privilege escalation** occurs when a user can view, modify resources to which he is not entitled. 
	+ `https://www.go`