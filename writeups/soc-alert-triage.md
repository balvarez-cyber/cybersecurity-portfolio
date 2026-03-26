# SOC Alert Triage – Phishing Investigation

## Overview
Analyzed inbound phishing alerts in a simulated SOC environment using TryHackMe.

## Objective
Determine whether alerts were true positives or false positives and document findings.

## Investigation Steps
- Reviewed email metadata (sender, subject, timestamps)
- Analyzed URLs for suspicious domains
- Identified phishing indicators (urgency, spoofed sender, malicious links)
- Checked firewall logs for blocked connections

## Findings
- Alerts contained suspicious external links
- Domains were not legitimate (e.g., amazon.biz instead of amazon.com)
- Firewall logs showed attempted connections to malicious URLs

## Conclusion
Classified alerts as **True Positive (Phishing)**

## Remediation Actions
- Blocked malicious domains
- Recommended user awareness training
- Suggested monitoring for similar activity

## Key Skills Demonstrated
- Phishing detection
- Alert triage
- Incident documentation
- Analytical thinking under uncertainty
