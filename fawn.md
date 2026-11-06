# HTB - Fawn (Starting Point)

**Difficulty:** Very Easy
**Category:** FTP, Anonymous Login

## Summary
Scanned the target with nmap and found an open FTP port (21) running 
vsftpd 3.0.3 on a Unix host. Logged in using the anonymous account, 
a common FTP misconfiguration that allows unauthenticated access, 
and retrieved the flag file.

## Methodology
1. Connected to the HTB network via OpenVPN
2. Ran `ping <target_IP>` to confirm connectivity
3. Ran `sudo nmap -sV <target_IP>` to enumerate open ports and services
4. Found port 21 (FTP) open, running vsftpd 3.0.3 on Unix
5. Connected via `ftp <target_IP>`
6. Logged in using the `anonymous` username with any password
7. Listed files with `ls` and found `flag.txt`
8. Downloaded it using `get flag.txt`
9. Exited FTP and read the flag using `cat flag.txt`

## Key Takeaways
- FTP anonymous login is a common misconfiguration to check for
- FTP transmits data unencrypted; SFTP/FTPS should be used instead
- Importance of version detection (`-sV`) during enumeration

🔗 [View Achievement](https://labs.hackthebox.com/achievement/machine/4191519/393)
