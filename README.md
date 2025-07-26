# Infotact Solutions –  Cybersecurity Projects

This repository contains **three enterprise-level cybersecurity projects** completed as part of practical training and portfolio development. The projects cover **network vulnerability assessment, web application penetration testing (OWASP Top 10), and secure Linux server setup & hardening**. Each project simulates real-world enterprise environments with **professional documentation, scanning reports, and remediation strategies**.

---

## Projects Overview

1. **Basic Vulnerability Assessment for a Small Business Network**
2. **Web Application Penetration Testing – OWASP Top 10 (DVWA)**
3. **Secure Linux Server Setup & Hardening – CIS Benchmark Compliance**

---

## 1. Project 1 – Basic Vulnerability Assessment

### **Problem Statement**

Simulate a real-world **vulnerability assessment** for a small business IT infrastructure. Identify security gaps, prioritize risks, and provide **mitigation strategies** to improve the security posture.

### **Key Steps Completed**

* Set up **VirtualBox lab** with Kali Linux, Metasploitable2, and OWASP Juice Shop.
* Conducted **network enumeration** and **port scanning** using Nmap.
* Performed vulnerability scans using **OpenVAS (Greenbone Vulnerability Manager)**.
* Mapped vulnerabilities to **CVSS scores** and prioritized risks.
* Developed **mitigation recommendations** for high/critical findings.
* Created a **professional report** with network map, vulnerabilities, and fixes.

### **Tools Used**

* **Kali Linux, Nmap, OpenVAS**
* VirtualBox for network simulation

**Deliverables:**

* **Vulnerability Assessment Report (PDF)**
  Comprehensive document detailing network architecture, identified vulnerabilities (via Nmap & OpenVAS), CVSS scoring, and mitigation steps.
* **OpenVAS Raw Scan Report (PDF)**
  Unfiltered output for audit validation.
* **PowerPoint Presentation (PPTX)**
  Executive summary with key findings, prioritized risks, and remediation roadmap.


---

## 2. Project 2 – Web Application Penetration Testing (DVWA)

### **Problem Statement**

Perform a **penetration test** on DVWA (Damn Vulnerable Web Application) focusing on **OWASP Top 10 vulnerabilities**, simulate real-world web attacks, and provide remediation.

### **Key Steps Completed**

* Set up DVWA in **local lab environment**.
* Recon and spidering using **Burp Suite**.
* Performed manual **SQL Injection**, **Command Injection**, **XSS (Reflected/Stored)**.
* Conducted **Brute Force attack** using Burp Intruder.
* Tested for **CSRF, Sensitive Data Exposure, Broken Access Control, Security Misconfiguration**.
* Collected **proof-of-concept screenshots** for all exploits.
* Provided remediation aligned with **secure coding best practices**.

### **Exploited Vulnerabilities**

* **SQL Injection** – Full DB dump using `' OR '1'='1--`
* **Command Injection** – Executed `127.0.0.1|pwd` revealing system paths
* **XSS (Reflected & Stored)** – `<script>alert('XSS')</script>` PoCs
* **Brute Force** – Password guessing via Burp Intruder
* **Sensitive Data Exposure** – Credentials in plaintext HTTP

### **Tools Used**

* **DVWA, Burp Suite, Firefox, Manual Payloads**

**Deliverables:**

* **Penetration Test Report (PDF)**
  Detailed exploitation steps of DVWA vulnerabilities (SQLi, XSS, Command Injection, Brute Force, CSRF, etc.) mapped to OWASP Top 10.
* **Proof-of-Concept Screenshots (embedded in report)**
  Exploitation evidence with payloads and responses.
* **PowerPoint Presentation (PPTX)**
  Summarized test methodology, findings, and remediation strategies for stakeholders.

---

## 3. Project 3 – Secure Linux Server Setup & Hardening

### **Problem Statement**

Deploy and harden an **Ubuntu Server 20.04 LTS** to meet **CIS Benchmark v3.0.0** recommendations. Secure it against common attacks using **firewall, auditing, PAM, SSH hardening, and kernel tuning**.

### **Key Steps Completed**

* **Deployed Ubuntu Server** in VirtualBox environment.
* **SSH Hardening:**

  * Changed default SSH port to `54321`
  * Disabled root login, password auth, X11 forwarding
  * Enforced `MACs hmac-sha2-512,hmac-sha2-256`
* **Firewall (UFW):**

  * Deny incoming, allow outgoing
  * Only SSH (custom port) allowed
* **PAM Password Policies:**

  * Enforced 14-character min length, complexity rules
* **Auditd & Logging:**

  * Monitored `/etc/passwd`, `/etc/shadow`, `/etc/group`
* **Kernel Hardening (`/etc/sysctl.conf`):**

  * Disabled TCP timestamps, restricted core dumps, enabled martian logging
* **Legal Banners:**

  * Configured `/etc/issue` and `/etc/issue.net`
* **CIS Manual Checks:**

  * Verified file permissions, disabled unused filesystems, secured GRUB
* **Vulnerability Scans:**

  * Nmap – Only port `54321` open, port 22 filtered
  * OpenVAS – Low severity issues (timestamps, weak MACs)

### **Tools Used**

* **UFW, Fail2Ban, Auditd, rkhunter, chkrootkit, OpenVAS, Nmap**
* **Manual CIS Benchmark Compliance**

**Deliverables:**

* **Nmap Scan (TXT)**
  Final stealth and version scan results after hardening (port 54321 only open).
* **OpenVAS Report (PDF)**
  Post-hardening vulnerability assessment showing low/none critical issues.
* **Secure Linux Server Setup & Hardening Report (DOCX)**
  Detailed CIS-based hardening steps, configurations (SSH, firewall, PAM, kernel), and audit findings.
* **Secure Linux Server Setup & Hardening Presentation (PPTX)**
  Executive summary with before/after comparison and next steps.

---

## Enterprise Tools & Technologies

**Operating Systems:** Ubuntu Server, Kali Linux
**Virtualization:** VirtualBox
**Vulnerability Scanning:** Nmap, OpenVAS
**Web App Testing:** DVWA, Burp Suite
**Server Security:** UFW, Fail2Ban, Auditd, PAM
---

## Folder Structure

```
└── Infotact Solutions/
    ├── Project 1 - Basic Vulnerability Assessment for a Small Business Network/
    │   ├── Basic Vulnerability Assessment - Report.pdf
    │   ├── Basic Vulnerability Assessment.pptx
    │   └── OpenVAS Report.pdf
    │
    ├── Project 2 - Web Application Penetration Testing (OWASP Top 10)/
    │   ├── Web Application Penetration Test DVWA.pdf
    │   └── Web Application Penetration Test DVWA.pptx
    │
    └── Project 3 - Secure Linux Server Setup & Hardening/
        ├── Nmap Scan.txt
        ├── OpenVAS Report.pdf
        ├── Secure Linux Server Setup & Hardening.docx
        └── Secure Linux Server Setup & Hardening.pptx
```
---

## Usage

Clone the repo and open each project folder for **detailed reports, configurations, and presentations**:

```bash
git clone https://github.com/<your-username>/infotact-solutions.git
cd infotact-solutions
```

---

## Author

**Ramjith M** – Cybersecurity Analyst (Trainee)

* Email: [ramjithmkannur@gmail.com](mailto:ramjithmkannur@gmail.com)
* Skills: Penetration Testing | Vulnerability Management | Server Hardening

---
