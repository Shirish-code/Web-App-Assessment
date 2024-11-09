 Nmap Report

## Findings from Nmap Scan
This report details the open ports and services identified by the Nmap scan, along with any notable security considerations.

### Open Ports and Services
- **Port 22 (SSH)**: Used for secure shell access.
  - **Recommendation**: Restrict SSH access to trusted IPs only.
- **Port 80 (HTTP)**: Unencrypted web traffic.
  - **Recommendation**: Redirect all HTTP traffic to HTTPS to ensure secure communication.
- **Port 443 (HTTPS)**: Secured web traffic, configured properly.

### Security Issues
- Open ports increase the attack surface and should be minimized wherever possible.
  - **Recommendation**: Use firewall rules to limit access to necessary ports and services.