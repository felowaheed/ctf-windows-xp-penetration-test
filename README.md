# CTF Penetration Test — Kali Linux vs Windows XP

Full walkthrough of a Capture The Flag (CTF) challenge completed as part of a 
university cybersecurity course. A Kali Linux attacker machine was used to 
compromise a Windows XP target machine over a NAT-configured virtual network.

---

## Environment Setup
- **Attacker:** Kali Linux (virtual machine)
- **Target:** Windows XP (virtual machine)
- **Network:** NAT configuration connecting both machines
- **Tools:** Nmap, Metasploit Framework (msfconsole), Meterpreter

---

## Phase 1 — Network Reconnaissance
- Used Nmap to scan the network and discover live hosts
- Identified the target machine's IP address
- Enumerated open ports and fingerprinted the target operating system
- Confirmed target was running Windows XP (32-bit)

---

## Phase 2 — Vulnerability Scanning
- Ran a full vulnerability scan against the target
- Identified exploitable vulnerabilities specific to the Windows XP 32-bit system

---

## Phase 3 — Exploitation
- Launched Metasploit Framework via msfconsole
- Selected the appropriate exploit module for the identified vulnerability
- Configured payload for the 32-bit target architecture
- Successfully executed the exploit and opened a Meterpreter shell on the target

---

## Phase 4 — Post-Exploitation
- Navigated the victim filesystem using Meterpreter commands
- Located and exfiltrated flag files:
  - `theflag.txt`
  - `Flag-catch-it.tar.gz`
- Extracted the archive and executed an embedded Python script
- Remotely changed the Windows XP system password

---

## Outcome
All CTF objectives completed successfully:
- Remote shell access gained
- Flag files located and exfiltrated
- System password changed remotely

---

## Topics
Cybersecurity · Penetration Testing · Metasploit · Kali Linux · 
CTF · Network Reconnaissance · Nmap · Meterpreter · Ethical Hacking
