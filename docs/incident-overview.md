# Incident Overview

**Organisation:** Falkenstein Automotive GmbH (fictional)  
**Incident:** Phishing-led endpoint and identity compromise followed by ransomware  
**Affected identity:** Employee identity (name withheld)  
**Suspicious sign-in:** 02:14 from Rotterdam  
**Access scope:** HR, Procurement, Finance and Engineering

An employee received a phishing email, opened it and executed a malicious attachment. Malware was installed on the employee's host and the user's password was stolen. The compromised identity was subsequently used to sign in from Rotterdam at 02:14, which the scenario identified as impossible travel.

The account's permissions extended to information across several departments. The incident later escalated to ransomware. The scenario indicates that the employee's personal data and other people's data were in the intruders' hands.

## Potential impact
- **Confidentiality:** personal and business information may have been exposed.
- **Integrity:** unauthorised modification or corruption may have occurred; confirmation requires evidence.
- **Availability:** ransomware created service-disruption risk.
- **Identity:** stolen credentials could enable impersonation and follow-on access.

The scenario does not quantify affected records, confirmed exfiltration volume, financial loss or downtime.

## Containment described
The affected endpoint was isolated and quarantined, firewall controls were used to block attacker access, and the affected account's password was reset.

## Analyst assessment
The incident demonstrates how phishing, endpoint execution, credential compromise and excessive access can combine to expand the blast radius. Identity containment and least-privilege review are as important as endpoint isolation.
