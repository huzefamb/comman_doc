# 1. task nmap 
## nmap port scanning task 
target: scanme.nmap.org \
Do port scanning on given target to find the following:


1. 2 Open UDP ports \
2. 2 Open TCP ports \
3. Top 1000 open TCP ports \
4. If ports 10, 31, 80,9091 are open or not. \
5. Scan all open TCP ports 

### 1.1  2 open UDP ports 
nmap -sU -p < port1 > < port2 > < target > 
```
──(root㉿kali)-[/home/kali/Documents/reposditory/comman_doc]
└─# nmap -sU -p 80,25 scanme.nmap.org 
Starting Nmap 7.95 ( https://nmap.org ) at 2025-09-15 14:34 EDT
Nmap scan report for scanme.nmap.org (45.33.32.156)
Host is up (0.28s latency).
Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f

PORT   STATE  SERVICE
25/udp closed smtp
80/udp closed http

Nmap done: 1 IP address (1 host up) scanned in 1.14 seconds

```


### 1.2  2 open TCP ports
nmap -p < port1 > , < port2 > < target >
```
┌──(root㉿kali)-[/home/kali/Documents/reposditory/comman_doc]
└─# nmap -p 100,242 scanme.nmap.org  
Starting Nmap 7.95 ( https://nmap.org ) at 2025-09-15 14:37 EDT
Nmap scan report for scanme.nmap.org (45.33.32.156)
Host is up (0.27s latency).
Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f
rDNS record for 45.33.32.156: 156.32.33.45.in-addr.arpa

PORT    STATE  SERVICE
100/tcp closed newacct
242/tcp closed direct

Nmap done: 1 IP address (1 host up) scanned in 0.76 seconds
```


### 1.3  top 1000 open TCP ports 
nmap < target >
```                                                                                                                                                 
┌──(root㉿kali)-[/home/kali]
└─# nmap scanme.nmap.org  
Starting Nmap 7.95 ( https://nmap.org ) at 2025-09-15 14:19 EDT
Nmap scan report for scanme.nmap.org (45.33.32.156)
Host is up (0.28s latency).
Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f
rDNS record for 45.33.32.156: 156.32.33.45.in-addr.arpa
Not shown: 992 closed tcp ports (reset)
PORT      STATE    SERVICE
22/tcp    open     ssh
25/tcp    filtered smtp
80/tcp    open     http
139/tcp   filtered netbios-ssn
445/tcp   filtered microsoft-ds
5060/tcp  filtered sip
9929/tcp  open     nping-echo
31337/tcp open     Elite

Nmap done: 1 IP address (1 host up) scanned in 45.56 seconds
```


### 1.4  if ports 10, 31, 80, 9091 are open or not
nmap -p < port1 > < port2 > < port3 > < port4 > < target > 
```
┌──(root㉿kali)-[/home/kali/Documents/reposditory/comman_doc]
└─# nmap -p 10,31,80,9091 scanme.nmap.org
Starting Nmap 7.95 ( https://nmap.org ) at 2025-09-15 14:44 EDT
Nmap scan report for scanme.nmap.org (45.33.32.156)
Host is up (0.27s latency).
Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f

PORT     STATE  SERVICE
10/tcp   closed unknown
31/tcp   closed msg-auth
80/tcp   open   http
9091/tcp closed xmltec-xmlmail

Nmap done: 1 IP address (1 host up) scanned in 0.97 seconds
```


### 1.5  scan all TCP ports 
nmap -p- < target >
```
┌──(root㉿kali)-[/home/kali/Documents/reposditory/comman_doc]
└─# nmap -p- scanme.nmap.org
Starting Nmap 7.95 ( https://nmap.org ) at 2025-09-15 15:03 EDT
Nmap scan report for scanme.nmap.org (45.33.32.156)
Host is up (0.28s latency).
Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f
Scanned at 2025-09-15 15:03:41 EDT for 1060s
Not shown: 65518 closed tcp ports (reset), 1 closed tcp ports (admin-prohibited)
PORT      STATE    SERVICE
22/tcp    open     ssh
25/tcp    filtered smtp
67/tcp    filtered dhcps
68/tcp    filtered dhcpc
80/tcp    open     http
137/tcp   filtered netbios-ns
138/tcp   filtered netbios-dgm
139/tcp   filtered netbios-ssn
445/tcp   filtered microsoft-ds
4485/tcp  filtered assyst-dr
5060/tcp  filtered sip
9761/tcp  filtered unknown
9929/tcp  open     nping-echo
31337/tcp open     Elite
32786/tcp filtered sometimes-rpc25
44924/tcp filtered unknown
Final times for host: srtt: 278477 rttvar: 10051  to: 318681

Read from /usr/share/nmap: nmap-protocols nmap-services.
Nmap done: 1 IP address (1 host up) scanned in 1061.03 seconds
```
                                                          
