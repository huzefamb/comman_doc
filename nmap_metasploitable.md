# nmap on metasploitable
target ip :192.168.0.110 \
purpose : learning  nmap scan \
aurthur : huzefa < huzefamb200207@gamil.com > 


## top 1000 port scanning 
nmap < target > 
```
──(root㉿kali)-[/home/kali]
└─# nmap 192.168.0.110     
Starting Nmap 7.95 ( https://nmap.org ) at 2025-09-13 02:15 EDT
Nmap scan report for 192.168.0.110
Host is up (0.0032s latency).
Not shown: 977 closed tcp ports (reset)
PORT     STATE SERVICE
21/tcp   open  ftp
22/tcp   open  ssh
23/tcp   open  telnet
25/tcp   open  smtp
53/tcp   open  domain
80/tcp   open  http
111/tcp  open  rpcbind
139/tcp  open  netbios-ssn
445/tcp  open  microsoft-ds
512/tcp  open  exec
513/tcp  open  login
514/tcp  open  shell
1099/tcp open  rmiregistry
1524/tcp open  ingreslock
2049/tcp open  nfs
2121/tcp open  ccproxy-ftp
3306/tcp open  mysql
5432/tcp open  postgresql
5900/tcp open  vnc
6000/tcp open  X11
6667/tcp open  irc
8009/tcp open  ajp13
8180/tcp open  unknown
MAC Address: 08:00:27:D2:AA:5F (PCS Systemtechnik/Oracle VirtualBox virtual NIC)

Nmap done: 1 IP address (1 host up) scanned in 0.78 seconds 
```


## scanning specific port 
nmap -p < port > < target > 
```
┌──(root㉿kali)-[/home/kali]
└─# nmap -p 21 192.168.0.110
Starting Nmap 7.95 ( https://nmap.org ) at 2025-09-13 02:18 EDT
Nmap scan report for 192.168.0.110
Host is up (0.00098s latency).

PORT   STATE SERVICE
21/tcp open  ftp
MAC Address: 08:00:27:D2:AA:5F (PCS Systemtechnik/Oracle VirtualBox virtual NIC)

Nmap done: 1 IP address (1 host up) scanned in 0.68 seconds
```


##scanning specific multiple ports 
nmap -p < port1 > < port2 > < target > 
```
┌──(root㉿kali)-[/home/kali]
└─# nmap -p 21,80 192.168.0.110
Starting Nmap 7.95 ( https://nmap.org ) at 2025-09-13 02:23 EDT
Nmap scan report for 192.168.0.110
Host is up (0.0011s latency).

PORT   STATE SERVICE
21/tcp open  ftp
80/tcp open  http
MAC Address: 08:00:27:D2:AA:5F (PCS Systemtechnik/Oracle VirtualBox virtual NIC)

Nmap done: 1 IP address (1 host up) scanned in 0.40 seconds
```


## scanning specific range 
nmap -p < start range > - < end range > < target > 
```
┌──(root㉿kali)-[/home/kali]
└─# nmap -p 1-100 192.168.0.110
Starting Nmap 7.95 ( https://nmap.org ) at 2025-09-13 02:29 EDT
Nmap scan report for 192.168.0.110
Host is up (0.0027s latency).
Not shown: 94 closed tcp ports (reset)
PORT   STATE SERVICE
21/tcp open  ftp
22/tcp open  ssh
23/tcp open  telnet
25/tcp open  smtp
53/tcp open  domain
80/tcp open  http
MAC Address: 08:00:27:D2:AA:5F (PCS Systemtechnik/Oracle VirtualBox virtual NIC)

Nmap done: 1 IP address (1 host up) scanned in 0.34 seconds
```


## scanning all ports 
nmap -p- < target > 
```
┌──(root㉿kali)-[/home/kali]
└─# nmap -p- 192.168.0.110     
Starting Nmap 7.95 ( https://nmap.org ) at 2025-09-13 02:35 EDT
Nmap scan report for 192.168.0.110
Host is up (0.00050s latency).
Not shown: 65505 closed tcp ports (reset)
PORT      STATE SERVICE
21/tcp    open  ftp
22/tcp    open  ssh
23/tcp    open  telnet
25/tcp    open  smtp
53/tcp    open  domain
80/tcp    open  http
111/tcp   open  rpcbind
139/tcp   open  netbios-ssn
445/tcp   open  microsoft-ds
512/tcp   open  exec
513/tcp   open  login
514/tcp   open  shell
1099/tcp  open  rmiregistry
1524/tcp  open  ingreslock
2049/tcp  open  nfs
2121/tcp  open  ccproxy-ftp
3306/tcp  open  mysql
3632/tcp  open  distccd
5432/tcp  open  postgresql
5900/tcp  open  vnc
6000/tcp  open  X11
6667/tcp  open  irc
6697/tcp  open  ircs-u
8009/tcp  open  ajp13
8180/tcp  open  unknown
8787/tcp  open  msgsrvr
36018/tcp open  unknown
48192/tcp open  unknown
51546/tcp open  unknown
57914/tcp open  unknown
MAC Address: 08:00:27:D2:AA:5F (PCS Systemtechnik/Oracle VirtualBox virtual NIC)

Nmap done: 1 IP address (1 host up) scanned in 11.25 seconds
```


## scanning UDP ports 
nmap -su -p < port > < target >
```
┌──(root㉿kali)-[/home/kali]
└─# nmap -sU -p 53 192.168.0.110
Starting Nmap 7.95 ( https://nmap.org ) at 2025-09-13 02:42 EDT
Nmap scan report for 192.168.0.110
Host is up (0.0022s latency).

PORT   STATE SERVICE
53/udp open  domain
MAC Address: 08:00:27:D2:AA:5F (PCS Systemtechnik/Oracle VirtualBox virtual NIC)
Nmap done: 1 IP address (1 host up) scanned in 0.49 seconds
```
