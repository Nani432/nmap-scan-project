# Basic Nmap Scan

**Target scanned:** `127.0.0.1` (localhost — my own machine)  
**Tool used:** Zenmap (Nmap GUI) — command shown: `nmap -T4 -A -v 127.0.0.1`  
**Date:** _(add date you ran the scan)_

---

# What is this
This repo contains the results of a simple Nmap network scan used for learning. The scan finds which ports (network “doors”) are open and what services (programs) are listening on those ports.

---

# Files in this project
- `nmap_scan_results.txt` — raw output from the Nmap scan (exact text copied from Zenmap).  
- `README.md` — this file.  
- `screenshots/scan_output.png` — screenshot of Zenmap showing the scan output.

---

# Quick summary of findings (simple)
- **Detected OS:** Windows (Nmap guessed the host runs Windows).  
- **Detected service(s):** SMB (smb2) was shown by Nmap scripts (Windows file-sharing service).  
- For full details, open `nmap_scan_results.txt` — it lists all ports, services, and script output.

---

# What some common lines mean (plain language)
- `22/tcp open ssh` → SSH service (remote login).  
- `80/tcp open http` → Web server (website).  
- `443/tcp open https` → Secure web server (HTTPS).  
- `445/tcp open smb` → Windows file sharing (SMB).  

> If you see a line like `PORT STATE SERVICE`, the first column is the port number, the second column is whether it is open, and the third is the service name.

---

# How to reproduce this scan (steps I used)
1. Open **Zenmap**.  
2. In **Target** enter: `127.0.0.1` (or the IP of a VM you own).  
3. Choose profile **Intense scan** (or use the Command shown: `nmap -T4 -A -v <target>`).  
4. Click **Scan** and wait for the scan to finish.  
5. Save the output: `File → Save Scan` or copy the **Nmap Output** text to `nmap_scan_results.txt`.  
6. Take screenshots of the output and save them in the `screenshots/` folder.

---

# Safety & legal note
Only scan machines you **own** or have **explicit permission** to scan. Scanning other people’s devices or networks without permission may be illegal.

---

# Short recommendations (if this were a real server)
- If a service is not needed, **close** the port or stop the service.  
- For services that must be open, use **strong passwords**, **firewall rules**, and enable **encryption** (for example, HTTPS).  
- Keep software updated to avoid known vulnerabilities.

