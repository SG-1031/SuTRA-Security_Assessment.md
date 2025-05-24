# Cybersecurity Assessment Plan: sutra.fcgo.gov.np

## Project Overview

**Target:** [https://sutra.fcgo.gov.np](https://sutra.fcgo.gov.np)  
**Type:** Web-based government application  
**Assessor:** Subash Gurung  
**Purpose:** To evaluate the security posture of the target application using only publicly available information and accessible components, without attempting intrusive or authenticated testing.

## Scope

- Public-facing web pages and resources only  
- No authenticated or restricted access testing  
- No vulnerability exploitation or intrusive scanning (e.g., no brute force, no injection attempts)  
- Information gathering through open-source intelligence (OSINT) and passive analysis  
- Security configuration review (headers, SSL/TLS) via non-intrusive tools

## Tools & Environment

- **Reconnaissance & Information Gathering:** Nmap (non-intrusive), WhatWeb, BuiltWith, Shodan, Dig  
- **Security Configuration:** SSL Labs, SecurityHeaders.com  
- **Passive Analysis:** Browser Developer Tools, online scanners  
- **Documentation:** Markdown files, screenshots, logs

---

## Step-by-Step Assessment Plan

| Phase | Description | Tools/Techniques | Output |
|-------|-------------|------------------|--------|
| Preparation | Define goals, confirm scope limited to public info | Documentation, risk policy | Clear scope documentation |
| Reconnaissance | Collect open-source info: domains, IPs, tech stack | WhatWeb, BuiltWith, Shodan, Dig | List of technologies and endpoints |
| Passive Security Analysis | Analyze HTTPS setup, security headers | SSL Labs, SecurityHeaders.com | SSL/TLS and header configuration report |
| Content Analysis | Review publicly available content and files | Browser Dev Tools, manual inspection | Summary of publicly exposed data |
| Vulnerability Research | Research known vulnerabilities related to identified tech | CVE databases, NVD, vendor advisories | List of potential risks |
| Reporting | Document findings, risks, and remediation advice | Markdown report, screenshots | `findings.md` and final report |

---

## References

- [OWASP Top 10](https://owasp.org/www-project-top-ten/)  
- [OWASP Testing Guide - Passive Testing](https://owasp.org/www-project-web-security-testing-guide/latest/4-Web_Application_Security_Testing/01-Information_Gathering)  
- [SSL Labs Test](https://www.ssllabs.com/ssltest/)  
- [Security Headers](https://securityheaders.com/)  
- [National Vulnerability Database (NVD)](https://nvd.nist.gov/)

---

## Disclaimer

This assessment uses only publicly available information and does not involve intrusive or unauthorized testing. It complies with ethical guidelines and legal requirements.


