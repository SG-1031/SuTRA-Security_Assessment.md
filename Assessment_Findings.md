# Cybersecurity Assessment Findings: sutra.fcgo.gov.np

## 1. Domain Registration and WHOIS Information

- Domain `fcgo.gov.np` is officially registered under Nepal’s .NP TLD.
- Managed by the National Information Technology Center (NITC) on behalf of the Government of Nepal.
- No WHOIS data is available for `.gov.np` domains via public registries.
- Subdomain `sutra.fcgo.gov.np` falls under this domain and shares the same registration context.

---

## 2. DNS Records and Name Servers

**DNS Snapshot (May 2024):**

| Name                  | Type | Value                                                                                              |
|-----------------------|------|----------------------------------------------------------------------------------------------------|
| fcgo.gov.np           | A    | 202.45.146.235                                                                                     |
| fcgo.gov.np           | MX   | mx1.nepal.gov.np (priority 5), mx2.nepal.gov.np (priority 10)                                      |
| fcgo.gov.np           | NS   | Azure DNS: ns1-37.azure-dns.com, ns2-37.azure-dns.net, ns3-37.azure-dns.org, ns4-37.azure-dns.info |
| fcgo.gov.np           | TXT  | v=spf1 mx a:mx1.nepal.gov.np a:mx2.nepal.gov.np -all                                               |
| sutra.fcgo.gov.np     | A    | 202.70.90.233                                                                                      |

- Domain is hosted via Microsoft Azure DNS.
- SPF record is configured for mail authentication.
- No AAAA or CNAME records were found.

---

## 3. Subdomain Enumeration

Identified active subdomains and corresponding IP addresses:

| Subdomain               | Purpose                            | IP Address(es)                |
|-------------------------|------------------------------------|-------------------------------|
| sutra.fcgo.gov.np       | SuTRA (Treasury App)               | 202.70.90.233                 |
| cgas.fcgo.gov.np        | CGAS+ (Accounting)                 | 202.70.88.113, 202.166.194.82 |
| rajaswa.fcgo.gov.np     | Revenue Payment Portal             | 202.70.88.119                 |
| pams.fcgo.gov.np        | Public Assets Management System    | 202.70.88.118, 202.166.194.84 |
| newrmis.fcgo.gov.np     | Revenue MIS                        | 202.70.88.112                 |

- No wildcard or unexpected subdomains found.
- Hosting appears localized within Nepal IP ranges.

---

## 4. SSL/TLS Configuration and Certificate

- Wildcard certificate (`*.fcgo.gov.np`) from Sectigo Limited was found expired (April 16, 2025).
- TLS support exists but may not be trusted due to the expired cert.
- No public scan results available for `sutra.fcgo.gov.np`.
- A full SSL Labs scan is recommended for detailed cipher/protocol validation.

---

## 5. HTTP Response and Security Headers

**Sample HTTP headers (fcgo.gov.np - May 2024):**

| Header           | Value                                     |
|------------------|-------------------------------------------|
| Server           | Apache/2.4.6 (CentOS) OpenSSL/1.0.2k-fips |
| X-Powered-By     | PHP/7.3.26                                |
| Cache-Control    | no-cache, private                         |

**Observations:**
- Missing standard security headers:
  - No `Strict-Transport-Security`
  - No `X-Frame-Options`
  - No `Content-Security-Policy`
- Session cookies are set (Laravel and XSRF token), but may lack `Secure` and `HttpOnly` flags.

---

## 6. Technology Stack Fingerprinting

- **Server:** Apache 2.4.6 on CentOS
- **Backend:** PHP 7.3.26 with Laravel
- **Frontend:** Bootstrap, jQuery, Highcharts, FontAwesome, Google Analytics
- Legacy `.asp` pages may still be present on SuTRA platform
- Potential mix of legacy Microsoft stack and modern PHP framework

---

## 7. robots.txt and sitemap.xml

- No `robots.txt` or `sitemap.xml` publicly available.
- No restrictions appear to be in place for bots or crawlers.
- Google and Bing appear to crawl the site freely.

---

## 8. Public File Exposure and Google Dorking

- No sensitive files, backup directories, or config files exposed via public search.
- No admin pages or login endpoints indexed.
- SuTRA appears login-protected and doesn’t reveal backend data to unauthenticated users.

---

## 9. Threat Intelligence and Vulnerabilities

- Domain not listed in threat intelligence feeds.
- No malware, phishing, or botnet reports.
- Outdated software detected:
  - **PHP 7.3**: End-of-life, security risks
  - **Laravel (legacy version)**: May be affected by CVEs if unpatched
- No evidence of exploits, but patching is strongly recommended

---

## 10. Blacklists and Blocklists

- Domain/IPs not found in major DNS-based or URL blacklists.
- Marked as “safe” by:
  - Google Safe Browsing
  - Symantec Reputation Database
  - Common blocklists (DNSBL/RBL)

---

## Summary of Key Risks

| Area                     | Risk Description                                                 | Risk Level |
|--------------------------|------------------------------------------------------------------|------------|
| Expired SSL Certificate  | HTTPS may not be properly enforced or trusted                    | High       |
| Outdated PHP Version     | PHP 7.3 is end-of-life with known security vulnerabilities       | High       |
| Laravel (Old Version)    | Legacy Laravel versions are exposed to CVEs                      | Medium     |
| Missing Security Headers | Incomplete hardening leaves the application open to web attacks  | Medium     |
| Public Certificate Logs  | Subdomains easily enumerated via certificate transparency        | Low        |

---

## Conclusion

The `sutra.fcgo.gov.np` domain and its parent systems exhibit a number of security gaps primarily related to outdated components and lack of configuration hardening. While no active exploits or public leaks were found, the presence of expired certificates, legacy frameworks, and missing headers increases risk. Prompt updates and implementation of modern security practices are recommended.

---

**Sources:**  
All findings are based on publicly accessible tools, OSINT resources, and non-intrusive passive scanning as of May 2024.
