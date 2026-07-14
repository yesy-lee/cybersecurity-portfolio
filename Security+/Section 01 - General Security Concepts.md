# Section 01 - General Security Concepts

## Learning Objectives

After completing this section, I should be able to:

- Explain the core principles of information security.
- Understand the CIA Triad.
- Explain Authentication, Authorization, and Accounting (AAA).
- Understand Non-repudiation.
- Perform a basic Gap Analysis.
- Explain the Zero Trust security model.
- Relate these concepts to the responsibilities of a SOC Analyst.

---

# 1. Security Concepts

## Definition

Information security is the practice of protecting systems, networks, applications, and data from unauthorized access, modification, disclosure, or disruption.

The primary objective is to reduce risk while maintaining business operations.

---

## Why It Matters

Every security technology exists to protect information and reduce cyber risk.

Whether using a firewall, antivirus, encryption, or MFA, the goal is always to improve security while supporting business needs.

---

## SOC Analyst Perspective

When investigating an incident, a SOC Analyst should ask:

- What asset is affected?
- What happened?
- How serious is the impact?
- Which security objective is affected?

---

# 2. CIA Triad

The CIA Triad is the foundation of information security.

| Principle | Description | Examples | Threats |
|------------|-------------|----------|----------|
| Confidentiality | Protect data from unauthorized access | Encryption, MFA, VPN | Data Breach, Credential Theft |
| Integrity | Ensure data remains accurate and unchanged | Hashing, Digital Signatures | Malware, Log Tampering |
| Availability | Ensure systems remain accessible | Backups, Redundancy | DDoS, Ransomware |

---

## SOC Example

| Incident | CIA Component |
|-----------|---------------|
| Phishing steals passwords | Confidentiality |
| Malware changes financial records | Integrity |
| Ransomware encrypts servers | Availability |

---

# 3. AAA

AAA stands for:

## Authentication

Who are you?

Examples:

- Password
- MFA
- Biometrics
- Smart Card

---

## Authorization

What are you allowed to access?

Examples:

- Administrator
- Standard User
- Read Only

---

## Accounting

What did you do?

Examples:

- Windows Event Logs
- Audit Logs
- SIEM Logs

---

## SOC Example

A user logs into Microsoft 365.

Authentication

↓

User identity is verified.

↓

Authorization

↓

The user is allowed to access SharePoint.

↓

Accounting

↓

The login activity is recorded inside Microsoft Sentinel.

---

# 4. Non-repudiation

## Definition

Non-repudiation ensures that someone cannot deny performing an action.

---

## Technologies

- Digital Signatures
- PKI
- Certificates
- Email Signing

---

## Real-world Example

An employee digitally signs an important contract.

Later, they cannot claim they never signed it because the digital signature proves authenticity.

---

## SOC Relevance

SOC analysts often verify whether actions were genuinely performed by specific users using digital signatures and audit logs.

---

# 5. Gap Analysis

## Definition

Gap Analysis compares the current security posture with the desired security posture.

---

## Example

Current State

- Password only

Desired State

- Multi-Factor Authentication

Gap

- MFA has not been implemented.

Recommendation

- Deploy MFA for all users.

---

## Why SOC Analysts Care

Gap Analysis helps identify security weaknesses before attackers exploit them.

---

# 6. Zero Trust

## Principle

Never Trust.

Always Verify.

---

## Core Concepts

- Verify every identity.
- Verify every device.
- Grant least privilege.
- Continuously monitor activity.

---

## Example

An employee logs in from Sydney.

Five minutes later another login appears from Russia.

Zero Trust triggers additional verification or blocks access.

---

## Why It Matters

Modern attacks frequently involve stolen credentials.

Even authenticated users should not automatically be trusted.

---

# Summary

## Key Takeaways

- Information security focuses on reducing risk.
- CIA Triad is the foundation of cybersecurity.
- AAA controls identity, permissions, and auditing.
- Non-repudiation provides proof of actions.
- Gap Analysis identifies security improvements.
- Zero Trust assumes no implicit trust.

---

# Security+ Exam Notes

Remember:

- Encryption → Confidentiality
- Hashing → Integrity
- Backups → Availability

Authentication → Authorization → Accounting

Zero Trust = Never Trust, Always Verify

Digital Signature = Non-repudiation

Gap Analysis = Current State vs Desired State

---

# SOC Interview Questions

### What is the CIA Triad?

### Explain the difference between Authentication and Authorization.

### Why is Zero Trust important in modern organizations?

### Give an example of Non-repudiation.

### What is the purpose of a Gap Analysis?
