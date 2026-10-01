# Acme Inc

Developer platform for **API mocking**, **contract testing**, and **shared sandboxes**.

This is a **public OSS fixture** for [Syndraft](https://github.com/lynnalabs/syndraft) end-to-end testing (knowledge ingest → draft → human approval). It is not a real product backend.

## Wire into Syndraft

| Field | Value |
| ----- | ----- |
| Docs platform | **GitHub** |
| Org / Owner | `lynnalabs` |
| Repository | `acme-inc` |
| Docs path | `docs` |
| Changelog feed | `https://raw.githubusercontent.com/lynnalabs/acme-inc/main/docs/changelog/feed.xml` |
| OpenAPI spec | `https://raw.githubusercontent.com/lynnalabs/acme-inc/main/openapi.yaml` |
| Blog feed (optional) | `https://raw.githubusercontent.com/lynnalabs/acme-inc/main/docs/blog/feed.xml` |
| Sitemap (optional) | `https://raw.githubusercontent.com/lynnalabs/acme-inc/main/public/sitemap.xml` |

No GitHub App install is required for **public** docs ingest.

After saving sources in Syndraft Settings, click **Refresh sources**, then confirm `/knowledge` shows `docs_github`, `docs_openapi`, and `changelog_feed`.

## What’s in the box

| Path | Purpose |
| ---- | ------- |
| `docs/guides/*` | Markdown for GitHub docs ingest |
| `docs/api/*` | Auth + CLI reference |
| `docs/changelog/` | Release notes + RSS (drift / AgentRel) |
| `docs/blog/feed.xml` | Blog RSS (Tier B) |
| `openapi.yaml` | OpenAPI 3.x for snippet gate + GEO drafts |
| `public/sitemap.xml` | Sitemap coverage helper |
| `llms.txt` / `AGENTS.md` | Agent-facing artifacts (Full + Mintlify paths) |
| `mintlify.json` | Mintlify nav stub for docs delivery tests |

## Suggested draft topics

- How to create a workspace and invite an editor
- Run contract tests in CI against staging
- Rate-limit headers and 429 handling
- Migrating off deprecated `POST /webhooks/endpoints`

## Quick start (fake CLI)

```bash
npx @acme-inc/cli init
npx @acme-inc/cli mock --spec ./openapi.yaml
```

## License

MIT — fixture content only.
