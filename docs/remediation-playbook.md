# Remediation Playbook (Practical Hardening)

## Firewall (UFW)
- Enable firewall
- Allow only required ports
- Restrict administrative services (SSH) to trusted IPs

## SSH Hardening (recommended)
- Disable password login when feasible
- Require key-based authentication
- Limit users who can SSH
- Consider moving SSH behind VPN / allowlist

## Web App Exposure
- Restrict internal apps to only the users who need access
- Consider reverse proxy + authentication for internal apps
- Monitor access logs

## Verification
Re-scan after changes to confirm only required ports remain reachable.
