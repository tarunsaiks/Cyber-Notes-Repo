It is combination of Google and Dork, Google = Search Engine; Dork = Special Query which gives specific results.

“Google dorking” (aka “Google hacking”) is the activity of performing advanced searches on Google. You can combine different Google dorks to comb data otherwise inaccessible to ordinary users of Google search.

## Scope Restricting Dorks
| Dork | Description | Example|
|---| --- | --- |
| site: | Restricts search to a particular website, a top level domain or subdomain | site: github.com, site:attack.mitre.org |
| filetype: "filetype", ext: <file_type>  | Restrict the returned web address to designated | filetype:pdf, ext:txt|
| @| Restricts search to a particular social platform like twitter, facebook. Not as precise as site: | @twitter Eathquake news |
|imagesize:(height)x(width) |Restrict image search results to specific dimensions, Like for Desktop wallpapers | imagesize: 1920x1080|
| define: | Return definitions of a word or phrase | define: hydroponic |
| stocks: | Check financial activity of a particular stock | stocks:TWTR |

## Text Dorks 

| Dork | Description | Example|
|---| --- | --- |
| intitle:, allintitle:| Look for pages with titles containing the search terms.The dork “intitle:” applies to its search parameter only, while “allintitle:” applies to the entire query string.|[intitle:toy story](https://www.google.com/search?q=intitle%3Atoy+story), [intitle:”toy story”](https://www.google.com/search?q=intitle%3A%22toy+story%22)Compare the above with the number of search results of [toy story](https://www.google.com/search?q=toy+story) and [“toy story”](https://www.google.com/search?q=%22toy+story%22). [allintitle:”toy story”](https://www.google.com/search?q=allintitle%3A%22toy+story%22).Compare with [intitle:”toy story”](https://www.google.com/search?q=intitle%3A%22toy+story%22) — both have the same number of search results.|  
| inurl:  | Find links containing the character string | inurl:login.php, inurl: healthy inurl: eating |
| allinurl: | Finds links contianing all words following `:` | allinurl:healthy eating|
|intext:, allintext: | Finds websites containing the payload |Compare intext:"Index of /" +.htaccess, allintext:"Index of /" +.htaccess |
| link | Searches for external links to pages. | link:"keyword" | 
| numrange | Used to locate specific numbers in your searches. | numrange:321-325 | 
| before/after | Used to search within a particular date range. |filetype:pdf & (before:2000-01-01 after:2001-01-01) | 
|related | List web pages that are “similar” to a specific web page. | related:www.google.com | | cache | Shows the version of the web page that Google has in its cache. | cache:www.google.com |


