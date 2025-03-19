# Web Security Research - XSS Attack, Vulnerability Scan, and Report Generation

## Overview
This repository contains research and testing related to web security, including:
- **Stored DOM-based XSS Attack**
- **Website Vulnerability Scanning using Netsparker**
- **Security Report Generation**

Each task is documented with steps and results.

---

## 1. Stored DOM-based XSS Attack
### **Objective:**
To exploit a stored DOM-based XSS vulnerability in the blog comment functionality of a target website.

### **Steps to Reproduce:**
1. Visit the vulnerable website (PortSwigger Lab).
2. Locate the comment section and enter the following payload:
   ```html
   <><img src=1 onerror=alert(1)>
   ```
3. Submit the comment.
4. Reload the page and verify that the alert box appears, confirming the XSS execution.
5. If not visible, inspect the DOM elements to confirm the injection.

### **Outcome:**
- Successfully bypassed the website's replace() function-based XSS protection.
- Stored XSS executed upon loading the affected page.

---

## 2. Web Vulnerability Scan using Netsparker
### **Objective:**
Perform a security assessment of `testasp.vulnweb.com` using Netsparker.

### **Findings:**
- **Critical:** Out-of-band SQL Injection
- **High:** Passwords transmitted over HTTP
- **Medium:** Possible Cross-Site Request Forgery (CSRF)
- **Low:** Outdated IIS version detected
- **Informational:** Cookies missing `HttpOnly` flag, Windows Short Filename disclosure

### **Outcome:**
- The scan detected **84 security issues**, with a mix of critical, high, medium, and low-risk vulnerabilities.
- Detailed report generated for analysis.

---

## 3. Security Report Generation
### **Objective:**
Compile a professional-style security report summarizing the findings from the vulnerability scan.

### **Report Includes:**
- **Target Website:** `testasp.vulnweb.com`
- **Scan Summary:** Number of vulnerabilities categorized by severity
- **Key Findings:** SQL injection, XSS, CSRF, outdated technologies
- **Remediation Recommendations:** Secure password transmission, input validation, CSRF protection, server updates

### **Outcome:**
- A structured report was generated summarizing all vulnerabilities and their impacts.
- Ready for submission or further analysis.

---

## Conclusion
This repository serves as documentation of our web security research activities. The steps outlined can be used for further security testing, ethical hacking, and cybersecurity learning.

### **Disclaimer:**
This project is for educational and ethical hacking purposes only. Do not perform security testing on any system without explicit permission.

---

## Author
[github.com/phoenixdev-512]
