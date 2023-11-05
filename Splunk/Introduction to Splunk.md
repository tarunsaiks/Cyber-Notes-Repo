# Machine Data

Machine data is everywhere flowing between devices ranging from physical devices to complex servers. This data is accumulated and stored by organizations in various formats.

Some of this data is structured and some of it not. It does not make any sense to see this data in its  raw format.

# Operational Intelligence

Lets take a scenario in a gaming company where a customer calls in to report an issue with payment.

1. The support console shows that everything is working correctly, It will be escalated to **Application Support**.
2. Application support team checks in all monitoring tools to look for issues. If not found, then it will be escalated to **Developer**.
3. Developer runs a test on code and looks for issues. If no issues are found, then it will be escalated to **System Administrator**.
4. System Admin if cannot resolve the issue, then it will be escalated to Database Administrator.

This whole process is very time-consuming and puts a lot of load on single person working on the issue at any given time.

Instead, using Operational Intelligence solves this issue in less time.

## Course Goals

Exploring Splunk, web, running searches and Using commands to create reports and dashboards.

## Process Flow

- Consider a gaming company, which has multiple vendors and online site where their games are being sold. And the company has its own website activity, internal teams, support, orders, from different parts of the world.
- Earlier, when a customer reached out to support, that issue is given a ticket, assigned to someone, and only one person could work on it manually, dropping everything else they were doing. This caused problem both at support and to customers costing time and resources.
- Splunk supports by using all the data in env, to support. When support req comes in, it automatically  routes to application support portal, where support team searches the data for events, where purchase attempts lead to error, using which he can pinpoint if the event matches the user's experience.
- That event is tied to a database query, which can be correlated to an entry in the slow query log