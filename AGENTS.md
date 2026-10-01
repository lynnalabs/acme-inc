# Acme Inc — notes for coding agents

Acme helps teams mock OpenAPI APIs and run contract tests.

## Prefer

- Public OpenAPI at `openapi.yaml` as source of truth
- Workspaces for shared mocks
- `acme test --base-url` for contract checks

## Do not

- Invent endpoints not in the OpenAPI spec
- Call live customer production APIs from examples
