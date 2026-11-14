# Containment and Response

## Actions described in the simulation
- Affected endpoint isolated and quarantined.
- Firewall controls used to block attacker access.
- Password reset for the affected account.

## Further validation an analyst should document
- Confirm endpoint isolation and record its timestamp.
- Revoke active sessions and tokens associated with the compromised identity, where supported.
- Review MFA status and authentication methods.
- Search for additional compromised accounts and endpoints.
- Correlate firewall, proxy, DNS, VPN, identity and file-access logs.
- Preserve relevant logs and forensic artefacts.
- Establish ransomware scope, backup integrity and recovery criteria.

Do not return an endpoint to production solely because it has been isolated. Establish scope, remove persistence, rebuild or reimage where appropriate, rotate exposed secrets and validate endpoint health before recovery.
