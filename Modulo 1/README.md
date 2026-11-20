# Ethical Hacking: Fundamentals and Methodologies

🌐 [English](README.md) | [Spanish](README.es.md) | [Go back](https://github.com/martinmorente-dev/Ethical-Hacker)

## What is ethical hacking?

An ethical hacker acts as an attacker to assess the security posture of a network or system and **minimize risk**. They use the same tools as a malicious attacker, but with **explicit permission** (the test's *scope*), and they report their findings to the client or vendor.

- **Ethical:** has permission and responsibly discloses vulnerabilities.
- **Unethical:** has malicious intent, gains unauthorized access, or publicly discloses a vulnerability without coordinating with the vendor.
- This process is known as **penetration testing (pentesting)**.

## Threat actors

| Actor | Motivation | Characteristics |
|---|---|---|
| **Organized crime** | Money | Well-funded groups using the latest techniques (ransomware, data theft). |
| **Hacktivists** | Ideological | Leak confidential data to embarrass or financially harm a target. |
| **State-sponsored** | Geopolitical | Cyber espionage and cyber warfare to steal information and cause disruption. |
| **Insider threats** | Varied | Employees tricked (e.g., phishing) or malicious insiders motivated by revenge or money. |

## Types of testing

- **Network infrastructure:** assesses the actual network, including wireless (bypassing security, breaking encryption, signal heat maps).
- **Application-based:** misconfigurations, input validation, injection, and logic flaws, aiming to reach the backend database. Key resource: **OWASP**.
- **Cloud:** governed by the **shared responsibility model** (varies across SaaS, PaaS, and IaaS). Contract details (SLAs, disaster recovery, encryption) must be defined, and each provider's testing policy reviewed.
- **Social engineering:** often out of scope because it tests people, not technology. The goal is to improve the awareness program, not to single out those who fail. Tool: **Social-Engineer Toolkit (SET)**, by Dave Kennedy.

## Testing perspectives

| Approach | Information given to the tester | Notes |
|---|---|---|
| **Black box** | Minimal, like an external attacker | Starts from public information. The defense team is sometimes not informed. |
| **White box** | Extensive: diagrams, IPs, configurations, credentials, source code | Aims to find as many vulnerabilities as possible. Broader scope. Recommended given today's adversaries. |
| **Gray box** | Partial: e.g., credentials without full documentation | Starts from a client machine and pivots laterally to measure impact. |

**Time and cost** usually determine which type of test is performed.

## Standards and methodologies

- **MITRE ATT&CK:** matrices of adversary tactics, techniques, and procedures (TTPs) (Enterprise, Network, Cloud, ICS, Mobile). Used by offensive teams, incident responders, and threat hunters.
- **OWASP WSTG:** web application security testing guide. Covers XSS, XXE, CSRF, and SQL injection, plus how to mitigate them.
- **NIST SP 800-115:** NIST guide for planning and conducting security tests. Replaced SP 800-42 and is an industry standard.
- **OSSTMM:** ISECOM manual (Pete Herzog) for repeatable, uniform security testing. Covers operational metrics, trust analysis, human, physical, wireless, telecom, and data network security, and produces the **STAR** report. Version 3, with version 4 in draft.
- **PTES:** seven phases:
  1. Pre-engagement interactions
  2. Intelligence gathering
  3. Threat modeling
  4. Vulnerability analysis
  5. Exploitation
  6. Post-exploitation
  7. Reporting
- **ISSAF:** information gathering → network mapping → vulnerability identification → penetration → gaining access and privilege escalation → further enumeration → compromising remote users/sites → maintaining access → covering tracks.

---

> ⚠️ **Disclaimer:** these notes are for educational purposes. Only test systems you own or have explicit written permission to assess.
