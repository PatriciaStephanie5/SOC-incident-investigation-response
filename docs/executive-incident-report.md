# Executive Incident Report

## Summary
Falkenstein Automotive GmbH (a fictional training organisation) experienced a simulated phishing-led incident resulting in malware installation, credential compromise, a suspicious sign-in from Rotterdam, access to information within several departments and a subsequent ransomware event.

## What happened
An employee executed a malicious attachment received through phishing. Malware was installed and the user's password was stolen. At 02:14, the compromised identity was used to sign in from Rotterdam, identified in the scenario as impossible travel. The account could access information in HR, Procurement, Finance and Engineering. Ransomware followed.

## Business impact
Personal and business information was put at risk, creating confidentiality, integrity and availability concerns. Stolen credentials could enable impersonation and follow-on attacks. Ransomware introduced operational disruption risk. The scenario does not quantify affected records, financial loss, downtime or confirmed exfiltration volume.

## Response
The endpoint was isolated and quarantined, firewall controls were used to block attacker access, and the affected password was reset.

## Priority recommendations
1. Enforce MFA and conditional access, with investigation of anomalous sign-ins.
2. Review permissions and implement least privilege across sensitive departments.
3. Strengthen email filtering, attachment detonation, application control and endpoint monitoring.
4. Correlate identity, endpoint, email, network and file-access telemetry.
5. Segment critical systems and sensitive data repositories.
6. Test immutable/offline backups and ransomware recovery.
7. Maintain a documented personal-data breach assessment and escalation process aligned with GDPR.

## Leadership decision
Sponsor a time-bound remediation plan covering identity security, least-privilege access, endpoint/email protection, monitoring and incident-response readiness. Assign accountable owners and completion dates.
