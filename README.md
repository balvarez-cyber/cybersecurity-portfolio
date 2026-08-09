# 🛡️ Cybersecurity Portfolio

Hands-on cybersecurity portfolio showcasing practical work in **security operations, incident response, digital forensics, application security, secure software development, and threat detection**.

The projects in this repository demonstrate my ability to investigate security events, analyze technical evidence, remediate application vulnerabilities, validate security controls, and communicate findings through structured technical documentation.

---

## 🔥 Featured Projects

### 🤖 SentinelDocs — LLM Security Lab

Built a Python and Flask document-support assistant to demonstrate how indirect
prompt injection can manipulate an AI system and how application-controlled
security boundaries change the outcome.

**Key accomplishments:**

- Integrated the OpenAI API with local document retrieval and a simulated support-ticket tool.
- Created vulnerable and hardened modes for controlled security testing.
- Demonstrated a poisoned vendor document changing a pending review into a false approval.
- Enforced ticket authorization in deterministic Python application code instead of trusting the model.
- Preserved live-model evidence and documented the threat model and OWASP LLM Top 10 mapping.
- Validated application and security behavior with 12 passing Pytest tests.

**Technologies:** Python • Flask • OpenAI API • Prompt Injection • Authorization • Pytest

👉 [View the complete project, source code, and security assessment](https://github.com/balvarez-cyber/sentineldocs-llm-security-lab)

---

### 🔐 Python Application Security Hardening

Hardened a vulnerable Python Flask application by addressing weaknesses in secrets management, credential storage, API authentication, and authorization.

**Key accomplishments:**

- Replaced hardcoded secrets with environment-based configuration and secure random fallbacks.
- Replaced plaintext passwords with PBKDF2-SHA256 password hashes.
- Implemented secure password verification with `check_password_hash()`.
- Enforced Bearer-token authentication on protected API endpoints.
- Implemented role-based access control using the principle of least privilege.
- Validated all remediations through automated security testing with Pytest.

**Technologies:** Python • Flask • PBKDF2-SHA256 • RBAC • API Security • Pytest

👉 [View Project](writeups/python-application-security-hardening.md)

---

### 🛡️ Secure Flask Application with Defensive Programming

Improved the security, reliability, and resilience of an existing Flask application through defensive programming and automated testing.

**Key accomplishments:**

- Added input validation for invalid and unexpected values.
- Implemented assertions to validate critical application assumptions.
- Added targeted exception handling for `KeyError` and `ValueError`.
- Replaced console output with structured INFO, WARNING, and ERROR logging.
- Verified the application through manual testing and six passing Pytest tests.

**Technologies:** Python • Flask • Defensive Programming • Logging • Pytest

👉 [View Project](writeups/python-defensive-programming.md)

---

### 🔎 Splunk SIEM Investigation: VPN Log Analysis

Investigated VPN authentication activity using Splunk to identify anomalous user behavior and suspicious connection patterns.

**Key accomplishments:**

- Ingested and analyzed VPN authentication logs.
- Performed user-focused investigation and geographic filtering.
- Correlated login activity across users, locations, and timestamps.
- Applied a structured SIEM investigation methodology.
- Documented findings and potential security concerns.

**Technologies:** Splunk • SPL • Log Analysis • User Behavior Analysis

👉 [View Project](writeups/splunk-vpn-investigation.md)

---

### 🔎 Elastic SIEM Investigation: VPN Log Analysis

Analyzed VPN activity in Elastic SIEM to identify suspicious authentication behavior, unusual IP activity, and potential unauthorized account usage.

**Key accomplishments:**

- Used KQL to filter users, IP addresses, locations, and authentication events.
- Investigated failed login patterns and time-based activity spikes.
- Identified abnormal connection behavior and suspicious account activity.
- Correlated multiple data points to assess potential security risk.

**Technologies:** Elastic SIEM • KQL • Authentication Analysis • Threat Hunting

👉 [View Project](writeups/elastic-siem-vpn-investigation.md)

---

### 🚨 EDR Alert Investigation

Investigated a simulated multi-stage endpoint attack involving malicious macro execution, PowerShell activity, and credential-access behavior.

**Key accomplishments:**

- Analyzed parent-child process relationships and process execution chains.
- Investigated PowerShell activity and LSASS memory access.
- Distinguished malicious behavior from legitimate system activity.
- Classified findings using the MITRE ATT&CK framework.
- Documented investigation findings and response recommendations.

**Technologies:** EDR • Process Analysis • PowerShell • MITRE ATT&CK

👉 [View Project](writeups/edr-alert-investigation.md)

---

### ⛏️ SIEM Investigation: CryptoMiner Detection

Investigated suspected unauthorized cryptocurrency-mining activity using SIEM alerts and endpoint process data.

**Key accomplishments:**

- Analyzed suspicious process execution and detection events.
- Identified indicators of compromise and abnormal resource usage.
- Assessed the activity as potential unauthorized cryptomining.
- Recommended containment, remediation, and follow-up monitoring actions.

**Technologies:** SIEM • Malware Analysis • IOC Identification • Incident Response

👉 [View Project](writeups/siem-investigation.md)

---

### 🧪 Digital Forensics Investigation

Performed forensic analysis of a Windows 11 disk image using Autopsy to identify suspicious files, deleted evidence, and relevant user activity.

**Key accomplishments:**

- Examined browser artifacts, event logs, file-system data, and deleted files.
- Correlated forensic artifacts to reconstruct user activity.
- Identified evidence relevant to potential data exfiltration.
- Maintained an evidence-based investigative approach.
- Documented findings in a structured forensic report.

**Technologies:** Autopsy • Windows Forensics • Timeline Analysis • Digital Evidence

👉 [View Project](writeups/autopsy-digital-forensics.md)

---

### 🎣 SOC Alert Triage: Phishing Investigation

Investigated a simulated phishing alert by analyzing sender information, domains, message content, and other indicators of compromise.

**Key accomplishments:**

- Identified spoofed domains and suspicious email indicators.
- Evaluated the alert and classified it as a true positive.
- Documented the investigative reasoning and supporting evidence.
- Recommended containment and response actions.

**Technologies:** Phishing Analysis • IOC Validation • Alert Triage • Threat Classification

👉 [View Project](writeups/soc-alert-triage.md)

---

## 🚀 Technical Skills

### Security Operations and Incident Response

- SOC alert triage and escalation
- Incident investigation and documentation
- SIEM log analysis and event correlation
- Endpoint and process-chain analysis
- Threat hunting and IOC identification
- MITRE ATT&CK mapping
- Authentication and user-behavior analysis
- Containment and remediation recommendations

### Application Security and Secure Development

- Python and Flask application security
- Defensive programming
- Secrets management
- PBKDF2-SHA256 password hashing
- Secure password verification
- API authentication
- Bearer-token validation
- Role-based access control
- Input validation and exception handling
- Structured application logging
- Automated security testing with Pytest

### Digital Forensics

- Windows disk-image analysis
- File-system and deleted-file analysis
- Browser and event-log artifacts
- Timeline reconstruction
- Evidence handling and chain of custody
- Forensic documentation
- Evidence-based investigative reporting

---

## 🛠️ Tools and Technologies

**Security Operations:** Splunk • Elastic SIEM • EDR platforms • Windows Event Logs • MITRE ATT&CK

**Digital Forensics:** Autopsy • FTK • Windows artifacts • Timeline analysis

**Development and Testing:** Python • Flask • Pytest • Git • GitHub • PowerShell • Bash

**Querying and Analysis:** SPL • KQL • SQL

**Training Platforms:** TryHackMe

---

## 🧠 What This Portfolio Demonstrates

This portfolio demonstrates my ability to:

- Investigate security alerts using structured analytical methods.
- Correlate endpoint, authentication, network, and user-activity data.
- Distinguish suspicious behavior from legitimate activity.
- Perform digital forensic analysis and document supporting evidence.
- Identify and remediate application security vulnerabilities.
- Implement authentication, authorization, logging, and credential-protection controls.
- Validate security improvements through automated testing.
- Translate technical findings into clear, actionable recommendations.

---

## 📚 Education and Professional Development

- Bachelor of Science, Cybersecurity and Information Assurance — Western Governors University, nearing completion
- ISC2 Systems Security Certified Practitioner (SSCP)
- CompTIA CySA+
- CompTIA Security+
- CompTIA Network+
- CompTIA A+
- CompTIA Data+
- CompTIA Project+
- ITIL 4 Foundation
- Linux Essentials

**Current areas of study:** Cloud security • Penetration testing • Detection engineering • Security automation

---

## 📈 Current Focus

I am currently expanding my hands-on experience in:

- Incident response and digital forensics
- Application security
- Cloud security
- Detection engineering
- Threat hunting
- Penetration testing
- Python-based security automation

---

## 👤 About Me

I am a cybersecurity professional with a background in law enforcement, security operations, incident response, investigations, and technical report writing. That experience strengthened my ability to assess complex situations, preserve evidence, communicate clearly, and make defensible decisions under scrutiny.

I am now applying those investigative skills to cybersecurity through hands-on work in security operations, digital forensics, application security, secure software development, and cloud security.

This portfolio continues to grow as I complete new projects, certifications, labs, and technical investigations.
