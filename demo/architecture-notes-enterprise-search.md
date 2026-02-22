Title: Architecture Notes — Enterprise Search (GitHub + Notion)

Unique demo keywords

- KEYWORD: OPAL-PROJECT-NEBULA
- KEYWORD: architecture-mango-33

High-level design

- Sources: GitHub repos, issues, pull requests; plus internal docs
- Indexing: incremental updates, permission-aware retrieval
- Query UX: natural language + filters

Key terms

- “permission-aware search”
- “connected knowledge”
- “source attribution”

Operational checklist

- Confirm GitHub connection authorised
- Confirm repo access
- Validate content types are enabled (files/issues/PRs as applicable)
- Run a test search for "architecture-mango-33"

Non-goals

- Real-time indexing within seconds (demo assumes a short delay is acceptable)
