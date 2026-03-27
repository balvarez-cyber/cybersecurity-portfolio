# 🔍 Digital Forensics Investigation (Autopsy)

## 📌 Overview
Conducted a forensic analysis of a Windows 11 disk image using Autopsy to identify suspicious activity, recover deleted files, and analyze system artifacts related to possible unauthorized access and data exfiltration.

---

## 🎯 Objectives
- Identify evidence of unauthorized access
- Analyze user activity and system artifacts
- Recover deleted or hidden files
- Determine indicators of potential data exfiltration or malicious behavior

---

## 🛠 Tools Used
- Autopsy 4.22.0
- Windows 11 forensic disk image
- FTK Imager

---

## 🔎 Investigation Process

### 1. Event Log Analysis
I reviewed Windows event logs within the forensic image to identify authentication activity, system events, and evidence that could help reconstruct system usage and possible unauthorized access.

![Security Event Logs](../screenshots/1-security-event-logs.png)

**Evidence Notes:**  
Windows event logs such as `Security.evtx` and `System.evtx` were located under `Windows\System32\winevt\Logs`, providing valuable system and authentication artifacts.

---

### 2. Suspicious User Documents
I examined the Administrator user profile and identified a suspicious planning document located in the Documents folder.

![Suspicious Planning Document](../screenshots/2-user-documents-artifacts.png)

**Evidence Notes:**  
The file `todo.docx` was located in `Users\Administrator\Documents`, suggesting potential planning or staging activity tied to the user account.

---

### 3. Suspicious Executable Discovery
I reviewed the Downloads folder and identified an unexpected executable file.

![Suspicious Executable](../screenshots/3-suspicious-executable.jpeg)

**Evidence Notes:**  
The file `logger.exe` was identified in the Administrator Downloads folder. Its location and name made it stand out as potentially suspicious and relevant to the investigation.

---

### 4. Deleted File Recovery
I recovered a deleted file that contained especially important evidence.

![Deleted File Recovery](../screenshots/4-deleted-file-recovery.jpeg)

**Evidence Notes:**  
The deleted file `secret.txt` contained instructions involving confidential information, an external email address, and guidance to remove evidence afterward. This strongly suggested deliberate malicious intent and attempted concealment.

---

### 5. System Event Review
I also reviewed system-level event logs to help understand overall system activity and timeline context.

![System Event Log](../screenshots/5-system-event-log.jpeg)

**Evidence Notes:**  
The `System.evtx` log helped establish system-level activity such as startup, shutdown, and service-related events relevant to the investigation timeline.

---

### 6. Browser Artifact Analysis
I analyzed browser-related artifacts, including cookies, to confirm access to external websites.

![Browser Cookies](../screenshots/6-browser-cookies.png)

**Evidence Notes:**  
Browser cookies associated with Microsoft Edge showed evidence of access to external domains, helping establish browsing behavior and external site interaction.

---

### 7. Prefetch Analysis
I reviewed Windows Prefetch data to identify evidence of executed applications.

![Prefetch Evidence](../screenshots/7-prefetch-evidence.jpeg)

**Evidence Notes:**  
Prefetch entries for `MSEDGE.EXE` confirmed browser execution on the system and supported timeline reconstruction of user activity.

---

### 8. Browser History Analysis
I examined browser history artifacts to identify specific sites accessed from the system.

![Browser History](../screenshots/8-browser-history.png)

**Evidence Notes:**  
Browser history showed access to external websites, providing additional insight into user activity and system usage during the relevant timeframe.

---

## 🚨 Key Evidence Identified

### Suspicious Document
- File: `todo.docx`
- Location: `Users\Administrator\Documents`
- Relevance: Possible planning or preparation activity

### Unauthorized Executable
- File: `logger.exe`
- Location: `Users\Administrator\Downloads`
- Relevance: Suspicious executable in user download location

### Deleted Sensitive File
- File: `secret.txt`
- Relevance: Included instructions involving confidential information, outside communication, and evidence deletion

### Browser Artifacts
- Evidence of external website access through cookies and browser history

### Program Execution
- Prefetch artifacts confirmed execution of Microsoft Edge

### Event Logs
- Security and system event logs helped support timeline reconstruction and system activity analysis

---

## 🧠 Conclusion
The forensic investigation revealed multiple artifacts indicating suspicious and potentially malicious activity on the Windows 11 system. The most significant findings included a suspicious executable (`logger.exe`), a planning-related document (`todo.docx`), and a deleted text file (`secret.txt`) containing instructions consistent with data exfiltration and concealment.

Taken together, the recovered files, browser artifacts, event logs, and execution evidence support the conclusion that the system was used in a manner inconsistent with normal policy-compliant behavior and likely involved unauthorized handling of sensitive information.

---

## 💡 Skills Demonstrated
- Digital Forensics Analysis
- Artifact Identification
- Deleted File Recovery
- Windows Event Log Analysis
- Browser Artifact Analysis
- Prefetch Analysis
- Evidence Documentation
- Investigative Thinking
