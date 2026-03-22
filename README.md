# HackSmarter Web App Capstone Walkthrough

## Target
- hacksmarter.hsm
- dev.hacksmarter.hsm
- IP: 10.1.45.229

## Environment
- Kali Linux (WSL2)
- Firefox
- Caido Proxy
- HackSmarter VPN

## Step 1 – VPN Connectivity
Connected to HackSmarter VPN and verified access to target.

Command used:
ping -c 2 10.1.45.229

## Step 2 – Hosts File Configuration
Added domain mappings to /etc/hosts:

10.1.45.229 hacksmarter.hsm
10.1.45.229 dev.hacksmarter.hsm

This allowed proper domain-based testing.

## Step 3 – Proxy Configuration
Firefox configured to use Caido proxy.
Traffic confirmed inside Caido HTTP history.

## Step 4 – Application Reconnaissance
Performed manual browsing of:
http://hacksmarter.hsm

Captured requests and responses in Caido.

## Step 5 – Development Portal Discovery
Identified dev portal reference and accessed:
http://dev.hacksmarter.hsm

Development interface exposed without authentication.

## Step 6 – phpinfo Exposure
Accessed phpinfo from dev portal.
Sensitive information disclosed:
- PHP version
- Apache version
- Document root
- Internal IP address
- Debug settings enabled

## Findings
1. Exposed Development Portal
2. phpinfo Information Disclosure
3. Debug Mode Enabled
4. Sensitive Configuration Exposure

## Evidence
Screenshots included in /screenshots directory:
- proxy setup
- caido traffic
- hosts file configuration
- dev portal
- phpinfo exposure

## Conclusion
The assessment identified multiple security weaknesses during reconnaissance phase, including exposed development functionality and sensitive configuration disclosure.
