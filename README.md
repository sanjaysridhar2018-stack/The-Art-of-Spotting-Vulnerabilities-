# The Art of Spotting Vulnerabilities
## Introduction

## The wolf's approach

## Network Reconnaissance 
## Understanding vulnerability patterns
### OWASP top 10
### SQLi
To overcome the fog of not knowing how to proceed, the very first thing i learnt was how to identify if it is an SQLi vulnerability which was quite simple. Firstly, check for a database error by adding a ' at the end of the query, or add ;-- to check if the application behaves differently by taking the following query as a comment and omitting it. Besides this,you can also add OR 1=1 which always returns a true statement rendering the query to always give a true value. Secondly, despite having an in depth knowledge of SQL i definitely had a few knowledge gaps i had to fill like a few commands i didn't know like Union, concat() as well as the information_scheme database which are the core fundamentals for SQLi.Beyond this, just simply memorising the types of SQLi like in band, out of band, blind as well as their different subcategories was definitely a necessity but simply not enough and subsequently moved straight onto a CTF which was my first real challenge. 
### XSS
Unlike SQLi where I already had grasped the basics of SQL before, here I faced a real challenge since I had no idea about Javascript, making my fundamentals weak. Now CTFs are where the real application part begins, one major learning is to first deploy a random search query and analysing the page source. This gives you an idea whether the input is converted into HTML attribute, if it is embedded in an image or if words like script are banned. This shifted my paythway from blindly testing payloads and understanding how the application actually behaves. If I were stuck in a HTML attribute my first question would be how to escape it rather than how i would inject it. Besides spotting vulnerabilities, you have to be smart about exploiting them as well. For instance if words like <script> are banned you can replace it with <sscriptcript> which would behave the same way.
### CSRF
I understood that the way to spot a CSRF vulnerability is 1) when the site has a way to ask for requests like changing of email address 2) when the site does not verify the origin of the get/post request 
### SSRF

## Tools
### NMap
This is one of the fundamental tools used in one of the very first steps of reconnaisance to gather information about the hosts as well as open ports. It is the basis of OS fingerprinting and is also used to enumerate the version the server is running on which can be used for exploitation if outdated or to find out if any CVEs exist for that particular version.
### Hydra
If the site does not limit the number of post requests you can send the password can be guessed through brute forcing . This is where hydra comes into play- when a common password wordlist is given , hydra can bruteforce it and try to guess the password since theres no limitation for the number of post requests you can send.
### Gobuster
Gobuster is mainly used to discover directories or files whcih are hidden to the naked eye. Moreover, it can expose sensitive information as well as directories which are not meant to be accessed by anyone except the root
### Curl
Curl is used for sending http requests manually to the site whch is a manual alternative of burp suite, as well as to test api endpoints and access headers
### Netcat
Netcat is used to establish tcp connections and is the followup tool after using nmap- after finding the open ports through nmap, nc can be used to listen on those ports constantly which can be used to test reverse shells
### Burp Suite 


## Insights
