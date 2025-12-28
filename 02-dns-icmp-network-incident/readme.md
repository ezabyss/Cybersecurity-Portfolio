# DNS & ICMP Network Traffic Analysis – Port 53 Unreachable

## Project Overview
This project analyzes a network connectivity incident where users were unable to access a website due to DNS resolution failure. Using tcpdump packet captures, DNS and ICMP traffic was analyzed to identify the affected protocol and possible root cause.

## Scenario
Users reported receiving a “destination port unreachable” error while attempting to access a website. Packet captures were collected during the incident to investigate the issue.

## Tools & Technologies
- tcpdump
- DNS (UDP)
- ICMP
- TCP/IP Model

## Key Findings
- DNS queries were sent using UDP to port 53
- ICMP error messages indicated “udp port 53 unreachable”
- DNS server did not respond to queries
- Domain name resolution failed

## Conclusion
The incident was caused by a failure in DNS service availability, preventing clients from resolving the website’s domain name.

## Skills
- Network traffic analysis
- DNS troubleshooting
- ICMP error interpretation
- Incident documentation
