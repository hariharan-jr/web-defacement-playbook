# SOC Paybookbook - Web Defacement Incident

## Incident Type:
Website Defacement (Unauthorized modification of website content)

## Objective
**The primary goals of this playbook are to:**
- Detect and verify defacement incidents
- Contain and mitigate the impact
- Identify root cause and attacker entry point
- Restore website functionality and integrity
- Communicate with stakeholders and document the incident

- ## Step by step response:

**-  1. PREPARATION**
- Maintain backups of web assets and databases
- Implement monitoring tools for website integrity
- Define escalation paths and response roles

**- 2. DETECTION:**
- Web defacement can be detected when the URL of the website remains the same,but the content has been changed without authorization. This usually includes messages from hackers, offensive content or replaced images.

- Example of Defaced Website: https://github.com/hariharan-jr/web-defacement-playbook/blob/e7afe5304215ef83cf7dd119956f42700e89eab7/assets/Defacement_Example.png

**How to detect:**
- Visit the website and look for any unexpected changes.
- Compare with a backup or a known good version.
- check for new or modified files on the server
- Monitor File Uploads & Modifications: A sudden spike in the number of uploaded or altered files—especially without approved changes—may indicate a potential web defacement or compromise. Such anomalies should be investigated immediately.

The Sitelock SMART product helps track daily file activity, showing how many files were uploaded or modified each day, making it easier to detect unusual patterns.

**## 3.Containment:**
Once a defacement is detected, the immediate goal is to stop the attack, minimize the impact and begin recovery.

**Immediate Steps:**
1. Take the website offline temporarily / Under Maintenance Mode (To protect users)
2. Disable Access Points (Revoke accesss to any unknown or suspicious users)
3. Check for backdoors or malicious scripts.
4. Identify Entery point: Review logs to find how the attacker gained access (eg: Vulnerabile Plugin, Weak Credentials)

**4. ERADICATION:**
After Containing the defacement, the next step is to completely remove all malicious files and attacker access.

**Key Steps:**
- Identify and patch vulnerabilities (e.g., SQLi, RFI, XSS)
- Remove malicious content and backdoors
- Scan for malware and unauthorized scripts
- Update all plugins, themes and the cms to the latest version

- Goal: Ensure no backdoors or malware remain in the system before going live again.

**5. RECOVERY:**
Once the system is cleaned, it's time to bring the website back online safely and ensure everything is working properly

**Key Steps:**
- Restore website from clean backups
- Validate integrity of restored content (verify all pages are loading correctly and there are no broken links or missing assets)
- Test Functionality
- Re-enable services and monitor closely


- Ensure the site is fully operational and secure before notifying users or customers
  
**6. COMMUNICATION:**
Clear and Timely Communication is important during a defacement incident to maintain trust and coordinate response efforts.

**Internal Communication**:
Notify the security/ IT Team immediately
Document and Inform Management or leadership with a brief summary of the issue, impact and actions taken
Share updates as progess is made (Containment, Cleanup, Recovery)

**External Communication**:
Notify the hosting provider (Bluehost, Hostgator) and Security Vendor (Sitelock)
Inform customers or users (only if there is a visible defacement or security impact (data exposure, malicious redirect, defacement))

**7. POST-INCIDENT REVIEW:**
After the incident is fully resolved conduct a post-incident review to understand what happened and how to improve future response.

**Key Action:**
- Conduct root cause analysis (eg: outdated plugin, weak password)
- Document the timeline
- Update security controls and policies
- Refine playbook based on lessons learned

- The goal is to prevent similar incidents and improve response readiness.

**- 8. TOOLS & RESOURCES:**
- File integrity monitoring (e.g., Sitelock)
- Web scanners (e.g., VirusTotal, Sitelock, Nessus)
- Log analysis tools (e.g.,Splunk)
- Backup and restore.
