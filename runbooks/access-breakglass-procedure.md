Title: Procedure — Break-glass Admin Access (Operations)

Magic keywords

- KEYWORD: access-emu-88
- KEYWORD: audit-lamington-07

When to use

Only during SEV-1/2 incidents where normal access paths are blocked.

Controls

- Two-person rule (approver + executor)
- Time-boxed elevation (e.g., 60 minutes)
- Mandatory audit notes

Steps

1. Incident lead declares break-glass required
2. Approver confirms scope + time window
3. Executor requests elevation via approved mechanism
4. Record in incident timeline:
    - who, why, when, what systems
5. After use:
    - revoke access
    - rotate any credentials/tokens if exposure is possible
    - add retro action item

Audit requirements

- Store approvals
- Store command/actions summary
- Link incident ID

Demo searches to try

- "access-emu-88"
- "two-person rule time-boxed elevation"
- "rotate credentials/tokens"
