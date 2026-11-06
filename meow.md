# HTB - Meow (Starting Point)

**Difficulty:** Very Easy
**Category:** Telnet, Weak Credentials

## Summary
Scanned the target with nmap and found an open Telnet port (23). 
Attempted common default credentials and successfully logged in 
using a weak/blank root credential, demonstrating how unsecured 
legacy services can expose a system to trivial compromise.

## Methodology
1. Connected to the HTB network via OpenVPN
2. Ran `nmap -sV -Pn <target_IP>` to enumerate open ports
3. Found port 23 (Telnet) open, running Linux telnetd
4. Connected via `telnet <target_IP>`
5. Attempted common usernames (admin, administrator, root)
6. Logged in successfully as root with a blank password
7. Retrieved the flag using `cat flag.txt`

## Key Takeaways
- Importance of disabling unnecessary legacy services like Telnet
- Risks of weak/default/blank passwords
- Basic enumeration workflow with nmap

🔗 [View Achievement](https://labs.hackthebox.com/achievement/machine/4191519/394)
