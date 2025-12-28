# tcpdump Log Explanation

This file explains a tcpdump log used to analyze a DNS failure where ICMP error messages were returned.

---

## Scenario Overview
A user attempted to access www.yummyrecipesforme.com but the website failed to load, so tcpdump was used to capture network traffic.

---

## tcpdump Log Entry – DNS Request
13:24:32.192571 IP 192.51.100.15.52444 > 203.0.113.2.domain: 35084+ A? yummyrecipesforme.com. (24)

Explanation:
1. 13:24:32.192571 indicates the exact time the packet was captured.
2. IP shows the packet is using the Internet Protocol.
3. 192.51.100.15 is the source IP address of the client system.
4. 52444 is a temporary source port chosen by the client.
5. > shows the direction of traffic from client to server.
6. 203.0.113.2 is the destination IP address of the DNS server.
7. domain indicates DNS service using port 53.
8. 35084 is the DNS query identification number.
9. + means recursion is requested which is normal DNS behavior.
10. A? shows the client is requesting an A record.
11. yummyrecipesforme.com is the domain name being resolved.
12. (24) represents the size of the DNS request in bytes.

---

## tcpdump Log Entry – ICMP Error Response
13:24:36.098564 IP 203.0.113.2 > 192.51.100.15: ICMP 203.0.113.2 udp port 53 unreachable, length 254

Explanation:
1. 13:24:36.098564 indicates when the error response was captured.
2. IP shows the packet uses the Internet Protocol.
3. 203.0.113.2 is the source IP address of the DNS server.
4. 192.51.100.15 is the destination IP address of the client.
5. ICMP indicates an Internet Control Message Protocol error.
6. udp port 53 unreachable means the DNS service is not accessible on the server.
7. length 254 shows the size of the ICMP error message.

---

## What This Log Shows
1. DNS requests were sent from the client to the DNS server.
2. The DNS server responded with ICMP errors instead of DNS replies.
3. UDP port 53 was unreachable on the DNS server.
4. DNS resolution failed causing the website to be inaccessible.

---

## Key Learning Points
1. DNS uses UDP port 53 for name resolution.
2. ICMP is used to report network delivery errors.
3. Port unreachable errors usually indicate a stopped service or blocked port.
4. tcpdump helps identify exactly where communication fails.

---

Note: This tcpdump log is simulated training data created for learning and portfolio purposes.
