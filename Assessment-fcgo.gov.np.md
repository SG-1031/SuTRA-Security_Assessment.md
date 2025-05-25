# Passive Cybersecurity Assessment Report: [www.fcgo.gov.np](http://www.fcgo.gov.np)

## 1. Overview

This report provides a passive reconnaissance-based cybersecurity assessment of the Nepal government subdomain `www.fcgo.gov.np`, including DNS, SSL/TLS, security headers, public exposure, and basic threat intelligence.

---

## 2. Domain and WHOIS Information

* **Domain:** fcgo.gov.np
* **Subdomain:** [www.fcgo.gov.np](http://www.fcgo.gov.np)
* **Registrant:** National Information Technology Center (NITC), Government of Nepal
* **WHOIS:** Not publicly available for .gov.np domains

---

## 3. DNS Records

| Domain                                    | Record Type | Value                                                  |
| ----------------------------------------- | ----------- | ------------------------------------------------------ |
| [www.fcgo.gov.np](http://www.fcgo.gov.np) | A           | 103.69.124.8 *(redirects to Education Office)*         |
| fcgo.gov.np                               | A           | 202.45.146.235                                         |
| fcgo.gov.np                               | MX          | mx1.nepal.gov.np (priority 5)                          |
| fcgo.gov.np                               | MX          | mx2.nepal.gov.np (priority 10)                         |
| fcgo.gov.np                               | NS          | Azure DNS (ns1-37.azure-dns.com, etc.)                 |
| fcgo.gov.np                               | TXT         | v=spf1 mx a\:mx1.nepal.gov.np a\:mx2.nepal.gov.np -all |

---

## 4. SSL/TLS and Certificate

* Certificate: Sectigo Limited wildcard (expired April 16, 2025)
* No active public scan data available
* HTTPS may not be properly enforced if certificate is not renewed

---

## 5. HTTP Response and Security Headers ([www.fcgo.gov.np](http://www.fcgo.gov.np))

| Header        | Value                 |
| ------------- | --------------------- |
| Server        | Apache/2.4.6 (CentOS) |
| X-Powered-By  | PHP/7.3.26            |
| Cache-Control | no-cache, private     |

**Missing Security Headers:**

* Strict-Transport-Security
* X-Frame-Options
* Content-Security-Policy
* Referrer-Policy

---

## 6. Technology Stack

* Web Server: Apache 2.4.6 (CentOS)
* Backend: PHP 7.3.26, Laravel framework
* Frontend: Bootstrap, jQuery, Highcharts
* Tracking: Google Analytics

---

## 7. robots.txt and sitemap.xml

* No `robots.txt` or `sitemap.xml` discovered
* Search engines have full crawl access

---

## 8. Public File Exposure / Google Dorking

* No open directories or exposed sensitive files discovered
* Login required to access internal functions
* No misconfigured admin panels found via public search

---

## 9. Threat Intelligence and Vulnerabilities

* Domain not on any major blacklists
* No phishing/malware flags found (Google Safe Browsing)
* Potential risk from outdated PHP and Laravel (EOL / CVEs exist)

---

## 10. Additional Observations (User-Supplied DNS Results)

```
nslookup www.fcgo.gov.np
Server:  Unknown
Address: 192.168.110.1
Non-authoritative answer:
Name:    www.fcgo.gov.np
Address: 103.69.124.8
```

* `103.69.124.8` leads to an unrelated site (Education Development and Coordination Unit, Doti).

---

## 11. Recommendations

* Renew SSL/TLS certificate immediately
* Apply missing security headers (HSTS, CSP, etc.)
* Upgrade PHP and Laravel to supported versions
* Monitor DNS records for anomalies (e.g., redirection to other gov sites)
* Periodically validate IP resolution and geolocation
