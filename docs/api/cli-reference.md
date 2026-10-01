# CLI reference

## `acme init [name]`

Scaffold a new project.

| Flag | Description |
|------|-------------|
| `--template` | `minimal` (default) or `full` |
| `--force` | Overwrite existing files |

## `acme mock`

Start a local mock server.

| Flag | Description |
|------|-------------|
| `--port` | Port (default `4010`) |
| `--spec` | Path to OpenAPI file |
| `--watch` | Reload on spec changes |

## `acme test`

Run contract tests against a base URL.

| Flag | Description |
|------|-------------|
| `--base-url` | Required target origin |
| `--all` | Test every operation |
| `--junit` | Write JUnit XML report |

## `acme import <source>`

Import OpenAPI from a URL or file path.
