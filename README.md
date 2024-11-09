# Comprehensive Web Application Security Assessment and System Hardening

This project performs a thorough security assessment of a vulnerable web application using tools like **OWASP ZAP**, **Qualys**, **Nmap**, and **Nikto**. The goal is to identify potential vulnerabilities and develop a structured plan for system hardening based on the findings.

---

## Table of Contents
- [Project Overview](#project-overview)
- [Tools Used](#tools-used)
- [Folder Structure](#folder-structure)
- [Commands Used](#commands-used)
- [Results Summary](#results-summary)
- [System Hardening Recommendations](#system-hardening-recommendations)
- [License](#license)

---

## Project Overview

This project encompasses a security audit on a target environment to identify web application and network vulnerabilities. The assessment focuses on web vulnerabilities, network exposure, and system misconfigurations. Following the scans, system hardening techniques are suggested to improve the security posture of the target.

## Tools Used

1. **OWASP ZAP** - Automated tool to find web application security risks.
2. **Qualys** - Provides in-depth vulnerability scanning and reporting.
3. **Nmap** - Network scanner used to detect open ports and services.
4. **Nikto** - Web server scanner for detecting outdated software and server misconfigurations.

## Folder Structure

The project folder is organized as follows:
project-folder/ │ ├── reports/ │ ├── zap-report.pdf │ ├── qualys-report.pdf │ ├── nikto-report.txt │ └── nmap-report.txt │ ├── documentation/ │ ├── vulnerability_summary.md │ ├── system_hardening.md │ └── findings.md │ ├── scripts/ │ └── commands.sh │ └── README.md


## Commands Used

### Nmap
- Basic network scan to discover open ports:
  ```bash
  nmap -sV <target-ip>

### Nikto
Web server vulnerability scan:

nikto -h <target-ip>

### OWASP ZAP
- Active scan:
  Launched within the ZAP GUI to analyze web application vulnerabilities.

### Qualys
- QualysGuard platform scan:
  Detailed vulnerability report generated using Qualys web-based interface.


### Results Summary
 - OWASP ZAP Findings
   Identified several security misconfigurations and potential threats in web application components, including: 
   1. Missing security headers
   2. Outdated libraries in use
 
 - Qualys Findings
   1.   Provided in-depth analysis of OS-level vulnerabilities and patch status.
   2.   Several high-priority vulnerabilities found related to system services and configurations.

 - Nmap Findings
   Detected open ports exposing critical services:
   1. Ports 22, 80, 443 were open
   2. Services associated with these ports required hardening or access restriction.

 - Nikto Findings
   Exposed misconfigurations in the web server:
   1. Outdated software
   2. HTTP methods not securely configured

### System Hardening Recommendations
Based on the findings, the following system hardening steps are recommended:

- Network Hardening
  1. Restrict open ports (limit external access where possible).
  2. Use firewall rules to manage access to necessary services.

- Web Application Hardening
  1. Implement security headers (e.g., Content-Security-Policy, X-XSS-Protection).
  2. Update web server software and libraries to the latest versions.

- OS-Level Hardening
  1. Regularly update and patch OS and software.
  2. Disable unnecessary services and protocols (e.g., disable FTP if not required).
  3. Implement user access controls and enforce strong password policies.