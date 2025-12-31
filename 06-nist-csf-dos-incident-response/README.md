# NIST CSF–Based Incident Response: DoS Attack Analysis

## Overview
This project documents a cybersecurity incident response analysis using the
National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF).

The incident involved a Denial of Service (DoS) attack caused by a flood of ICMP
packets that disrupted internal network services for approximately two hours.

## Scenario Summary
A malicious actor exploited an unconfigured firewall to send excessive ICMP
traffic into the network, overwhelming resources and preventing normal
operations. The incident was mitigated by blocking ICMP traffic, restoring
critical services, and implementing additional security controls.

## Framework Used
- NIST Cybersecurity Framework (CSF)
  - Identify
  - Protect
  - Detect
  - Respond
  - Recover

## Project Contents
- `incident-report-nist-csf.md` – Full incident report aligned to NIST CSF
- `nist-csf-overview.md` – Beginner-friendly explanation of NIST CSF
- `lessons-learned.md` – Security improvements and takeaways

## Skills
- Incident response documentation
- Network security analysis
- Denial of Service (DoS) mitigation
- Firewall hardening and monitoring
- Applying NIST CSF to real-world incidents
