# TCP SYN Flood Attack – Denial of Service Analysis

## Project Overview
This project analyzes a denial-of-service incident caused by a TCP SYN flood attack. The attack overwhelmed a web server by flooding it with incomplete TCP connection requests, resulting in service disruption and connection timeouts for legitimate users.

## Scenario
A travel agency experienced a website outage after employees reported connection timeout errors when accessing the company’s sales webpage. Network monitoring alerts indicated abnormal traffic targeting the web server.

## Tools & Techniques
- Wireshark (TCP packet analysis)
- TCP three-way handshake analysis
- Network attack identification
- Incident response documentation

## Key Findings
- Large volume of TCP SYN packets from a single unfamiliar IP address
- Incomplete TCP handshakes
- Server resource exhaustion
- Legitimate user connections failing

## Impact
The web server became unable to handle legitimate traffic, preventing employees from accessing sales and promotional content required for business operations.

## Conclusion
The outage was caused by a TCP SYN flood attack designed to exhaust server resources and deny service to legitimate users.
