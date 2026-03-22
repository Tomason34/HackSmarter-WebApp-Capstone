# HackSmarter Capstone – Vulnerability Notes

## 1. Exposed Development Portal
URL: http://dev.hacksmarter.hsm  
Description:
The development environment was accessible without authentication.

Impact:
Attackers can access debug tools and sensitive configuration.

Severity: Medium


## 2. phpinfo() Information Disclosure
Description:
The dev portal exposed phpinfo() output.

Information disclosed:
- PHP version
- Apache version
- Document root
- Internal IP address
- Enabled modules
- Debug configuration

Impact:
Provides attackers with reconnaissance data for targeted exploitation.

Severity: Medium


## 3. Debug Mode Enabled
Observation:
Error display enabled in production-like environment.

Impact:
May expose stack traces, file paths, and sensitive logic.

Severity: Medium


## 4. Sensitive Configuration Exposure
Leaked Information:
- /var/www/html/dev.hacksmarter.hsm
- Internal container IP
- Apache modules
- PHP extensions

Impact:
Facilitates LFI, RCE, and targeted attacks.

Severity: Low-Medium


## 5. Development Artifacts Exposure
Dev references and internal notes were visible.

Impact:
Reveals testing environment and potential hidden endpoints.

Severity: Low


## Summary
Total Findings: 5  
Risk Level: Moderate  
Primary Issue: Development environment exposed to unauthenticated users.
