# Google Dorking,

Google dorking is a way of filtering the results from the search in google. We can filter it using some keywords mentioned below,

| Keywords   | Description                                                           | Usage                                                                   |
| ---------- | --------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| filetype:  | gives specific file type                                              | filetype:pdf                                                            |
| inurl:     | search in url                                                         | inurl:admin                                                             |
| intitle:   | search in title                                                       | intitle:admin                                                           |
| intext:    | search in text                                                        | intext:admin                                                            |
| site:      | gives the specific site                                               | site:google                                                             |
| allinurl:  | same as inurl                                                         | allinurl:admin+login                                                    |
| allintext: | same as intext                                                        | allintext:admin+login                                                   |
| related:   | search for related words                                              | related:photoshop                                                       |
| inanchor:  | search for the anchor text (any links with downloadable content)      | inanchor:                                                               |
| \*         | It is a wild card. If you want to search for anything, you can use it | site:\*book.com (any site ended with book.com)                          |
| +          | You can use it for adding search items                                | inurl:admin+login                                                       |
| -          | This can be use to eliminate anything from search result              | site:\*book.com -facebook.com (except facebook site will be the result) |
| \|         | This is also called 'or' operator                                     | inurl:admin \| inurl:login                                              |

Types of Bug using Google dorks,

- Server Misconfigurations,
- Sensitive information disclosure,
- Directory / Path traversal,
- Information disclosure,
- Insecure storage of credentials.

Example keywords,

- Index of
- Index of admin
- Index of backup
- Index of trash
- Index of /etc/passwd
- filetype:log inurl:"password.log"

Some critical files extensions,

- .db
- .inc
- .conf
- .env

About .htaccess and .htpasswd,

- .htaccess is a directory which can be store the sensitive information,
- .htpasswd is a file where sensitive information are stored.

![googleSearchResult](../images/1.png)