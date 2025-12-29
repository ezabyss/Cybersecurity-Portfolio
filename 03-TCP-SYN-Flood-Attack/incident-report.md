# Cybersecurity Incident Report
## TCP SYN Flood Attack

### Section 1: Identify the type of attack that may have caused this network interruption

One potential explanation for the website’s connection timeout error message is that the web server was overwhelmed by an excessive number of incomplete TCP connection requests.

The logs show that a large number of TCP SYN packets were sent repeatedly from a single unfamiliar IP address to the web server on port 443. Many of these requests were not followed by completed TCP handshakes.

This event could be a TCP SYN flood attack, which is a form of denial-of-service (DoS) attack.

---

### Section 2: Explain how the attack is causing the website to malfunction

When a client attempts to connect to a web server, a TCP three-way handshake occurs:

1. The client sends a SYN packet to initiate a connection.
2. The server responds with a SYN-ACK packet and reserves system resources.
3. The client sends an ACK packet to complete the connection.

During a SYN flood attack, a malicious actor sends a large number of SYN packets but does not complete the handshake. The server allocates resources for each request and waits for responses that never arrive.

As a result, the server’s connection table fills up, preventing it from accepting legitimate connection requests. This causes connection timeouts and service unavailability for users attempting to access the website.
