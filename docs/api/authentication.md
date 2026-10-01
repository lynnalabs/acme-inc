# Authentication

## CLI login

```bash
acme auth login
```

Opens a browser OAuth flow. Tokens are stored in `~/.config/acme/credentials.json`.

## API tokens

Create a token in the dashboard under **Settings → API tokens**.

```bash
export ACME_TOKEN=acm_live_...
acme workspace list
```

## Mock auth

When your OpenAPI security scheme is `bearer`, the mock server accepts any non-empty `Authorization: Bearer …` header unless you set `--strict-auth`.
