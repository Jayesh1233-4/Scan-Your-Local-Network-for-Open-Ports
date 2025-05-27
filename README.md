# Scan-Your-Local-Network-for-Open-Ports

This repository documents a basic network reconnaissance task where I used **Nmap** to scan my local network for open ports.


## Task

**Objective:** Discover open ports on devices in the local network to understand network exposure.

**Tools Used:**
- [Nmap](https://nmap.org/) (free)

  
## Steps Performed

1. Installed Nmap from the official site.
2. Identified my local IP range: `192.168.89.0/24`.
3. Ran the following command to perform a TCP SYN scan:
   ```bash
   nmap -sS 192.168.89.0/24

4. Collected the following results:
192.168.89.57: Open port 53 (domain)
192.168.89.104: Open ports 22 (ssh), 135 (msrpc), 139 (netbios-ssn), 445 (microsoft-ds)
192.168.89.19: All ports closed

5. Security Risks Identified
SSH (port 22) exposed on 192.168.89.104.
NetBIOS and SMB ports (135, 139, 445) open, which could be a risk if not properly secured.
DNS service (port 53) open on 192.168.89.57.

## Outcome

 Gained basic network reconnaissance skills.
Understood the open services and potential risks in the local network.
