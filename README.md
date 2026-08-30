# OWASP Juice Shop Web Application Penetration Test

## Overview

This project documents a comprehensive web application penetration testing assessment performed against a locally deployed **OWASP Juice Shop** environment.

The objective was to follow a structured penetration testing workflow to identify, validate, prioritize, and document security vulnerabilities while evaluating their potential impact, detection opportunities, and recommended remediation.

All testing was performed in an isolated and authorized local Docker environment.

---

## Assessment Scope

**Target:** OWASP Juice Shop  
**Environment:** Local Docker deployment  
**Testing Type:** Web Application Penetration Testing  
**Risk Framework:** OWASP Top 10 (2021) and CVSS-based prioritization

The assessment included:

- Environment verification
- Reconnaissance and technology fingerprinting
- Port and service enumeration
- HTTP header analysis
- API endpoint enumeration
- Client-side application analysis
- Vulnerability identification
- Controlled exploitation
- Post-exploitation impact analysis
- Detection and logging analysis
- Remediation planning
- Retest criteria

---

## Methodology

The assessment followed a structured seven-stage workflow:

```text
Environment Verification
        ↓
Reconnaissance
        ↓
Scanning & Enumeration
        ↓
Vulnerability Assessment
        ↓
Controlled Exploitation
        ↓
Impact & Detection Analysis
        ↓
Reporting & Remediation
```

---

## Key Findings

| ID | Finding | Severity | CVSS |
|---|---|---|---:|
| F01 | SQL Injection – Authentication Bypass | Critical | 9.8 |
| F02 | Broken Access Control – Administrative Access | Critical | 9.1 |
| F03 | DOM-Based Cross-Site Scripting (XSS) | High | 8.2 |
| F04 | Public File Directory / Developer Artifact Exposure | High | 7.5 |
| F05 | Confidential Document Exposure | High | 7.5 |
| F06 | Poison Null Byte File Access Bypass | High | 7.2 |
| F07 | Unauthenticated Metrics Endpoint | Medium | 6.5 |
| F08 | Verbose Error Handling | Medium | 5.3 |

---

## Attack Chain

A key attack path demonstrated during the assessment was:

```text
SQL Injection
      ↓
Authentication Bypass
      ↓
Administrator Session
      ↓
Privileged Application Access
      ↓
Exposure of Sensitive Functionality
```

Additional weaknesses independently exposed internal files, developer artifacts, runtime metrics, and application information.

---

## Tools & Technologies

- Docker
- Nmap / Zenmap
- Chrome Developer Tools
- Manual HTTP request analysis
- OWASP Juice Shop
- OWASP Top 10
- CVSS
- NIST National Vulnerability Database
- MITRE CVE
- GitHub Security Advisories

---

## Skills Demonstrated

- Web application penetration testing
- Reconnaissance and enumeration
- Technology fingerprinting
- Attack-surface analysis
- Port and service scanning
- HTTP security analysis
- API endpoint enumeration
- Client-side application analysis
- SQL injection testing
- Cross-site scripting testing
- Authentication and authorization testing
- Broken access control analysis
- Sensitive information exposure analysis
- Security misconfiguration assessment
- CVSS risk prioritization
- OWASP Top 10 mapping
- Controlled exploitation
- Post-exploitation impact analysis
- Attack-chain analysis
- Security logging and detection analysis
- Remediation planning
- Retest planning
- Technical security reporting

---

## Detection & Defensive Analysis

The assessment also examined how the demonstrated attacks could be identified using defensive security controls.

Detection opportunities included:

- SQL injection patterns in authentication requests
- Encoded null-byte sequences in URLs
- Repeated HTTP 500 responses
- Unauthenticated access to monitoring endpoints
- Enumeration of sensitive directories
- Suspicious privileged sessions following abnormal authentication activity
- Centralized web and application log monitoring

This provides a connection between offensive security testing and defensive concepts such as **SIEM monitoring, alerting, and detection engineering**.

---

## Remediation Focus

The highest-priority remediation areas included:

- Implementing parameterized database queries
- Enforcing server-side authorization
- Applying secure output encoding and XSS protections
- Removing publicly accessible backup and internal files
- Restricting monitoring endpoints
- Validating encoded file-path input
- Suppressing verbose production errors
- Implementing appropriate HTTP security headers
- Maintaining dependency patching and vulnerability management
- Centralizing security logging and alerting

---

## Full Penetration Testing Report

The complete report contains detailed methodology, technical findings, screenshots, supporting evidence, vulnerability analysis, impact assessments, detection opportunities, remediation recommendations, and retest criteria.

**[View the Full Penetration Testing Report](./OWASP_Juice_Shop_Penetration_Test_Report_Professional.pdf)**

---

## Ethical Testing Notice

All security testing documented in this project was performed against a **locally hosted, intentionally vulnerable OWASP Juice Shop instance** in an isolated and authorized laboratory environment.

No public, production, or third-party systems were scanned or exploited.

---

## References

- OWASP Juice Shop
- OWASP Top 10
- OWASP Cheat Sheet Series
- NIST National Vulnerability Database (NVD)
- MITRE CVE
- GitHub Security Advisories
