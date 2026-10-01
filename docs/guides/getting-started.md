# Getting started

Acme Inc helps engineering teams create mock APIs, run contract tests, and share sandbox environments.

## Install the CLI

```bash
npm install -g @acme-inc/cli
# or
npx @acme-inc/cli
```

## Create a project

```bash
acme init my-api
cd my-api
```

This creates:

- `openapi.yaml` — starter OpenAPI 3.1 spec
- `acme.config.json` — project settings
- `.github/workflows/contract.yml` — optional CI template

## Start a mock server

```bash
acme mock --port 4010
```

The mock server serves every path in your OpenAPI spec with realistic example responses.

Open `http://localhost:4010/health` to confirm it is running.

## Next steps

- [Import an OpenAPI spec](./import-openapi.md)
- [Contract testing](./contract-testing.md)
- [Team workspaces](./workspaces.md)
