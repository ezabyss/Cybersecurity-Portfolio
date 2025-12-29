# Wireshark TCP SYN Flood Log Explanation

This file explains how a TCP SYN flood attack appears in a Wireshark capture.

Log Entry:
203.0.113.0 -> 192.0.2.1 TCP [SYN]

Explanation:
The source IP repeatedly sends SYN packets to the web server, attempting to initiate TCP connections.

Log Entry:
192.0.2.1 -> 203.0.113.0 TCP [SYN, ACK]

Explanation:
The web server responds and allocates resources for the connection.

Issue Observed:
The attacker does not send the final ACK packet, leaving the connection half-open.

Impact:
Many half-open connections consume server resources, preventing legitimate users from establishing connections and causing timeout errors.
