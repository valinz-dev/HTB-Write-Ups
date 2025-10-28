#  Hack The Box Writeups

Welcome to my collection of **Hack The Box** write-ups. This repository includes detailed notes and walkthroughs of **retired HTB machines**, written for educational and ethical purposes only.

> ⚠️ **Disclaimer:** All content is for **educational use** only. These writeups are based on publicly retired machines and follow HTB's rules and guidelines. Unauthorized use of this material on active machines is strictly prohibited.

---

## Machines Covered

| Machine Name | Difficulty | OS       | Status     |
|--------------|------------|----------|------------|
| Blue         | Easy       | Windows  | Complete   |
| Nibbles      | Easy       | Linux    | Complete   |
| Shocker      | Easy       | Linux    | Complete   |
| Irked        | Easy       | Linux    | Complete   |
| Traverxec    | Easy       | Linux    | Complete   |
| OpenAdmin    | Easy       | Linux    | Complete   |
| Knife        | Easy       | Linux    | Complete   |
| ScriptKiddie | Easy       | Linux    | Complete   |
| Armageddon   | Easy       | Linux    | Complete   |
| Legacy       | Easy       | Windows  | Complete   |
| Cronos       | Medium     | Linux    | Complete   |
| Nineveh      | Medium     | Linux    | Complete   |
| Magic        | Medium     | Linux    | Complete   |
| Jarvis       | Medium     | Linux    | Complete   |
| Poison       | Medium     | Linux    | Complete   |
| Haircut      | Medium     | Linux    | Complete   |
| Pit          | Medium     | Linux    | Complete   |
| Bastard      | Medium     | Windows  | Complete   |
| Worker       | Medium     | Windows  | Complete   |
| Intelligence | Medium     | Windows  | Complete   |
| Fuse         | Medium     | Windows  | Complete   |
| Passage      | Medium     | Linux    | Complete   |
| Sauna        | Medium     | Windows  | Complete   |
| Heist        | Medium     | Windows  | Complete   |
| Arctic       | Medium     | Windows  | Complete   |
| Reel         | Hard       | Linux    | Complete   |
| Kotarak      | Hard       | Linux    | Complete   |
| Tartarsauce  | Hard       | Linux    | Complete   |
| Conceal      | Hard       | Windows  | Complete   |
| RastaLabs    | Hard       | Windows  | Complete   |


*More machines coming soon as I progress through HTB!*

---

##  Tools & Techniques Used
Enumeration
General:

nmap – Port scanning and service version detection

rustscan – Fast port scanner, often used before nmap

netcat / nc – Banner grabbing, basic connections

ping, traceroute, whois, dig – Network reconnaissance

Web Enumeration:

dirb, gobuster, ffuf – Directory and file brute-forcing

nikto – Web vulnerability scanner

whatweb, wappalyzer – Identify technologies

curl, wget – Interact with endpoints manually

SMB / Windows-Specific:

enum4linux, enum4linux-ng – Enumerate SMB shares, users

smbclient, rpcclient, crackmapexec – Access and query SMB services

nmap --script smb* – SMB-related NSE scripts

bloodhound, SharpHound – Active Directory enumeration

Linux-Specific:

pspy, lsof, netstat – Monitor running processes and ports

Manual checks in /proc, cron, .bash_history

Exploitation
Web Applications:

Burp Suite – Intercept and modify HTTP traffic

SQLMap – Automated SQL injection

wfuzz, hydra – Credential brute-forcing

XSStrike, XSSer – XSS vulnerability testing

Shells and Payloads:

msfconsole – Metasploit Framework

msfvenom – Generate payloads

Manual command injection (;, &&, |, backticks)

File Upload / LFI / RFI Techniques:

Bypassing filters, exploiting vulnerable uploaders

Local/Remote File Inclusion testing

Privilege Escalation
Linux:

linPEAS, linux-smart-enumeration, LES – Automated enumeration

sudo -l – Check for sudo permissions

GTFOBins – Known privilege escalation paths

Check for SUID binaries: find / -perm -4000

Misconfigured cron jobs, writable /etc/passwd, exposed credentials

Windows:

winPEAS, PowerUp.ps1, Seatbelt.exe – Privilege enumeration

whoami /priv, icacls, accesschk.exe – Privilege analysis

Dump registry hives: SAM, SYSTEM, SECURITY

Exploitable configurations: AlwaysInstallElevated, unquoted service paths, weak ACLs

Post-Exploitation
Access & Shell Management:

netcat – Reverse/bind shell, tunneling

bash, python, perl, php – Web shell scripting

powershell – Advanced scripting and system interaction

Persistence Techniques:

SSH key injection

Scheduled tasks, cron jobs

Startup folder or Run key abuse

Credential and Data Collection:

Extract browser data, saved passwords, tokens

mimikatz, lsass dump

Credential reuse, token harvesting

Additional Tools & Techniques
evil-winrm – WinRM shell for Windows

impacket suite – Tools like secretsdump.py, psexec.py, wmiexec.py

responder, mitm6 – LLMNR/NBT-NS spoofing and poisoning

chisel, ngrok, ssh -R – Pivoting and tunneling

john, hashcat, crackstation.net – Password cracking

---
Last updated: 2025-09-24
