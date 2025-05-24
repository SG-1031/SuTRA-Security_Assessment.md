# Web Application Security Assessment Plan

## Target Application
**URL:** https://sutra.fcgo.gov.np/

## Objective
To perform a structured cybersecurity assessment of the public and authenticated components of the specified web-based application. The goal is to identify potential vulnerabilities and provide actionable recommendations.

## Legal Notice
This assessment must only be conducted with explicit permission. All activities will adhere to ethical guidelines and applicable laws.

---

## Assessment Phases

| Phase                       | Description                                                                | Tools/Notes                                             |
|-----------------------------|----------------------------------------------------------------------------|---------------------------------------------------------|
| 1. Preparation              | Define scope, ensure permission, and plan methodology                      | GitHub repo setup, documentation templates              |
| 2. Reconnaissance           | Gather technical and contextual information about the application          | WhatWeb, Wappalyzer, Nmap, DNSdumpster                  |
| 3. Threat Modeling          | Identify possible attack surfaces, inputs, and user roles                  | STRIDE, OWASP Threat Modeling Cheat Sheet               |
| 4. Vulnerability Scanning   | Scan for known issues using automated tools                                | Nikto, OWASP ZAP, Nuclei                                |
| 5. Manual Testing           | Validate scan results and test for logic flaws, injection, and auth issues | Burp Suite, Postman                                     |
| 6. Authentication Testing   | Evaluate login and session management                                      | Brute force resistance, session timeout, token handling |
| 7. Data Exposure Review     | Look for sensitive information leaks in requests/responses                 | Dev Tools, Burp Proxy, Mitmproxy                        |
| 8. HTTPS & Header Analysis  | Check TLS/SSL setup and HTTP security headers                              | SSL Labs, SecurityHeaders.com                           |
| 9. Reporting                | Document findings with evidence, severity ratings, and fixes               | Markdown reports, screenshots, logs                     |
| 10. Re-testing (if allowed) | Validate fixes for previously found vulnerabilities                        | Same tools and scripts reused                           |

---

## Deliverables
- `README.md`: Summary of the assessment project
- `findings.md`: Detailed list of identified issues
- `logs/`: Scanner and manual test outputs
- `scripts/`: Custom test scripts and payloads
- `screenshots/`: Screenshots as evidence of vulnerabilities
- `docs/`: Supporting documentation or references

---

## Methodology Standards
- OWASP Web Security Testing Guide (WSTG)
- OWASP Top 10
- CVSS v3.1 for risk scoring

---

## Notes
- All tests should avoid causing service disruption.
- Time-boxed testing to avoid prolonged impact.
- Document test dates and times clearly.
