# PASTA Threat Modeling Analysis – Sneaker Marketplace App

---

## I. Define Business & Security Objectives

- Enable users to securely buy and sell sneakers through a mobile platform
- Process financial transactions quickly and reliably
- Protect sensitive user data, including credentials and payment information
- Maintain compliance with financial and privacy regulations (e.g., PCI-DSS)

Security is a core business requirement, as loss of trust or data breaches could directly impact revenue, reputation, and legal standing.

---

## II. Define the Technical Scope

**Technologies in Use:**
- Application Programming Interface (API)
- Public Key Infrastructure (PKI)
- AES & RSA encryption
- SHA-256 hashing
- SQL databases

**Priority Technology: API**

APIs were prioritized because they handle authentication, payments, messaging, and data exchange between users and backend services. APIs significantly expand the attack surface and are common targets for injection attacks, broken authentication, and token abuse.

---

## III. Decompose the Application (Data Flow)

**Primary Process:** Product Search & Purchase  
- User submits search query
- API processes request
- Database returns inventory listings
- User initiates purchase
- Payment data encrypted and transmitted
- Transaction stored in database

This process involves multiple trust boundaries and sensitive data flows.

---

## IV. Threat Analysis

**Identified Threats:**
1. Injection attacks targeting API or SQL queries
2. Session hijacking through stolen or weak authentication tokens

These threats could allow unauthorized access to user accounts or financial data.

---

## V. Vulnerability Analysis

**Potential Vulnerabilities:**
1. Lack of prepared SQL statements (SQL Injection risk)
2. Broken or improperly scoped API authentication tokens

These weaknesses could be exploited to manipulate data or escalate privileges.

---

## VI. Attack Modeling (Attack Tree)

**Primary Asset:** User Data  
- SQL Injection → Lack of prepared statements  
- Session Hijacking → Weak login credentials or token handling  

This model demonstrates how multiple vulnerabilities can lead to the same high-impact outcome.

---

## VII. Risk Analysis & Security Controls

**Recommended Security Controls:**
1. Strong password policies and credential hashing (SHA-256 + salting)
2. Principle of least privilege for APIs and database access
3. Secure token management with expiration and rotation
4. Incident response procedures for rapid containment

These controls reduce both the likelihood and impact of successful attacks.

---

## 🏁 Conclusion

This PASTA-based assessment demonstrates how threat modeling helps identify security risks early in the development lifecycle. By aligning business objectives with technical security controls, organizations can reduce exposure, protect user trust, and prevent costly incidents before launch.

---

✍️ Notes By Abhishek (Ez Abyss)
