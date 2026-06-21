# The Art of Spotting Vulnerabilities
## Introduction

## The wolf's approach

## Network Reconnaissance 
## Understanding vulnerability patterns
### OWASP top 10
### SQLi
To overcome the fog of not knowing how to proceed, the very first thing i learnt was how to identify if it is an SQLi vulnerability which was quite simple. Firstly, check for a database error by adding a ' at the end of the query, or add ;-- to check if the application behaves differently by taking the following query as a comment and omitting it. Besides this,you can also add OR 1=1 which always returns a true statement rendering the query to always give a true value. Secondly, despite having an in depth knowledge of SQL i definitely had a few knowledge gaps i had to fill like a few commands i didn't know like Union, concat() as well as the information_scheme database which are the core fundamentals for SQLi. Finally, besides just learning the types of SQLi like in band, out of band, blind as well as their different subcategories i preferred an application based learning and moved straight onto a CTF which was my first real challenge. 
### XSS
### CSRF
### SSRF

## Tools
## Insights
