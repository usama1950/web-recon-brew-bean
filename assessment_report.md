# Cyber Security Assessment Report
## Brew & Bean Cafe

**Assessment Type:** Basic Security Assessment  
**Prepared by:** Muhammad Usama Arshad  
**Date:** 12 November 2026

## 1. Executive Summary

The purpose of this assessment was to review basic cybersecurity concepts and perform preliminary web reconnaissance for the Brew & Bean Cafe project.

The assessment combines two practical exercises: Linux security fundamentals through OverTheWire Bandit Levels 0–2 and web reconnaissance using Burp Suite Professional in a PortSwigger Web Security Academy lab.

The exercises helped identify important security practices related to remote access, file handling, web application endpoints, and input parameters.

## 2. Assessment Scope and Methodology

The assessment included:

- Linux command-line security concepts.
- SSH remote access and file permissions awareness.
- Handling special filenames and command-line input.
- Web reconnaissance using Burp Suite.
- Identification of application URLs and parameters.

**Scope limitation:** The Bandit and PortSwigger exercises were conducted in training environments. No direct penetration test of Brew & Bean Cafe's real systems was performed.

## 3. Findings – Linux Security (Task 1)

The OverTheWire Bandit exercises covered Levels 0–2.

**Level 0 – SSH Access**

Established an SSH connection to the Bandit server and used Linux commands such as `ls` and `cat` to locate and read files.

**Level 1 – Special Filenames**

Learned how to access files with special names, such as `-`, using relative paths.

**Level 2 – Filenames with Spaces**

Practiced accessing filenames containing spaces and special characters using quotation marks and relative paths.

**Security observation:** Correct command usage and careful handling of filenames are important for reliable Linux administration.

All discovered passwords were excluded from the public documentation.

## 4. Findings – Web Reconnaissance (Task 2)

**Tool:** Burp Suite Professional  
**Target:** PortSwigger Web Security Academy training lab  
**Method:** Browser traffic interception and Site Map analysis.

During reconnaissance, six distinct URLs were identified, including the homepage, `/filter` endpoint, and category-based requests.

**Identified parameter:**

- Endpoint: `/filter`
- Parameter: `category`

**Potential security concern: SQL Injection**

The `category` parameter was identified as an input worth further testing for SQL injection.

However, SQL injection was not confirmed during this reconnaissance exercise. Additional authorized testing would be required.

A Burp Suite Site Map screenshot is included in the project's screenshots folder.

## 5. Recommendations

**1. Enforce Strong Password Policies**

Require strong, unique passwords for employee accounts and administrative systems. Avoid password reuse and change compromised credentials immediately.

**2. Secure and Update Web Applications**

Keep website software, plugins, frameworks, and server components updated. Validate and sanitize user input, use parameterized SQL queries, and conduct regular authorized security testing.

**3. Enable Multi-Factor Authentication (MFA)**

Enable MFA for administrator accounts, email accounts, and other important business services to reduce the risk of unauthorized access.

## 6. Conclusion

The exercises provided practical experience in Linux security fundamentals and web reconnaissance.

The findings highlight the importance of secure remote access, careful file handling, input validation, strong authentication, and regular software maintenance.

Further testing of actual Brew & Bean Cafe systems should only be performed with proper authorization.

---

**End of Report**

*Prepared for the Brew & Bean Cafe Cyber Security Awareness Project.*
