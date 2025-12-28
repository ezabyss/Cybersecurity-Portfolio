# Cybersecurity Incident Report
## Network Traffic Analysis

### Incident Summary
Users were unable to access the website www.yummyrecipesforme.com and received a destination port unreachable error. Network traffic was captured and analyzed using tcpdump.

### Evidence Collected
- Repeated DNS queries sent via UDP
- ICMP error messages returned from the DNS server
- Error message: “udp port 53 unreachable”

### Analysis
The tcpdump logs show that DNS requests were sent from the client system to the DNS server using UDP on port 53. Each request resulted in an ICMP error response indicating that the destination port was unreachable. This pattern occurred multiple times, confirming that DNS communication was consistently failing.

### Root Cause
The most likely root cause is that the DNS service on the destination server was unavailable, misconfigured, or blocked by a firewall, preventing UDP traffic on port 53 from being processed.

### Impact
Because DNS resolution failed, users were unable to obtain the IP address for the website, making the website inaccessible.

### Recommended Solution
- Verify that the DNS service is running on the server
- Check firewall rules to ensure UDP port 53 is allowed
- Confirm DNS server configuration
- Restart DNS services if necessary
- Monitor DNS traffic to confirm successful resolution
