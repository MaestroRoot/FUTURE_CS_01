
Website Vulnerability Assessment – Google Gruyere
Task Name
Vulnerability Assessment Report – Google Gruyere Web Application

📋Overview
This project documents a Grey-box Vulnerability Assessment performed against Google Gruyere, a deliberately vulnerable web application developed by Google for cybersecurity training and educational purposes.
The assessment was conducted to identify, analyze, and document exploitable security weaknesses within the application, evaluate their potential impact using the DREAD risk rating framework, and recommend practical remediation measures.
A total of 6 vulnerabilities were identified — 4 rated High and 2 rated Medium — covering areas such as input handling, file upload functionality, HTTP response headers, session management, and client-side scripting behavior.

⚠️ Disclaimer:
 All testing was performed exclusively on an intentionally vulnerable application within an authorized, educational scope. No malicious, destructive, or unauthorized techniques were employed at any point.

🛠️ Tools & Environment
TOOL&ENVIRONMENT	 PURPOSE
Kali linux	Testing environment
Nmap 	Service detection & vulnerability scanning
Owasp zap	Application vulnerability scanning
Burp suite	HTTP interception& vulnerability analysis
Securityheaders.com	HTTP security headers analysis
Browser dev tools	Manual analysis and & POC



🚨 Vulnerabilities Found
	VULNERABILITY.	D	R	E	A	D	TOTAL	RATING
1	Information Disclosure	3	3	3	3	2	14	High
2	Stored XSS	3	3	3	3	3	15	High
3	File Upload XSS	3	3	3	3	2	14	High
4	Absence of Security Headers	2	3	2	3	3	13	Medium
5	Cross-Site Request Forgery (CSRF)	3	3	2	3	2	13	High
6	AJAX Client-Side Manipulation	2	2	2	2	2	10	Medium


📁 Repository Structure
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
└── 📄 README.md                             # This file

⚖️ Scope & Ethics
✅ Allowed
Public-facing pages only
Passive scanning
Header checks
Configuration analysis
❌ Not Allowed
Login bypass
Exploitation
Brute force attacks
Denial-of-Service (DoS)
Any activity that can harm the website

All activities conducted during this assessment strictly adhered to the above scope. Google Gruyere is a sandbox application intentionally built for security training, and all testing was performed responsibly within its educational boundaries.
👤 Author
Samson Budigila
Cybersecurity Student – Institute of Finance Management, Dar es Salaam, Tanzania
📧 samsonbudigila6@gmail.com
📞 +255 757 502 743
📄 License
This project is intended for educational purposes only. All findings are confidential and must not be used for unauthorized or malicious activities
