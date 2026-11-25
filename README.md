# 🔐 Web Application Penetration Testing Assessment


This repository contains the full methodology, technical walkthrough, vulnerability analysis, and proof-of-concept evidence for an authorized Black-Box Web Application Penetration Test conducted on the Mediroza General Hospital patient portal.

## Executive Summary

As part of the **NETWORKWALKS Cybersecurity Training (Batch B084 – Week 4)**, an end-to-end security assessment was performed against the Mediroza General Hospital web infrastructure.

The primary goal was to evaluate the application's attack surface, identify authentication weaknesses, analyse PDF document encryption, examine hidden file metadata, and identify critical database exposures.

## Assessment Objectives

- **Reconnaissance:** Discover hidden endpoints and restricted directories through robots.txt.
- **Authentication Testing:** Identify username enumeration and SQL Injection vulnerabilities.
- **Document Security Analysis:** Evaluate PDF encryption and password strength.
- **Deep Reconnaissance:** Analyse file metadata and identify exposed database backups.
- **Risk Reporting:** Document vulnerabilities with severity ratings and remediation recommendations.

## Technical Methodology

### Phase 1: Reconnaissance & Initial Access

1. Endpoint Discovery via robots.txt
2. Username Enumeration Vulnerability
3. SQL Injection Login Bypass

### Phase 2: PDF Encryption & Hash Recovery

1. Report 1 Password Recovery
2. Report 2 Password Recovery
3. Report 3 Password Recovery (Extended Dictionary Attack)

### Phase 3: Deep Reconnaissance & Exploit Chaining

1. PDF Decryption using qpdf
2. Metadata Extraction using ExifTool
3. Directory Listing Analysis
4. Database Backup Exposure
5. Confidential Data Disclosure

## Key Vulnerabilities & Risk Summary

| Finding ID | Vulnerability | Severity |
|---|---|---|
| VULN-01 | SQL Injection (Authentication Bypass) | CRITICAL |
| VULN-02 | Unrestricted Backup Exposure & Directory Listing | CRITICAL |
| VULN-03 | Plaintext Confidential Data Disclosure | CRITICAL |
| VULN-04 | Weak PDF Document Encryption | HIGH |
| VULN-05 | Sensitive Metadata Leakage in Distributable PDFs | MEDIUM |
| VULN-06 | Inconsistent Authentication Error (User Enumeration) | MEDIUM |

## Remediation & Security Recommendations

- **Parameterized Queries:** Use prepared statements (PDO or mysqli prepared statements).
- **Disable Directory Browsing:** Disable directory listing using `Options -Indexes` in Apache.
- **Generic Error Messages:** Standardize authentication responses.
- **Metadata Sanitization:** Use ExifTool to remove unnecessary document metadata.
- **Secure Storage:** Store database backups outside the public web root.

## Tools & Technologies Used

| Category | Tools |
|---|---|
| Web Assessment | Browser Developer Tools, cURL, Burp Suite |
| Password Cracking | NETWORKWALKS Hash Calculator & Cracker, John the Ripper (JTR) |
| File Analysis & Decryption | ExifTool, qpdf, wget |

## Assessment Information

| Item | Details |
|---|---|
| Training Programme | NETWORKWALKS Cybersecurity Career Track |
| Batch | B084 |
| Assessment | Week 4 |
| Assessment Type | Black-Box Web Application Penetration Testing |
| Lead Mentor | Sir Waqas Karim (CCIE) |
| Author | Anas Askhan |

## Report & Evidence

The complete penetration testing report, including technical walkthroughs, screenshots, vulnerability analysis, and proof-of-concept evidence, is available in this repository.

**Report:** `Penetration-Report.pdf`

## Legal Notice & Educational Scope

This repository is maintained exclusively for academic, research, and professional portfolio demonstration.

All security tests, vulnerability disclosures, and dynamic attacks demonstrated herein were executed inside an authorized sandbox environment operated by NETWORKWALKS.

Applying these assessment techniques against production assets or unauthorized endpoints without formal permission is strictly prohibited.

---

**Anas Askhan**  
Cybersecurity Student  
NETWORKWALKS Cybersecurity Career Track
