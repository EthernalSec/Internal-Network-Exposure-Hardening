# Internal-Network-Exposure-Hardening
# Internal Network Exposure & Hardening (Lab)

## What this project shows
This project demonstrates how an internal network is assessed after an attacker gains initial access (e.g., phishing) and how to reduce lateral movement risk through practical hardening.

A realistic lab environment was built using:
- Kali Linux (security workstation)
- Ubuntu server hosting OWASP Juice Shop in Docker (business application)
- An internal “office LAN” using a host-only network

## Why it matters
Many real incidents escalate because internal services are overly reachable (SSH, admin portals, web apps). Reducing exposure and enforcing access controls can prevent ransomware spread and server takeover.

## What was performed
- Internal host discovery (identify devices on the LAN)
- Service identification (determine exposed internal services)
- Hardening actions:
  - Firewall rules to allow only required ports
  - Administrative access restrictions (SSH limited to admin workstation)

## Deliverables
- Client-style report: `docs/report.md`
- Remediation playbook: `docs/remediation-playbook.md`
- Evidence: `evidence/`

## Ethics
Only test environments you own or have explicit authorization to assess.
