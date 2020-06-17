# Windows

## Active Directory
- [Active Directory Security](https://adsecurity.org/)

## Tools
- [BloodHound](https://github.com/BloodHoundAD/BloodHound)
- [Nishang](https://github.com/samratashok/nishang) - Offensive PowerShell for red team, penetration testing and offensive security.
- snmpwalk
- hydra - bruteforce logins
	- slow to avoid timeouts, so you want a smaller password lists
- enum4linux - Null session enumeration
- CrackMapExec - grab plaintext passwords out of memory
- Responder - DNS spoofing tool
- Bettercap - ARP spoofing

## Notes
- SMB (server message block) for inter-node communication
	- 139, 445 ports
- domain controllers 53 (DNS), 88 (kerberos), 389 (ldap), RDP (3389)
- Kerberoasting
	- https://www.blackhillsinfosec.com/a-toast-to-kerberoast/
	- https://www.varonis.com/blog/kerberos-how-to-stop-golden-tickets/
- Null Session - Anonymous
	- connect with empty username and password
- NTLM
	- checks password hash
	- https://en.wikipedia.org/wiki/NT_LAN_Manager
- Getting System is higher than admin
- psexec - https://ss64.com/nt/psexec.html
