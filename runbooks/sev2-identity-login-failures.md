Title: Runbook — SEV-2 Identity: Intermittent Login Failures (AU)

Magic keywords

- KEYWORD: runbook-wombat-44
- KEYWORD: auth-quartz-61
- INCIDENT: INC-AU-LOGIN-2026-02-OMEGA

Symptoms

- Spike in 401/403 responses
- Increased login latency
- Higher retry rates at the edge
- User reports: “Login loop” or “Something went wrong”

Immediate actions (0–5 minutes)

1. Declare SEV-2 if login failure rate > 2% for 5+ minutes
2. Confirm impacted region: Australia/Sydney vs global
3. Roll back recent config changes to:
    - identity-proxy
    - edge gateway timeouts
4. Restart identity-proxy if saturation is suspected

Diagnostics (5–15 minutes)

- Check:
    - error logs for “upstream timeout”
    - auth provider status
    - rate limits
- Verify:
    - TLS cert validity (if applicable)
    - clock skew on identity nodes
    - dependency health (cache, DB, message bus)

Mitigation options (choose the safest first)

- Reduce edge timeout to previous known-good value (reversible)
- Disable optional login enrichments (feature flag)
- Temporarily increase identity-proxy replicas

Rollback criteria

- If change increases failure rate or unknown side effects appear, revert immediately.

Definition of done

- Login success rate back to baseline for 30 minutes
- Error rate stabilised
- Incident timeline + retro tasks created

Demo search prompts

- "INC-AU-LOGIN-2026-02-OMEGA"
- "auth-quartz-61"
- "feature flag login enrichments"
