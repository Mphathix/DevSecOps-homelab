# My DevSecOps Journey & Security Home Lab

## About Me
Hello! I am a **Web Application Developer Intern at Studyhalo**. While building software is incredible, I am taking my next professional step to explore System Operations, Networking, and Cybersecurity. I am following the structured path on **roadmap.sh/devsecops** to transition into a DevSecOps engineering mindset.

Before introducing security tools into our development pipelines at Studyhalo, I am building an isolated **Nested Virtual Home Lab** to master core networking, firewalls, threat monitoring, and system administration.

---

## Complete Target Lab Architecture
This is the full corporate-style blueprint I am building inside my physical machine based on the virtualization series by [Lyal Saayman](https://youtube.com/playlist?list=PLjjkJroii8DDb0QZpWLo978VXcLp8-xW3&si=AP1xgUCPSNLeufz_). It acts as a segmented corporate environment split by a centralized firewall.

* **Hypervisor Component:** Oracle VM VirtualBox
* **Central Gateway Firewall:** OPNsense (FreeBSD 64-bit) - Acting as the perimeter router and traffic inspector.
* **The Attacker Subnet:** Kali Linux Workspace - Used for security auditing and penetration testing.
* **The Target Enterprise Subnet:** 
  * Windows Server (Active Directory Domain Controller)
  * Windows 10 Enterprise Client (Victim Endpoint)
  * Ubuntu Linux Server (Production Asset)
* **The Security Operations Center (SOC) Log Analysis Pipeline:** Elastic Monitoring Server (SIEM) - Collecting security events from the entire environment to spot attacks.

---

## Project Execution Roadmap & Lab Logs
To keep my 16GB RAM laptop stable, I am executing this project in strict operational phases and documenting every hurdle.

* **Phase 1: Firewall Perimeter & Attacker Node Verification**
  * *Log File:* [Read the full lab journal](./logs/homelab-journal.md)
  * *Key Milestones:* Fixed a missing Microsoft runtime dependency for VirtualBox, rebuilt OPNsense after a post-install disk error, and worked around the missing DHCP server with a temporary static IP so Kali could reach the OPNsense web GUI.
