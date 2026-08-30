# OWASP Juice Shop Web Application Penetration Test

## Overview

This project documents a comprehensive web application penetration testing assessment performed against a locally deployed **OWASP Juice Shop** environment.

The objective was to follow a structured penetration testing workflow to identify, validate, prioritize, and document security vulnerabilities while also evaluating their potential impact, detection opportunities, and recommended remediation.

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
