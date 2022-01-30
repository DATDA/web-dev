---
layout: single
title: "Getting Started"
permalink: /getting-started/
author_profile: false
toc: true
toc_label: "Table of Contents"
toc_icon: "cog"
toc_sticky: true
---

# Getting Started With Cybersecurity

You may be asking yourself the following question: "Where the hell do I start?".
We all have been there, trust us. What we want to do here is to give you some basic starting points that will hopefully begin your torrid forays into the Dark Arts. Fret no longer my friend because here we have created a (semi)comprehensive guide to the l33t skillz you need to tackle the perilous world of cybersecurity!
Hackers are often described as the electronic handyman, the "jack of all trades, master of none"
of the techno world. This is very true in the fact that vulnerabilities and attacks can come
from any number of a bajillion different directions so knowing a little bit about a lot of
stuff can and a lot about a few things can get you very far in this field.
Also, there is definitely no need to be a master in ALL fields of cybersecurity, in the
workforce you will find yourself part of a team of very talented individuals who are very
talented in a few areas but lacking in others. Hopefully those 'others' areas are filled by
either you or some of your other teammates so that, combined, your teams knowledge encompasses
the entire spectrum of the field so that you may effectively combat cybercrime.

So, without further ado, I prezent to you a list of topics/walkthroughs to get your feet wet.

<p id="before"></p>

## Things to Know Before

