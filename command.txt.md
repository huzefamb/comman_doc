# Commands List

pwd - Shows your location in terminal.

ls -l - long listing (permissions, size, etc.)

ls -a - show hidden files (start with .)

ls -la - both together.

/etc - Directory.

/var - Directory.

/usr - Directory.

(~) - Refers to home.

sudo apt update - check for updates.

nmap - local system.

cd - change Directory
nmap	Basic scan (top 1000 TCP ports)	
nmap -sn	Ping scan – find live hosts only	
nmap -sS	SYN (stealth) scan	
nmap -sT	TCP Connect scan (no root needed)	
nmap -sU	Scan UDP ports	
nmap -p-	Scan all 65,535 ports	
nmap -p	        Scan specific ports	
nmap -sV	Detect service versions	
nmap -O	        Detect operating system	
nmap -A	        Aggressive scan (OS, version, scripts)	
nmap --script=vuln	Run vulnerability scan scripts
nmap scanme.nmap.org	Scan a website	
nmap --script=http-enum	      Web dir enum on HTTP port
nmap -iL	Scan multiple targets from a file	
nmap --exclude	Exclude IP from scan	
nmap -f	        Use fragmented packets (evade firewall)	
nmap -D	        Use decoy IPs to hide your own
nmap -sI	Idle scan (zombie host)	
nmap -T4	Set scan speed (0–5)	
nmap -oN	Save output in normal format	 
nmap -oG	Save grepable output	
nmap -oX	Save XML output	
✅ nmap -sS -sV -O -A --script=vuln -p- -T4	Full pentest scan (stealth, detailed, all ports)	
