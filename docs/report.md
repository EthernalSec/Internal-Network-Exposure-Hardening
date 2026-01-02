# Internal Network Exposure & Hardening Report (Lab)

## Executive Summary
An internal assessment identified reachable services on a business server within the internal LAN. Hardening actions were implemented to reduce lateral movement risk by restricting inbound access to only required services and limiting administrative access to trusted devices.

## Lab Scope
- Internal LAN: 192.168.56.0/24
- Security workstation: Kali (192.168.56.101)
- Business server: Ubuntu + Docker + Juice Shop (192.168.56.102)

## Key Findings (Before Hardening)
- SSH (22/tcp) exposed internally
- Web application (3000/tcp) exposed internally

## Hardening Actions Implemented
1. Firewall enabled and configured using an allow-list approach
2. Restricted SSH to trusted admin workstation (192.168.56.101)
3. Allowed only required service port(s) for the business application
4. ### Firewall & Access Control

A host-based firewall (UFW) was enabled on the business server using a default-deny posture. Only required services were permitted:

- SSH (22/tcp) for administrative access  
- Web application (3000/tcp) for the business service  

Administrative SSH access was further restricted by allowing connections only from the trusted security workstation (192.168.56.101), reducing the risk of lateral movement following a workstation compromise.


## Verification
Post-hardening checks confirm reduced exposure to only necessary services.

## Evidence
See `evidence/` for scan output and firewall configuration snapshots.