You are about to get started learning about computer security which comes with it the inherent fact that many parts of it are dangerous. Since the best way to learn about anything computers is using computers, the fact that you are learning about the dangers parts of computers while using one means there is the possibility of being exposed to these dangers yourself. Below we have compiled a (again, somewhat) comprehensive steps and precautions that you should beware of before entering this field. Please be careful and remember, [Sic Hunt Leones](https://en.wikipedia.org/wiki/Here_be_dragons).
- **GET AN ANTIVIRUS!** This should always be step one, and one of the simplest and easiest to protect yourself from ~85% of all bad things. Paid programs can sometimes be the better option because A) the product is the product and not you. B) You are providing financial resources for the experts to continue being experts. But there are also free options such as ClamAV among others. So setup an antivirus, use it, dont bring it down for anything.
- **SETUP YOUR FIREWALL!** These can prevent baddies from ever getting inside your computer from the internetz.
- Get familiar with **sandboxing and file checking tools**. Virtual machines are usually the go to for opening risky files but have been known to be exploitable(i.e. the baddie breaks free from the VM and runs loose on your actual machine). VirtualBox and VMWare are the two most common. Dont open risky PDF, MS Office, or zip files on you own machine without scanning them, your antivirus will help with this. For exploring ZIP files, get familiar with the [binwalk](https://github.com/ReFirmLabs/binwalk/wiki/quick-start-guide) program on linux, this will tell you exactly what is inside of a file(i.e. ZIP), as there may be some bad script hidden and set to execute when you [unzip the folder](https://en.wikipedia.org/wiki/Zip_bomb).
- Buy yourself a **VPN subscription**. You'll be looking up a lot of stuff that has performed illegal activities before you knew about it, but why should you let others know your looking that up? A VPN will keep your activities fairly anonymous on the internet as well as providing an extra layer of encryption for you. With any sort of free VPN, you will be the product and that company will sell your internet history elsewhere, so fork up the bitcorn and pay.
- Use **javascript and tracking blockers** in your web browser. These will prevent Google Analytics from triggering and recording a visit to the site, as well as any other malicious javascript that might execute. For more tips see our Online Safety talks under the Presentation categories on the [wiki page](https://github.com/DATDA/main/wiki).
- **Dont blindly click on links**. See where they go first and determine whether or not that is a place that you actually want to go to. Sometimes throughout this site you will see [defanged urls](https://www.ibm.com/support/knowledgecenter/en/SSBRUQ_30.0.0/com.ibm.resilient.doc/install/resilient_install_defangURLs.htm) which is the process of slightly altering web links and addresses to prevent an accidental click-through to a malicious location. 

<p id="linux"></p>

## Linux

**Overview:** - The operating system that lets you control everything. Learn about the free Operating System that powers almost every backend server and high performance computing clusters.  
**Search Terms:** Debian, Ubuntu, Kali, Mint, Fedora
* [Beginners 1](http://www.reallylinux.com/)
* [Linux Basics](https://www.digitalocean.com/community/tutorials/an-introduction-to-linux-basics) by Digital Ocean.

**Setup Kali**  
To start learning some more Linux as well as begin exploring a common system for security, you should setup a Kali Linux system of some sorts. You can download the images from [here](https://www.kali.org/downloads/). In order to use this wonderful hacking OS you will eventually need to install it. Here is a list of tutorials that will cover that (since I am to lazy to type one up ;-P).
* [Null-Byte.wonderhowto](https://null-byte.wonderhowto.com/how-to/mac-for-hackers-install-kali-linux-as-virtual-machine-0174250/)
* [Hacking Tutorial](http://www.hacking-tutorial.com/hacking-tutorial/10-steps-how-to-create-kali-linux-virtual-machine-in-virtual-box/#sthash.FSi64ItA.dpbs)
* [Youtube](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=7&cad=rja&uact=8&ved=0ahUKEwiqvMWvpJHWAhXpgVQKHZRBAl4QtwIIjQEwBg&url=https%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DFvdJAJnlFz0&usg=AFQjCNGhGWTqP_gASRelb-T-O4JDXBgdTQ) NOTE: not previewed

After you have successfully installed either a VM or RM (real machine) then [here is a page with 10 tutorials](https://www.techworm.net/2016/11/top-10-best-tutorials-start-learning-hacking-kali-linux.html) covering some things you can do with Kali.

There is also several other security oriented virtual machines that are worth exploring:
* [SANS SIFT Incident Response VM](https://digital-forensics.sans.org/community/downloads)
* [Flare VM](https://www.fireeye.com/blog/threat-research/2017/07/flare-vm-the-windows-malware.html) FireEye reverse engineering Win10 VM.

<p id="home-net"></p>

## Home Network

The best way to practice these skills is by actually setting up and configuring machines on a network. Researchers at Idaho National Labs recommended that if you do not have your own somewhat advanced home network then you should begin doing that right away. Visit the pawn shop or WillGoodz for some cheap hardware(switches, routers, small cheap desktops, etc.) and build up. Below are some resources for guidance on how to setup your own home laboratory for doing security research:  
* https://www.cyberstudents.org/blog-post/build-your-own-lab/
* https://systemoverlord.com/2017/10/24/building-a-home-lab-for-offensive-security-basics.html
* https://www.reddit.com/r/homelab/comments/80r2d0/how_do_i_secure_my_homelab/
* https://www.udemy.com/build-your-own-cyber-lab-at-home/
* http://www.irongeek.com/security/building-an-infosec-lab-on-the-cheap.htm

<p id="commandline"></p>

## Command Line

**Overview:** - This is where the real power is. Unleash the power of the terminal explore the world of green text against a black background. Learn basic concepts for navigating around the commandline and using the many tools callable from a few keystrokes.  
**Search Terms:** Terminal, Bash,

<p id="networking"></p>

## Network Forensics

**Overview:** - Everything that is connected is useless unless it can communicate over that connection. Learn how networked communication works and how to extract meaningful information from network traffic captures. We have a [directory of network](https://github.com/DATDA/main/tree/master/networking) tools and scripts from past presentations and activities to check out.
**Search Terms:** Wireshark, OSI model, TCP/IP model, network packet structure,
- **Beginning:** Read up on the [OSI](https://en.wikipedia.org/wiki/OSI_model) and
[TCP/IP](https://www.geeksforgeeks.org/computer-network-tcpip-model/) models. These are different reference models used to define exactly at what [layer of abstraction](https://en.wikipedia.org/wiki/Abstraction_layer) you are currently looking/referencing. An understanding of these layers is the bottom of this learning pyramid

- **Practice:** Procure a copy of [Practical Packet Analysis](https://nostarch.com/packetanalysis3) for a good introductory walkthrough of exploring all sorts of wireless packet structures and scenarios associated with reading wireless data with Wireshark. If you want to explore the packets on your own then still visit that webpage and download the zip file containing the packet captures used in the book. These are free and you can open them up with Wireshark to walkthrough the network traffic and make your own determination of what is happening. [This Site](https://www.netresec.com/?page=PcapFiles) also has a good list of different types of network traffic

<p id="wireless"></p>

## Wireless

**Overview:** - Your home router provides it, so does your school, your phone, contactless payment systems, and everything without a cord. Learn about how wifi, bluetooth, and other wireless technologies work.  
**Search Terms:** wifi, aircrack-ng, bluetooth, bluesnarf, NFC/RFID,

<p id="osint"></p>

## OSINT - Open Source Intelligence

**Overview:** - Using freely available sources of knowledge/information to gather details about a target.  
**Search Terms:** Google dorks(trust me, its a thing), Maltego,  
- [Vortimo](http://vortimo.com/beta3/) - Automated OSINT collection tool
- [Automating OSINT](http://automatingosint.com/blog/) - blog about automating OSINT techniques

<p id="websites"></p>

## Web Technologies

**Overview:** - Everything is online nowadays. Most of it is crap. Here we exploit the crap. Learn how websites run and operate.  
**Search Terms:** HTML, HTML5, Javascript, NodeJS, CSS(styling for webpages, not super important but it's a thing), PHP, ASPnet
- Become familiar with the structure of an HTML document. Learn about div, form, input, and script tags and their functionality. 
- Learn some javascript. This is in almost every website and has been growing in popularity recently. Many different web exploits are through the javascript framework of the website so knowing this will get you a long way. This also allows you to perform some web scraping activities such as easily pulling all the information from a table into a csv output straight from your browser. 
- CSS is the web language that controls style and use useful to have a general understanding of. We have discovered some sites trying to obfuscate through CSS so explore the CSS methods for showing or hiding content.
- PHP is a backend server language that powers many websites such as WordPress. Understand how [form submissions](https://www.w3schools.com/php/php_forms.asp) work will be useful, this is the most common way for outsiders to interact with the actual server.
* We offer a number of vulnerable website sandboxes for exploration in our [playground](https://github.com/DATDA/main/wiki/Getting-the-right-connections).

<p id="databases"></p>

## Databases

**Overview:** - Almost everything and its mother is being stored in a database. Here you will learn how databases function and how to properly exploit them.  
***Search Terms:*** SQL(Standard Query Language), NoSQL, SQLite, MySQL, MariaDB, MongoDB  
- Learn SQL, structured query language. This is the language of pretty much all [relational databases](https://en.wikipedia.org/wiki/Relational_database). Learn how to create/delete/update databases, tables, and records using SQL. Then read about [SQL injection](https://www.w3schools.com/sql/sql_injection.asp) techniques which are an extremely common web application exploit and it is possible to find very revealing contained within the database with this technique.
 
<p id="reversing"></p>

## Reverse Engineering

**Overview:** - The goal of this section is to turn machine code back into a human readable format. Learn how to determine the contents of compiled and obfuscated programs.  
**Search Terms:** Decompiling, IDA Pro, HexRays, obfuscation, RE
- [Introductory Reversing course](https://sites.google.com/secured.org/malwareunicorn/reverse-engineering/re101) from Malware Unicorn.
- [Beginning Reversing Videos](https://www.youtube.com/channel/UCLDnEn-TxejaDB8qm2AUhHQ) from MalwareTech.
- [Malware Analysis for Hedgehogs](https://www.youtube.com/channel/UCVFXrUwuWxNlm6UNZtBLJ-A)
- [Create a Windows VM for malware research](https://zeltser.com/free-malware-analysis-windows-vm/)
- [Setup FLARE VM tools](https://github.com/fireeye/flare-vm) - useful PowerShell script to auto install a lot of common RE tools.
- The NSA recently released a new tool aimed at providing an open source competitor to [IDA Pro](https://www.hex-rays.com/products/ida/), called [Ghidra](https://github.com/NationalSecurityAgency/ghidra). Follow [this link](http://ghidra.re/online-courses/) for tutorials provided by the developers. 
- [Awesome Reverse Engineering](https://github.com/wtsxDev/reverse-engineering) resources list
- [Cuckoo Sandbox](https://cuckoosandbox.org/) - automated malware analysis tool
- [ARM Assembly and Exploitation](https://azeria-labs.com/) - website containing tutorials and slides from previous workshops held by Azeria Labs.
- [Incident Response List](https://github.com/meirwah/awesome-incident-response) - Github list of resources for incident response.

<p id="crypto"></p>

## Crypto

**Overview:** - Using fancy maths we are able to convert normal plain text into incomprehensible garbage that nobody can read unless they have the secret key. Learn basic hashing and encryption techniques. Check out our [crypto directory](https://github.com/DATDA/main/tree/master/crypto) for scripts and files from our past presentations and activities.
**Search Terms:** hashing, SHA256, DES, base64, elliptic curves(possibly backdoored)

<p id="wargames"></p>

## Wargames & Capture the Flag

**Overview:** - There are many services online that provide game-style lessons for learning security concepts.
**Search Terms:** wargames, ctf
- [SmashTheStack](http://smashthestack.org/) - Wargaming network
- [OverTheWire](https://overthewire.org/wargames/) - Wargaming network
- [CTFTime](https://ctftime.org) - Capture The Flag events page, view almost all available capture the flag events
- [National Cyber League](https://www.nationalcyberleague.org) - Capture the Flag contest held by CEDAR every semester
- [24/7 CTF](https://247ctf.com/) - Never ending CTF that allows you to practice solving challenges at your own pace. (thnx Mr. Peace for this link)
- [Embedded Security CTF](https://microcorruption.com/hall_of_fame) - CTF Focused on reversing firmware and hardware hacking


<p id="general-trainings"></p>

## General Trainings

- [Open Security Training](https://ost2.fyi/) - free security classes
- [Clark Center](https://clark.center) - Free industrial control system themed courses
