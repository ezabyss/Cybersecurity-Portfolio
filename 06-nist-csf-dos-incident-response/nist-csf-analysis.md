# NIST Cybersecurity Framework (CSF) Analysis

This document maps the ICMP-based Denial of Service (DoS) incident to the five
core functions of the NIST Cybersecurity Framework (CSF). The goal is to show
how the incident was identified, mitigated, and used to improve the organization’s
security posture.

---

## 1. Identify

**Purpose:** Understand assets, risks, and vulnerabilities.

### Observations
- Internal network services were disrupted for approximately two hours.
- The firewall lacked ICMP filtering and rate-limiting rules.
- Network monitoring was insufficient to immediately detect abnormal ICMP traffic.

### Risks Identified
- Firewall misconfiguration allowed unrestricted ICMP traffic.
- Lack of visibility delayed detection of the DoS attack.

---

## 2. Protect

**Purpose:** Implement safeguards to limit or contain the impact of incidents.

### Controls Implemented
- Firewall rule added to limit incoming ICMP packet rates.
- IDS/IPS deployed to filter ICMP traffic based on suspicious patterns.
- Non-critical network services were taken offline during the incident.

### Security Benefit
These controls reduce the likelihood that excessive ICMP traffic can overwhelm
network resources and disrupt availability.

---

## 3. Detect

**Purpose:** Identify incidents quickly and efficiently.

### Detection Enhancements
- Network monitoring software deployed to track traffic volume and patterns.
- Firewall logging enabled for ICMP traffic.
- IDS/IPS alerts configured for abnormal ICMP activity.

### Security Benefit
Improved detection enables faster identification of DoS attacks, reducing downtime
and limiting business impact.

---

## 4. Respond

**Purpose:** Contain, analyze, and mitigate the incident.

### Response Actions
- Incoming ICMP traffic blocked at the firewall.
- Non-critical services stopped to stabilize the network.
- Critical services restored first to support business continuity.
- Network traffic and firewall logs analyzed to determine root cause.

### Security Benefit
These actions successfully contained the attack and prevented further disruption.

---

## 5. Recover

**Purpose:** Restore services and improve resilience.

### Recovery Activities
- Network services gradually restored to normal operation.
- Firewall configurations reviewed and hardened.
- Monitoring and IDS/IPS controls tested for effectiveness.
- Lessons learned documented for future incidents.

### Security Benefit
The organization returned to normal operations with stronger controls and improved
resilience against future DoS attacks.

---

## Conclusion

Applying the NIST Cybersecurity Framework provided a structured approach to managing
the ICMP flood DoS incident. By aligning actions to each CSF function, the organization
improved its ability to identify risks, protect assets, detect threats, respond
effectively, and recover quickly.
