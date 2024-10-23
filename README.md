# Machines

| Machine Name        | Operating System | Tools Used                        | Skills Learned                 |
|---------------------|------------------|-----------------------------------|--------------------------------|
| [Lame](./Machines/Lame/) | Linux            | Nmap, FTP, SearchSploit, Metasploit, smbclient | Identifying vulnerable services, Exploiting Samba |
| [Mirai](./Machines/Mirai/) | Linux            | Nmap, Gobuster, SSH, df, strings            | Identifying an IoT device, Forensic file recovery |
| [Active](./Machines/Active/) | Windows         | Nmap, smbclient, gpp-decrypt, Impacket, John the Ripper, Metasploit | SMB enumeration techniques, Group Policy Preferences enumeration and exploitation, Identification and exploitation of Kerberoastable accounts |
| PermX | Linux            | TBA        |  This machine is still active. The writeup will be available once the machine is retired. |
| [BoardLight](./Machines/BoardLight) | Linux            | Nmap, Ffuf, Netcat, Git, Python3, SSH, Bash | Dolibarr Exploitation, SUID Exploitation      |
| GreenHorn | Linux            | TBA             | This machine is still active. The writeup will be available once the machine is retired. |
| [Blue](./Machines/Blue) | Windows         | Nmap, smbclient, crackmapexec, SearchSploit, Metasploit | Identifying Windows targets using SMB, Exploit modification  |
| [Legacy](./Machines/Legacy) | Windows         | Nmap, crackmapexec, SearchSploit, Metasploit   | Identifying vulnerable services, Exploiting SMB          |
| [Cap](./Machines/Cap/) | Linux            | Nmap, WireShark, FTP, SSH, Python, Wget, LINpeas | IDOR, Exploiting Linux capabilities   |
| [Jerry](./Machines/Jerry) | Windows         | Nmap, Python3, Metasploit, MSFVenom, Netcat| Tomcat exploitation using multiple approaches, Writing scripts to brute-force credentials, Custom war file payload creation |
| [Netmon](./Machines/Netmon/) | Windows | Nmap, FTP, Metasploit | Exploiting PRTG Network Monitor |
| [Keeper](./Machines/Keeper/) | Linux | Nmap, SSH, Git, SCP, Python3, KeePassXC, PuTTYgen | Identifying vulnerabilities in Request Tracker, KeePass exploitation |

# Starting Point

| Machine Name        | Operating System | Tools Used                        | Skills Learned                 |
|---------------------|------------------|-----------------------------------|--------------------------------|
| [Meow](./Starting%20Point/Tier%200/Meow/) | Linux | ping, Nmap, Telnet | Performing port scanning and service identification using Nmap, Exploiting Telnet|
| [Fawn](./Starting%20Point/Tier%200/Fawn/) | Linux | Nmap, FTP | Exploiting anonymous FTP login |
| [Dancing](./Starting%20Point/Tier%200/Dancing/) | Windows | Nmap, smbclient | Enumerating SMB shares |
| [Redeemer](./Starting%20Point/Tier%200/Redeemer/) | Linux | Nmap, redis-cli | Interacting with and enumerating a Redis server |
| [Explosion](./Starting%20Point/Tier%200/Explosion/) | Windows | Nmap, xfreerdp | Connecting to a remote desktop using xfreerdp |
| [Preignition](./Starting%20Point/Tier%200/Preignition/) | Linux | Nmap, Gobuster | Performing directory brute-forcing using Gobuster, Identifying and exploiting default web credentials |
| [Mongod](./Starting%20Point/Tier%200/Mongod/) | Linux | Nmap, mongo | Connecting to and interacting with a MongoDB instance |
| [Synced](./Starting%20Point/Tier%200/Synced/) | Linux | Nmap, rsync | Enumerating and downloading files from rsync shares |
| [Appointment](./Starting%20Point/Tier%201/Appointment/) | Linux | Nmap, BurpSuite | Performing SQL injection attack |
| [Sequel](./Starting%20Point/Tier%201/Sequel/) | Linux | Nmap, MySQL | Interacting with a MySQL database using MySQL CLI |
| [Crocodile](./Starting%20Point/Tier%201/Crocodile/) | Linux | Nmap, FTP, Gobuster| Gaining access to a system by combining FTP enumeration and directory brute-forcing |
| [Responder](./Starting%20Point/Tier%201/Responder/) | Windows | Nmap, Responder, John the Ripper, evil-winrm | Exploiting Local File Inclusion (LFI) vulnerabilities, Capturing and cracking NTLMv2 hashes |
| [Three](./Starting%20Point/Tier%201/Three/) | Linux | Nmap, WFuzz, awscli | Discovering and interacting with S3 buckets, Uploading and executing a PHP webshell |
| [Ignition](./Starting%20Point/Tier%201/Ignition/) | Linux | Nmap, Gobuster, BurpSuite | Brute-forcing admin login credentials, Discovering hidden directories |
| [Bike](./Starting%20Point/Tier%201/Bike/) | Linux | Nmap, Wappalyzer, BurpSuite | Exploiting Server-Side Template Injection (SSTI) vulnerabilities, Using Node.js globals to execute arbitrary system commands on the server |
| [Funnel](./Starting%20Point/Tier%201/Funnel/) | Linux | Nmap, FTP, SSH, psql | SSH tunneling (local port forwarding), Interacting with a PostgreSQL database |
| [Pennyworth](./Starting%20Point/Tier%201/Pennyworth/) | Linux | Nmap, BurpSuite, Netcat | Brute-forcing login credentials, Establishing a reverse shell |
| [Tactics](./Starting%20Point/Tier%201/Tactics/) | Windows | Nmap, smbclient | Enumerating and extracting files from SMB shares |
| [Archetype](./Starting%20Point/Tier%202/Archetype/) | Windows | Nmap, smbclient, Impacket (mssqlclient), Powershell, Wget, Netcat, WinPEAS | Exploiting Microsoft SQL Server vulnerabilities, Using WinPEAS for privilege escalation |
| [Oopsie](./Starting%20Point/Tier%202/Oopsie/) | Linux | Nmap, DirBuster, Gobuster, Netcat, SSH |  Cookie manipulation, Exploiting SUID binaries and PATH manipulation for root access |
| [Vaccine](./Starting%20Point/Tier%202/Vaccine/) | Linux | Nmap, FTP, John the Ripper, Hashcat, SQLmap, Netcat, vi | Password cracking with John the Ripper and Hashcat, Exploiting SQL injection vulnerabilities with SQLmap, Privilege escalation through configuration modification in `pg_hba.conf` and shell execution via vi |
| [Unified](./Starting%20Point/Tier%202/Unified/) | Linux | Nmap, BurpSuite, tcpdump, rogue-jndi, Netcat, mkpasswd, mongo, SSH | Exploiting JNDI injection vulnerabilities in Java applications, Interacting with MongoDB to retrieve and manipulate user credentials |
| [Included](./Starting%20Point/Tier%202/Included/) | Linux | Nmap, curl, TFTP, Netcat, lxc, Wget, Git, Python3 | Local File Inclusion (LFI) exploitation, LXD container privilege escalation |
| [Markup](./Starting%20Point/Tier%202/Markup/) | Windows | TBA | TBA |
| [Base](./Starting%20Point/Tier%202/Base/) | Linux | TBA | TBA |