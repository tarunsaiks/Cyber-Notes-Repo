## What is OSINT ?

OSINT is gathering and analysing publicly available data for intelligence purposes, which includes information collected from the internet, mass media, specialist journals and research, photos, and geospatial information. The information can be accessed via the open internet (indexed by search engines), closed forums (not indexed by search engines) and even the deep and dark web. People tend to leave much information on the internet that is publicly available and later on results in impersonation, identity theft etc.

## **OSINT Techniques**

**Google Dorks**

Google Dorking involves using specialist search terms and advanced search operators to find results that are not usually displayed using regular search terms. You can use them to search specific file types, cached versions of a particular site, websites containing specific text etc.  Bad actors widely use it to locate website configuration files and loopholes left due to bad coding practices. Some of the widely used Google dorks are mentioned below:

-   **inurl**: Searches for a specified text in all indexed URLs. For example, `inurl:hacking` will fetch all URLs containing the word "hacking".
-   **filetype**: Searches for specified file extensions. For example, `filetype:pdf "hacking"` will bring all pdf files containing the word "hacking". 
-   **site**: Searches all the indexed URLs for the specified domain. For example, `site:tryhackme.com` will bring all the indexed URLs from  `tryhackme.com`.
-   **cache**: Get the latest cached version by the Google search engine. For example, `cache:tryhackme.com`.

For example, you can use the dork `site:github.com "DB_PASSWORD"` to search only in `github.com` and look for the string `DB_PASSWORD` (possible database credentials). You can learn more about Google dorks through [this](https://tryhackme.com/room/googledorking) free room.
![[78095df3e60ffa72f618bf9e735c129b.png]]

**WHOIS Lookup**

WHOIS database stores public domain information such as registrant (domain owner), administrative, billing and technical contacts in a centralised database. The database is publicly available for people to search against any domain and enables acquiring Personal Identifiable Information (PII) against a company, like an email address, mobile number etc., of technical contact. Bad actors can, later on, use the information for profiling, [spear phishing campaigns](https://www.trendmicro.com/vinfo/us/security/definition/spear-phishing) (targeting selected individuals) etc. Nowadays, registrars offer Domain Privacy options that allow users to keep their WHOIS information private from the general public and only accessible to certain entities like designated registrars. 

  

Multiple websites allow checking the WHOIS information against the website. For example, you can check WHOIS information on `github.com` through this [free website](https://who.is/whois/github.com). 

![Image for GitHub](https://tryhackme-images.s3.amazonaws.com/user-uploads/62a7685ca6e7ce005d3f3afe/room-content/52968096eecbc3a4838b1b2ea88ef2cd.png)

We can see that Google has allowed and disallowed specific URLs for web scrapers and search engines. The disallow parameter helps bad actors to identify sensitive directories that can be manually accessed and exploited, like the admin panel, logs folder, etc.

**Breached Database Search**

Major social media and tech giants have suffered data breaches in the past.  As a result, the leaked data is publicly available and, most of the time contains PII like usernames, email addresses, mobile numbers and even passwords. Users may use the same password across all the websites; that enables bad actors to re-use the same password against a user on a different platform for a complete account takeover. Many web services offer to check if your email address or phone number is in a leaked database; [HaveIBeenPwned](https://haveibeenpwned.com/) is one of the free services.   

![Image for Database Hack](https://tryhackme-images.s3.amazonaws.com/user-uploads/62a7685ca6e7ce005d3f3afe/room-content/013ed1d5089a766f057c74be80e17f1c.png)  

Elf Recon McRed tried to run all email addresses of the Santa gift shop website to identify any leakage, and gladly no data breach was found. 

  

**Searching GitHub Repos**

GitHub is a renowned platform that allows developers to host their code through version control. A developer can create multiple repositories and set the privacy setting as well. A common flaw by developers is that the privacy of the repository is set as public, which means anyone can access it. These repositories contain complete source code and, most of the time, include passwords, access tokens, etc.   

![Image for Github Repositories](https://tryhackme-images.s3.amazonaws.com/user-uploads/62a7685ca6e7ce005d3f3afe/room-content/01cbf12bf2825395635bff6b7f0dac65.gif)