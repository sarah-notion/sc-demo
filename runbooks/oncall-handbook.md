Title: On-Call Handbook — APAC (Demo)

Magic keywords

- KEYWORD: pager-kookaburra-09
- KEYWORD: shift-bilby-72

Scope

This handbook covers triage, escalation, and comms for APAC incidents.

On-call principles

- Stabilise first, diagnose second
- Communicate early and regularly
- Prefer reversible changes

Triage checklist (first 10 minutes)

1. Confirm incident severity (SEV-1/2/3)
2. Establish a single incident channel + incident lead
3. Check dashboards:
    - API 5xx rate
    - Login success rate
    - Queue depth / saturation
4. Confirm blast radius:
    - Region (AU/SG/Global)
    - Specific endpoint or service
5. Start an incident timeline document (timestamps in Australia/Sydney)

Escalation matrix (demo)

- Platform On-call: primary responder
- SRE Lead: if SEV-1 or customer-impact > 15 mins
- Security: if auth anomalies, suspicious logins, token leakage
- Comms/Support: if external customer comms required

Comms template (internal)

- What we know:
- What we’re doing:
- Customer impact:
- Next update at:

Demo searches to try

- "shift-bilby-72"
- "incident timeline Australia/Sydney"
- "stabilise first diagnose second"
