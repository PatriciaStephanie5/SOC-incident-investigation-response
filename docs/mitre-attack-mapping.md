# MITRE ATT&CK Mapping

This mapping separates **scenario-supported** behaviour from **hypotheses**. Exact technique IDs are assigned only where the scenario provides sufficient indicators. All other entries remain hunting leads.

| Scenario Behaviour | Status | MITRE Tactic | Technique (ID) | Evidence / Rationale | Hunting Priority |
|---|---|---|---|---|---|
| Phishing email leading to attachment execution | Scenario-supported | Initial Access | Phishing: Spearphishing Attachment (T1566.001) | Employee opened phishing email and executed malicious attachment | High – recover email headers, attachment hash, and execution telemetry |
| Malware installation on endpoint | Scenario-supported | Execution | User Execution: Malicious File (T1204.002) | Malicious attachment executed on the host | High – process creation and parent-child analysis |
| Credential theft | Scenario-indicated | Credential Access | Credentials from Password Stores / OS Credential Dumping (T1555 / T1003) – *hypothesis* | Password was stolen; exact method not specified | High – determine capture method (browser, memory, keylogger, etc.) |
| Sign-in from Rotterdam at 02:14 | Scenario-supported | Defense Evasion / Initial Access | Valid Accounts (T1078) | Impossible-travel authentication using compromised identity | High – correlate identity logs, source IP, device, MFA status |
| Access to HR, Procurement, Finance, Engineering data | Scenario-indicated | Discovery / Collection | File and Directory Discovery (T1083) / Data from Local System (T1005) – *hypothesis* | Account had legitimate access rights; no confirmed lateral movement tooling | Medium – review file-access and SMB logs |
| Ransomware | Scenario-supported | Impact | Data Encrypted for Impact (T1486) | Ransomware event followed the compromise | High – confirm encryption activity, affected paths, ransom note |

### Hunting Priorities (ordered)
1. Recover phishing message, attachment, and execution telemetry.
2. Reconstruct process tree around attachment execution.
3. Correlate all authentication events for the compromised identity (including MFA and device context).
4. Review access logs for the four departmental repositories.
5. Hunt for bulk reads, archive creation, or unusual outbound transfers.
6. Confirm ransomware indicators and scope of encryption.

**Rule applied:** Exact ATT&CK technique IDs are used only when behaviour is sufficiently described. Remaining items are labelled as hypotheses and treated as hunting leads.
