---
layout: single
author_profile: true
read_time: true
comments: true
share: true
related: true
toc: false
toc_label: "TOC LABEL"
toc_icon: file-alt
toc_sticky: false
title:  "Meeting Notes for Nov. 4, 2021"
date:   2021-11-04
categories: notes
author: scrypy
---

## Hacker Jeopardy

- Newz: This is the amount of money Google will pay you if you can exploit a linux kernel flaw.
  - `$31,337`
- Toolz: `awk -v cols=$(tput cols) '{e=int(log($10)*5); print("\x1b[42m" substr($0, 1, e) "\x1b[0m" substr($0, e+1) )}' access_log | less -SR`
- Knawledge: This is the name of a virtual machine dedicated to security monitoring capabilities
  - Security Onion

## Website Revamp

- Discussed the possiblity of revamping the website (aka changing the jekyll template being used for the website)
- Trying to "combine" the current website with the wiki in github. Better way to organize the presentations we have stored in the github

## Review of problems from previous CTFs

- Discussed the first couple of problems from the Flareon competition
- went over a couple interesting problems that stumped us from the NCL Individual competition

## Planning NCL Meetup this weekend

- meeting in EERB 228 on Saturday from 11 AM till 4 PM to work on the NCL team competition.

## Raffle Giveaway

Gave away a Humble Bundle book bundle to one lucky member who was present at the meeting. 
