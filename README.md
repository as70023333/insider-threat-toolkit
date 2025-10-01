# Insider Threat Toolkit

Opinionated starter kit for detecting and triaging potential insider activity involving GitHub (org-level or enterprise logs).

Contents:
- Sigma rules (generic -> convert to your SIEM)
- Splunk queries
- Elastic / KQL queries
- Python script to parse GitHub audit logs and flag anomalies
- Incident triage & containment playbooks
- Tuning notes and testing dataset

Goal: give an ops team fast detection capabilities focused on:
- suspicious Personal Access Token (PAT) usage
- mass repo cloning or exports
- admin changes and privilege escalations
- package registry exfiltration
- secrets/credential misuse

How to use:
1. Place your GitHub audit logs (organization audit log / enterprise audit log) into your SIEM or S3.
2. Convert Sigma rules to your SIEM or import the provided queries.
3. Run `scripts/gh_audit_detector.py` against sample or live audit JSON for quick testing.
4. Follow `playbooks/triage_runbook.md` when an alert fires.

Contributions welcome. See `CONTRIBUTING.md`.
