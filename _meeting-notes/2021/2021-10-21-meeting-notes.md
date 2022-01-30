---
title:  "Meeting Notes for Oct. 21, 2021"
date:   2021-10-21
categories: notes
author: scrypy
---

# Meeting Notes Oct. 21, 2021:

## Hacker Jeopardy

- Newz: This popular software recently disclosed a bug in their ssh key generation algorithms.
  - [Gitkraken](https://www.gitkraken.com/blog/weak-ssh-key-fix)
- Toolz: awk -v cols=$(tput cols) '{c=int(sin(NR/10)*(cols/6)+(cols/6))+1;print(substr($0,1,c-1)
"\x1b[41m" substr($0,c,1) "\x1b[0m" substr($0,c+1,length($0)-c+2))}' access_log | less -SR
  - [color a sine wave in a logfile output](https://twitter.com/climagic/status/1450835437753339905)
- Knawledge: what port is commonly used for SSH?
  - 22

## CTF Meetup this weekend

- just a couple people showed up in person last weekend for the NCL preseason, maybe b/c confusion with the poll in discord
- planning on setting up a team for the NCCDC, need to cover more attack/defense topics
- compete in overthewire for learning more about A&D skills: <https://overthewire.org/warzone/>
- download VM images from VulnHub to practice more A&D skills: <https://www.vulnhub.com/>
- <https://www.nationalccdc.org/index.php/competition/regionals>
- we are in the "at large" region and need to email the director for a sign up link

## CTF category of the week: scanning

- nmap homepage: <https://nmap.org/>
- scapy homepage: <https://scapy.net/>

## Prizes/Raffles

- gave away one book bundle
- awarded prizes for first and second place in the NCL preseason competition
