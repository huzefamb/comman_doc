# Footprinting
## Scanning host on network
1. namp
` nmap -sn < gateway > / cidr `


example
```
nmap -sn 192.168.0.1/24           
Starting Nmap 7.95 ( https://nmap.org ) at 2025-09-09 02:09 EDT
Nmap scan report for 192.168.0.1
Host is up (0.0064s latency).
MAC Address: B0:4E:26:22:5E:DA (TP-Link Technologies)
Nmap scan report for 192.168.0.105
Host is up (0.00020s latency).
MAC Address: AC:19:8E:12:E8:EB (Intel Corporate)
Nmap scan report for 192.168.0.108
Host is up (0.00085s latency).
MAC Address: 08:00:27:D2:AA:5F (PCS Systemtechnik/Oracle VirtualBox virtual NIC)
Nmap scan report for 192.168.0.106
Host is up.
Nmap done: 256 IP addresses (4 hosts up) scanned in 2.09 seconds
```

2. Netdiscover
`sudo netdiscover -r < gateway > / cidr `

Exmple

```
sudo netdiscover -r 192.168.0.1/24
 Currently scanning: Finished!   |   Screen View: Unique Hosts                                                                        
                                                                                                                                      
 178 Captured ARP Req/Rep packets, from 7 hosts.   Total size: 10680                                                                  
 _____________________________________________________________________________
   IP            At MAC Address     Count     Len  MAC Vendor / Hostname      
 -----------------------------------------------------------------------------
 192.168.0.105   ac:19:8e:12:e8:eb      5     300  Intel Corporate                                                                    
 192.168.0.107   78:2b:46:8f:f1:60    147    8820  Intel Corporate                                                                    
 192.168.0.103   c0:bf:be:3f:61:e7      4     240  AzureWave Technology Inc.                                                          
 192.168.0.1     b0:4e:26:22:5e:da     13     780  TP-LINK TECHNOLOGIES CO.,LTD.                                                      
 192.168.0.100   16:9d:5a:ae:8f:2d      5     300  Unknown vendor                                                                     
 192.168.0.108   08:00:27:d2:aa:5f      2     120  PCS Systemtechnik GmbH                                                             
 192.168.0.109   c0:bf:be:3f:61:e7      2     120  AzureWave Technology Inc.  
```
