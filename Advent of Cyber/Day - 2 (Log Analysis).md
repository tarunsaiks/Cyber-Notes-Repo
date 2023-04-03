## What are Log files??

Log files are the files that contain historical record of events and other data from an application. Some common examples that you may find in a log file :

+ Login attempts or failures
+ Traffic on a network
+ Things (website, URL's, files, etc.) that have been accessed.
+ Password changes
+ Application errors (used in debugging)
+ and many many more

Log files are extremely important in finding answers to below question
+ What has happened?
+ When has it happened?
+ Where has it happened?
+ Who did it? Were they successful?

### How does a log file look like??

![[Pasted image 20221206153221.png]]

It usually contains a timestamp of the event, name of the service that is generating the log file and actual event the service logs

`Event Viewer` from windows shows the event logs which are categorized into Application, Security, Setup and System

In Linux (Ubuntu and Debian) has log files located at `/var/log` with categories like
+ Authentication - `auth.log` -  Contains all auth attempts either remote or on the system itself - (Failed password for `root` from `192.168.1.35` port 22)
+ Package Management - `dpkg.log` - Contains events related to packages in system (useful in debugging and reverting changes)
+ Syslog - `syslog` - Contains all events related to things happening in system background like crontabs, services.
+ Kernel - `kern.log` - contains all events related to kernel events like changes to kernel, output from devices such as networking equipment or physical devices such as USB devices.

Log files can quickly contain many events and thousands of entries, The difficulty in analysing log files is seperating useful information from useless. Tools such as Splunk are software solutions known as `Security Information and Event Management (SIEM)` is dedicated to aggregating logs for  analysis.

## Grep 101
