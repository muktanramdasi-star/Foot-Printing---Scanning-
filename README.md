# Foot-Printing---Scanning-
Hands-on domain footprinting, DNS enumeration, subnet scanning, ARP inspection, and network topology mapping for the Networkwalks Week 2 cybersecurity internship.

Hands-on domain footprinting, DNS enumeration, subnet scanning, and network topology mapping for the Networkwalks Week 2 cybersecurity internship.

# PENETRATION TESTING & NETWORK SCANNING REPORT

## Description & Overview
This report documents the practical execution of Week 2 tasks (W2-PM1 and W2-PM5) under the Networkwalks Cybersecurity Internship Program.

The primary objective was to perform domain reconnaissance, collect target infrastructure metadata, identify active hosts on the local subnet, and understand network scanning and topology mapping.

All activities were executed within the approved testing scope for educational and cybersecurity training purposes.

## 1. Document Metadata & Scope
* Pentester Name: Mukta Ramdasi
* Program / Batch: Networkwalks Cybersecurity Internship
* Date: November 12, 2026
* Modules Completed: W2-PM1 (Multiple Kali Tools), W2-PM5 (Zenmap Scanning)
* Target Environments:
  * networkwalks.com (Secured written permission)
  * Local Subnet / Virtual LAN Network
* Permission Status: Secured written permission from client (Yes)
* Phases Covered: Phase 1 (Reconnaissance & Footprinting), Phase 2 (Scanning & Network Discovery), Phases 3–5 (In Progress)

## 2. Executive Summary & Liability Disclaimer
This report contains confidential technical information gathered during authorized security testing under the Networkwalks Cybersecurity Internship Program.

The activities focused on domain footprinting, DNS enumeration, website technology detection, Web Application Firewall identification, HTTP header inspection, local network host discovery, and topology visualization.

All activities were executed within the approved scope covering networkwalks.com and the local network. Unauthorized distribution or misuse of this security data is strictly prohibited.

## 3. Technical Activities & Findings

### 3.1 Domain Reconnaissance & Footprinting (Task W2-PM1)
Target Domain: networkwalks.com

* WHOIS Enumeration (whois): Collected domain registration details, identifying GoDaddy.com, LLC as the registrar (Creation Date: 06 November 2019 | Expiry Date: 06 November 2027).
* DNS Enumeration (dnsrecon): Collected DNS records, identifying SOA and NS servers (://hostgator.com and ://hostgator.com), MX server (://networkwalks.com), and A record IP address (192.232.216.135).
* WhatWeb Fingerprinting (whatweb): Identified website technologies, including Apache, WordPress 7.1.4, Bootstrap 7.1.4, and jQuery 3.7.1.
* DNS Resolution (nslookup): Performed DNS resolution, confirming that networkwalks.com resolves to 192.232.216.135.
* WAF Inspection (wafw00f): Executed Web Application Firewall fingerprinting and detected ModSecurity (SpiderLabs).
* HTTP Header Analysis (curl -I): Inspected HTTP response headers, observing HTTP/2 200 OK, Apache server details, security-related response headers, and active HTTP-to-HTTPS redirection.

### 3.2 Subnet Discovery & Topology Mapping (Task W2-PM5)
Target Network: Local Subnet / Virtual LAN Network

* Identified the local network configuration using Windows IP Configuration.
* Initiated an Nmap Ping Scan (-sn) through the Zenmap GUI across 256 IP addresses (completed in approximately 8.06 seconds using Nmap version 7.99).
* Captured scan results and visualized the network topology using Zenmap's graphical interface.

## 4. Risk Analysis & Threat Impact
* Information Exposure via Passive Reconnaissance: Publicly available WHOIS and DNS records reveal domain and infrastructure information that could assist external reconnaissance.
* Technology Disclosure: Identifying website technologies and software versions may help attackers research potential weaknesses in the technology stack.
* Network Visibility: Discovering active hosts provides information about devices connected to the local network.

Note: No open ports, running services, or vulnerabilities were verified or exploited during the Ping Scan.

## 5. Security Recommendations
* Keep website software, CMS platforms, plugins, and server components updated.
* Review DNS records and domain registration information regularly.
* Maintain updated Web Application Firewall (ModSecurity) rules and configurations.
* Monitor active devices and network traffic regularly.
* Perform authorized port scanning and vulnerability assessments when required.

## 6. Conclusion
The Week 2 tasks (W2-PM1 and W2-PM5) provided practical experience in domain footprinting, DNS enumeration, website technology detection, network discovery, and topology visualization.

Tools including WHOIS, WhatWeb, Nslookup, DNSRecon, cURL, WAFW00F, Nmap, and Zenmap helped gather target metadata and map local network devices. The collected terminal outputs and screenshots were saved as technical evidence for documentation and internship submission.

## 7. Tools & Command Reference
The following tools and commands were used during the security assessment:

| Command / Tool | Technical Purpose |
| :--- | :--- |
| whois networkwalks.com | Retrieves domain registration details and registrar information. |
| dnsrecon -d networkwalks.com | Enumerates DNS records (SOA, NS, MX, A, TXT, SRV) and infrastructure data. |
| nslookup networkwalks.com | Performs DNS resolution for the target domain. |
| whatweb networkwalks.com | Identifies web server technologies, CMS, and frontend libraries. |
| wafw00f networkwalks.com | Detects Web Application Firewall (WAF) protection. |
| curl -I http://networkwalks.com | Examines HTTP response headers, server details, and HTTPS redirects. |
| ipconfig /all | Displays local network configuration on Windows. |
| nmap -sn <local-subnet> | Performs host discovery (Ping Scan) across the local subnet. |
| Zenmap | Provides a graphical interface for Nmap scanning and network topology mapping. |

## 8. Evidences Collected
The following terminal outputs and screenshots were captured during the practical activities:

* WHOIS terminal output.
* WhatWeb technology detection output.
* Nslookup DNS resolution results.
* DNSRecon enumeration output.
* cURL HTTP response header output.
* WAFW00F detection output.
* Zenmap Nmap Ping Scan screenshot.
* Zenmap network topology screenshot.

## Author & Reference Information
* Author: Mukta Ramdasi
* Program: Networkwalks Cybersecurity Internship
* LinkedIn Profile: linkedin.com/in/mukta-ramdasi-605350335




