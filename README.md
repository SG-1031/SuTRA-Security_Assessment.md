# SuTRA Web Application Security Assessment

## Target
**Application URL:** https://sutra.fcgo.gov.np/

## Assessor
**Name:** Subash Gurung  
**Role:** Cybersecurity Analyst  
**Date:** 2025-05-24

---

## Project Structure

```
repo/
├── README.md              # Project overview
├── findings.md            # Documented vulnerabilities and issues
├── logs/                  # Scanner and manual test logs
├── screenshots/           # Visual evidence of findings
├── scripts/               # Custom payloads or automation scripts
└── docs/                  # Additional resources or references
```

---

## README.md (Contents)

### Web Application Security Assessment

This repository contains a security assessment of the government web-based application at [https://sutra.fcgo.gov.np](https://sutra.fcgo.gov.np/). It includes the methodology, tools used, findings, and recommendations.

### Objectives
- Identify potential security vulnerabilities
- Analyze risk impact and likelihood
- Provide actionable remediation suggestions

### Scope
- Public endpoints and login forms
- Basic authenticated sections (with permission)

### Methodology
- Reconnaissance
- Threat modeling
- Automated scanning
- Manual testing
- Reporting and recommendations

### Tools Used
- Nmap, WhatWeb, Nikto
- OWASP ZAP, Burp Suite
- Postman, SSL Labs, SecurityHeaders

### Legal Disclaimer
Assessment conducted under educational and ethical guidelines. No unauthorized access or harm was intended.

---

## findings.md (Initial Content)

# Security Findings Summary

| ID | Category       | Vulnerability          | Risk   | Status             |
|----|----------------|------------------------|--------|--------------------|
| 1  | Authentication | Weak login mechanism   | Medium | Pending validation |
| 2  | Injection      | Possible SQL Injection | High   | In progress        |

---

## logs/, screenshots/, scripts/, docs/
- Use these folders to store output from tools like Burp, ZAP, or screenshots of issues.
- Scripts can include fuzzing payloads or automation helpers.
- Docs can hold references to CVEs, OWASP docs, etc.
