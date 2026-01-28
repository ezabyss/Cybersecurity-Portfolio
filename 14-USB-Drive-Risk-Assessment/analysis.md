# USB Baiting Risk Analysis

## 1. Contents Analysis
The USB drive contains a mixture of personal and professional files, including family photos, pet images, resumes, employee schedules, and hiring documentation. These files may contain personally identifiable information (PII) and sensitive organizational data. Storing personal and work-related data on the same removable device increases the risk of unauthorized disclosure and misuse.

## 2. Attacker Mindset
From an attacker’s perspective, the information on the USB drive could be leveraged to conduct targeted phishing, impersonation, or social engineering attacks against hospital staff. 
Documents such as shift schedules and hiring letters provide insight into internal operations and employee roles. The USB device itself may have been intentionally planted to exploit human curiosity and establish an initial access vector.

## 3. Attack Vectors
Potential attack vectors include:
- USB baiting to deliver malicious software
- Social engineering using exposed personal and employee data
- Credential harvesting through infected documents
- Unauthorized system access via malware execution

Once the device is connected to a production or unmanaged system, multiple entry points may be established within the organization’s environment.

## 4. Risk Analysis
Malicious software such as ransomware, keyloggers, or remote access trojans could be concealed on the USB device. If connected to a production workstation, the device could lead to data breaches, loss of system integrity, or disruption of hospital operations. Even in the absence of malware, exposed files could enable future targeted attacks, impacting confidentiality, integrity, and availability (CIA triad).

## 5. Mitigation and Security Controls
Recommended controls include:
- Disabling USB autorun functionality
- Enforcing removable media usage policies
- Conducting employee security awareness training
- Separating personal and business storage devices
- Using virtualization or sandboxing for device inspection
- Implementing centralized monitoring and incident reporting procedures

These controls align with defense-in-depth and least privilege principles.

## 6. Incident Response Guidance: Found USB Devices
If an unknown USB drive is discovered on organizational property, it should be treated as a potential security incident. Employees should be instructed not to insert the device into any workstation or personal system and to report it immediately to the security or IT team.

Security teams should analyze the device only within a sandboxed or virtualized environment disconnected from production networks. The device should be scanned using up-to-date detection tools, and any indicators of compromise (IOCs) should be documented and investigated. Clear procedures help reduce the likelihood and impact of USB baiting attacks.
