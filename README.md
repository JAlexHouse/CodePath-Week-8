# Project 8 - Pentesting Live Targets

Time spent: 12 hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: SQL Injection
![SQLI](https://raw.githubusercontent.com/acm482/CodePath-Week-8/master/gifs/blue-sqli.gif)
Additional Notes:
1. Exact url for the get sqli can be found [here](https://raw.githubusercontent.com/acm482/CodePath-Week-8/master/assets/SQLI-Blue.txt)

Vulnerability #2: Session Hijacking/Fixation
![Session Hijacking/Fixation](https://raw.githubusercontent.com/acm482/CodePath-Week-8/master/gifs/blue-session.gif)
Additional Notes:
1. Rather than use a php script, I used the plugin EditThisCookie. The plugin can be found [here](https://chrome.google.com/webstore/detail/editthiscookie/fngmhnnpilhplaeedifhccceomclgfbg?hl=en).

## Green

Vulnerability #1: Username Enumeration
![Enumeration](https://raw.githubusercontent.com/acm482/CodePath-Week-8/master/gifs/green-userenum.gif)
Additional Notes:

Vulnerability #2: Cross-Site Scripting
![XSS](https://raw.githubusercontent.com/acm482/CodePath-Week-8/master/gifs/green-xss.gif)
Additional Notes:
1. XSS script can be found [here](https://raw.githubusercontent.com/acm482/CodePath-Week-8/master/assets/XSS-Green.html)


## Red

Vulnerability #1: Insecure Direct Object
![IDOR](https://raw.githubusercontent.com/acm482/CodePath-Week-8/master/gifs/red-idor.gif)
Additional Notes:

Vulnerability #2: Cross-Site Request Forgery
![CSRF](https://raw.githubusercontent.com/acm482/CodePath-Week-8/master/gifs/red-csrf.gif)
Additional Notes:
1. The server blocked the use of iFrames via X-Frame-Options: Identify
2. The server also does not have a 'Access-Control-Allow-Origin' header, which defaults to blocking unlisted origins.
3. In order to combat the first two points, I elected to make use of the XSS Vulnerability on the Green site to bypass the origin policy and execute xmlhttp javascript to post the csrf request.
4. The XSS CSRF script can be found [here](https://raw.githubusercontent.com/acm482/CodePath-Week-8/master/assets/CRSF-Red-Javascript.html)


## Notes

Describe any challenges encountered while doing the work
