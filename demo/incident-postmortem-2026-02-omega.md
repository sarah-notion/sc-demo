Title: Incident Postmortem — OMEGA — 2026-02-18

Incident ID

INC-OMEGA-2026-02-18

Unique demo keywords

- KEYWORD: koala-lighthouse-77
- KEYWORD: incident-honeycomb-91

Summary

On 18 Feb 2026, customers reported intermittent login failures for the AU region after a configuration change to the identity proxy.

Customer impact

- 4.7% of login attempts failed for ~23 minutes
- Primary region affected: Australia/Sydney
- Severity: SEV-2

Root cause

A misconfigured timeout between the edge gateway and the identity proxy caused request retries to pile up.

Resolution

Rolled back the timeout change and restarted the identity proxy service.

Action items

1. Add synthetic login checks for AU region (owner: Platform) — due 2026-03-01
2. Update runbook: "SSO / SCIM troubleshooting" — due 2026-03-05
3. Create alert: sustained 401/403 anomalies — due 2026-03-02

Search hints for the demo

Try searching for:

- "INC-OMEGA-2026-02-18"
- "incident-honeycomb-91"
- "SSO / SCIM troubleshooting"
- "Australia/Sydney login failures"
