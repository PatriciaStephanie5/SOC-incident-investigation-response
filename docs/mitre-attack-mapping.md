# MITRE ATT&CK Mapping

This is a preliminary hunting map, not a claim that each technique is confirmed.

| Scenario behaviour | ATT&CK area to investigate | Hunting direction |
|---|---|---|
| Phishing email | Initial Access – Phishing | Review headers, sender infrastructure, URLs and attachment metadata |
| Malicious attachment execution | Execution – User Execution / Malicious File | Review process creation, parent-child process chain and file execution telemetry |
| Credential theft | Credential Access | Determine whether credentials were captured from browser, memory, input or another source |
| Rotterdam sign-in at 02:14 | Valid Accounts / identity-based access | Correlate identity logs, source IP, device, MFA and session details |
| Access to multiple departmental data sets | Discovery / Collection; assess lateral movement only if supported | Review file access, SMB, directory and application logs |
| Ransomware | Impact – Data Encrypted for Impact may be relevant | Confirm encryption activity, affected paths, ransom note and endpoint telemetry |

## Hunting priorities
1. Search email and endpoint telemetry for the phishing message, attachment, hashes and execution time.
2. Review process trees around attachment execution.
3. Correlate authentication events for the compromised identity.
4. Review access logs for HR, Procurement, Finance and Engineering repositories.
5. Hunt for bulk reads, archive creation and unusual outbound transfers.
6. Identify ransomware indicators and affected systems.

Assign exact ATT&CK technique IDs only after validating behaviour against evidence and the ATT&CK knowledge base.
