# Contract testing

Contract tests assert that a live service still matches your OpenAPI contract.

## Run locally

```bash
acme test --base-url https://staging.example.com
```

Acme walks every operation marked `x-acme-test: true` (or all operations with `--all`) and checks:

1. Status code is in the documented responses
2. Response body validates against the schema
3. Required headers are present

## In CI

```yaml
- name: Contract tests
  run: npx @acme-inc/cli test --base-url ${{ secrets.STAGING_URL }} --all
```

## Flaky endpoints

Skip an operation temporarily:

```yaml
x-acme-skip: true
```

Prefer fixing the contract or the service — skips are reported in the weekly summary.
