Title: Runbook — Database Connection Saturation

Magic keywords

- KEYWORD: db-macadamia-25
- SERVICE: postgres-primary
- ALERT: GRAFANA-ALERT-DB-CONN-EXHAUST

Symptoms

- Elevated API latency
- Errors:
    - “too many connections”
    - connection pool timeouts
- DB CPU may be normal while connection count is high

Immediate actions

1. Confirm connection count + pool stats (app + DB)
2. Identify top connection sources (service, job, tenant)
3. Apply one reversible mitigation:
    - scale app replicas down/up carefully (depending on pool behaviour)
    - reduce worker concurrency
    - enable read-only mode (if supported)
4. If safe, increase pool size only after verifying DB max_connections headroom

Diagnostics

- Check recent deploys for connection leaks
- Review long-running queries + idle in transaction sessions
- Validate connection pool settings (max, idle timeout)

Prevention

- Add pool metrics + dashboards
- Add automated tests for connection leaks
- Ensure timeouts exist at:
    - app pool
    - DB server
    - network layer

Demo searches to try

- "GRAFANA-ALERT-DB-CONN-EXHAUST"
- "db-macadamia-25"
- "idle in transaction"
