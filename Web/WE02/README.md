# WE02 (100 pts)

## Description
View the page at https://cfta-we02.allyourbases.co and try to get the flag.

## Approach
Upon visiting the site, nothing jumps out in the page source or front end, so we can do initial checks including /robots.txt (also mentioned in the spoiler sent out), which shows this.
```
User-agent: *

Allow: /
Disallow: /4ext6b6.html
```
When we visit the disallowed page (https://cfta-we02.allyourbases.co/4ext6b6.html), we find the flag.

## Flag
`Shhh_robot_you_said_too_much!`
