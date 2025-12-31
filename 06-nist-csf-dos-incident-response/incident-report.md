# Incident Report: ICMP Flood Denial of Service (DoS)

## Incident Summary
The organization experienced a denial of service (DoS) attack that disrupted
internal network operations for approximately two hours. The incident was caused
by a flood of ICMP packets entering the network through an unconfigured firewall.

## Incident Type
- Denial of Service (DoS)
- ICMP Flood / Ping Flood 

## Timeline
- Attack detected: Internal services became unavailable
- Response initiated: ICMP traffic blocked at firewall
- Mitigation: Non-critical services stopped
- Recovery: Critical services restored
- Resolution: Network returned to normal operation

## Impact
- Internal network services unavailable
- Employees unable to access resources
- Business operations temporarily disrupted

## Root Cause
The firewall lacked ICMP rate limiting and source verification, allowing
unrestricted ICMP traffic to overwhelm network resources.

## Mitigation Actions
- Blocked incoming ICMP traffic
- Implemented ICMP rate limiting
- Enabled source IP verification
- Deployed IDS/IPS and monitoring tools

## Current Status
The incident has been resolved. Network services are fully operational with
improved security controls in place.
