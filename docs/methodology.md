# Methodology – Internal Network Exposure Assessment

## Goal
Identify internal hosts and services reachable on the LAN and reduce lateral movement risk through targeted hardening.

## Steps
1. Confirm assessor IP and subnet
2. Host discovery across the internal subnet
3. Service scan against identified server(s)
4. Identify high-risk services (remote admin, web apps, file shares)
5. Apply hardening:
   - Firewall allow-listing (only required ports)
   - Restrict admin services (SSH) to trusted admin workstation(s)
6. Re-scan to verify exposure reduction
