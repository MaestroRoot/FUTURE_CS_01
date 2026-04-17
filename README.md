# 🔐 Website Vulnerability Assessment – Google Gruyere

## Task Name
**Vulnerability Assessment Report – Google Gruyere Web Application**


---
Target : https://google-gruyere.appspot.com/
## 📋 Project Overview

This project documents a **Grey-box Vulnerability Assessment** performed against [Google Gruyere](https://google-gruyere.appspot.com/), a deliberately vulnerable web application developed by Google for cybersecurity training and educational purposes.

The assessment was conducted to identify, analyze, and document exploitable security weaknesses within the application, evaluate their potential impact using the **DREAD risk rating framework**, and recommend practical remediation measures.

A total of **6 vulnerabilities** were identified — **4 rated High** and **2 rated Medium** — covering areas such as input handling, file upload functionality, HTTP response headers, session management, and client-side scripting behavior.

> ⚠️ **Disclaimer:** All testing was performed exclusively on an intentionally vulnerable application within an authorized, educational scope. No malicious, destructive, or unauthorized techniques were employed at any point.

---

## 🛠️ Tools & Environment

| Tool | Purpose |
|------|---------|
| **Kali Linux** | Testing environment / OS |
| **Nmap** | Service detection & vulnerability scanning |
| **OWASP ZAP** | Web application vulnerability scanning |
| **Burp Suite** | HTTP interception & vulnerability analysis |
| **SecurityHeaders.com** | HTTP security headers analysis |
| **Browser (Chrome)** | Manual testing & proof-of-concept validation |

---

## 🚨 Vulnerabilities Found

| # | Vulnerability | DREAD Score | Risk Rating |
|---|--------------|-------------|-------------|
| 1 | Information Disclosure (exposed `dump.gtl`) | 14/15 | 🔴 High |
| 2 | Stored XSS (Cross-Site Scripting) | 15/15 | 🔴 High |
| 3 | File Upload XSS (`hacked.html`) | 14/15 | 🔴 High |
| 4 | Absence of Security Headers | 13/15 | 🟡 Medium |
| 5 | Cross-Site Request Forgery (CSRF) | 13/15 | 🔴 High |
| 6 | AJAX-Based Client-Side Manipulation | 10/15 | 🟡 Medium |

### Risk Summary
- 🔴 **High:** 4 vulnerabilities
- 🟡 **Medium:** 2 vulnerabilities
- 🟢 **Low:** 0 vulnerabilities

---

## 📁 Repository Structure

```
📦 vulnerability-assessment-google-gruyere/
├── 📁 images/                               # Evidence & proof-of-concept screenshots
│   ├── ajax_manipulation.png                # AJAX client-side manipulation evidence
│   ├── csrf_burpsuite.png                   # CSRF endpoint intercepted via Burp Suite
│   ├── csrf_deletion_confirmed.png          # Confirmed snippet deletion via CSRF
│   ├── file_upload_xss_1.png                # Malicious HTML file upload success
│   ├── file_upload_xss_2.png                # Session cookie exposed via uploaded file
│   ├── hacked_html.png                      # Contents of the crafted hacked.html payload
│   ├── information_disclosure.png           # Exposed dump.gtl with plaintext credentials
│   ├── missing_security_headers.png         # SecurityHeaders.com scan showing missing headers
│   ├── security_headers.png                 # Full security headers scan result (Grade F)
│   ├── snippets_before_deletion.png         # All three snippets before CSRF deletion
│   ├── stored_xss.png                       # Stored XSS alert box execution
│   └── url_execution.png                    # Direct URL execution confirming CSRF
├── 📄 Vulnerability_assessment_report.pdf   # Full assessment report
└── vulnerability_assessment_report.md
└── 📄 README.md                             # This file
```

---

## ⚖️ Scope & Ethics

### ✅ Allowed
- Public-facing pages only
- Passive scanning
- Header checks
- Configuration analysis

### ❌ Not Allowed
- Login bypass
- Exploitation
- Brute force attacks
- Denial-of-Service (DoS)
- Any activity that can harm the website

> All activities conducted during this assessment strictly adhered to the above scope. Google Gruyere is a sandbox application intentionally built for security training, and all testing was performed responsibly within its educational boundaries.

---

## 👤 Author

**Samson Budigila**
Cybersecurity Student – Institute of Finance Management, Dar es Salaam, Tanzania

📧 [samsonbudigila6@gmail.com](mailto:samsonbudigila6@gmail.com)
📞 +255 757 502 743
🔗 [LinkedIn Profile](https://www.linkedin.com/in/samson-budigila)

---

## 📄 License

This project is intended for **educational purposes only**. All findings are confidential and must not be used for unauthorized or malicious activities.
