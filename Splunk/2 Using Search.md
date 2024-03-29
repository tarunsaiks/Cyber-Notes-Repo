
#splunk #searchandreporting #splunkapps #splunk_search 
In Search and Reporting app, Add the appropriate term on which we need to search and select time range and get the results.

>[!tip]
>Limiting a search by time is a key to faster results and it is a best practice.

The search is sent to Splunk where it becomes a Splunk Job, New Search page opens, which can be saved as Knowledge object and few actions can be performed along with timeline.

- Save As - Allows to save as Knowledge objects
- Search Result Tab (Events, Patterns, Statistics, Visualisation)
- Search Action buttons (Pause, Stop, Share, Print and Export)
- Search mode selector
- Timeline

If searches creates any  statistics or patterns, it will be available in respective tabs, if not it will show links to pivot, link to generate quick reports and search commands.

#splunk_search #splunk_transforming_commands

>[!Note]
> Commands that create statistics and visualizations are called ==Transforming Commands==. These are the commands that transform event data into data tables.

>[!Note]
>By default, a search job will remain active for 10 minutes after that, splunk will need to run that job again to fetch results. However, shared search job remains active for 7 days.
>

### Search Action Buttons
- Pause
- Stop
- Share - To other users in the organization, where they can see exact results when you run the search, 
- Print 
- Export - Raw, CSV, XML and JSON formats supported
### Search mode Selector
Fast, Smart and Verbose mode.

Fast - Field Discovery disabled - Cuts down Field Information
Verbose - All the fields data and verbose.

## Exploring Events and Search Terms

Events are returned in a reverse chronological list (newest items first)

Wildcards can be used to match terms better using `*`

Search terms are not case sensitive.

Uppercase Booleans of AND, OR, NOT can be used.

Boolean Order of operations are
1. NOT
2. OR
3. AND
Parenthesis can be used to prioritize it first.

Exact terms can be searched by placing them in quotes `"login" "failed"`

Escape characters can be used in a search using `\`

```
info="user \"ChrisV4\" not in database"
```
