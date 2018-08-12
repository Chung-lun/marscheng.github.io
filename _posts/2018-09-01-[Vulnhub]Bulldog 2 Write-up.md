---
layout: post
title:  "[Vulnhub]Bulldog 2 Write-up"
subtitle: ""
author: Mars Cheng
tags: 
- Penetration Testing
- Vulnhub
- OSCP
- Write-up
---
## Overview

>This is a vulnerable machine from vulnhub, and the write-up refers some internet resources. If any 
mistake or suggestion, please let we konw. Thanks.


## Walkthrough

### Information gathering
As usual, we firstly use Nmap to scan the machine which tool can discover machine port status, service, and version. 
* This machine only open port 80, and provide web service based on niginx 1.14.0.    

```console
[15:17:52] root:bulldog2/ # nmap -A 192.168.0.17 
# Nmap 7.70 scan initiated Tue Aug  7 15:17:52 2018 as: nmap -A  192.168.0.17 
Nmap scan report for 192.168.0.17
Host is up (0.0095s latency).
Not shown: 999 filtered ports
PORT   STATE SERVICE VERSION
80/tcp open  http    nginx 1.14.0 (Ubuntu)
|_http-cors: HEAD GET POST PUT DELETE PATCH
|_http-server-header: nginx/1.14.0 (Ubuntu)
|_http-title: Bulldog.social
MAC Address: F8:59:71:17:CF:41 (Intel Corporate)
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Device type: general purpose
Running: Linux 3.X|4.X
OS CPE: cpe:/o:linux:linux_kernel:3 cpe:/o:linux:linux_kernel:4
OS details: Linux 3.10 - 4.11, Linux 3.2 - 4.9
Network Distance: 1 hop
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE
HOP RTT     ADDRESS
1   9.55 ms 192.168.0.17

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Tue Aug  7 15:18:11 2018 -- 1 IP address (1 host up) scanned in 19.32 seconds
```

* We browse the website


