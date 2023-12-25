Splunk search language is built by 5 components

- Search Terms - Foundations of Search Queries
- Commands - Tells what we want to do with those search results (creating charts, computing statistics and formatting)
- Functions - Explain how we want to chart, compute and evaluate the results.
- Arguments - Variables we apply to the function (product_name)
- Clauses - Explains how we want results grouped or defined.

### Splunk Search Language Example

```SQL
index=network sourcetype=cisco_wsa_squid usage=Violation | stats count(usage) as Visits
```

index=network sourcetype=cisco_wsa_squid usage=Violation ->Search Terms

stats count(usage) as Visits -> search components

stats - command

count() - function

usage - argument

as - clause

| - Pipe

![Splunk Search Language Example](Splunk_search_language_example.png)


Using Network index data from cisco_web_security_application data where it is counting number of users that were prohibited access using keyword Violation. This data is stored in a field called Visits.

search command can be used at any time of search pipeline to further search in the results.

![](search_pipeline_search.png)