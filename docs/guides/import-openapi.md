# Import an OpenAPI spec

Acme Inc accepts OpenAPI 3.0 and 3.1 JSON or YAML.

## From a URL

```bash
acme import https://api.example.com/openapi.json
```

## From a local file

```bash
acme import ./openapi.yaml
```

## What gets imported

- Paths and operations
- Request bodies and response schemas
- Examples (used by the mock server)
- Security schemes (mapped to mock auth headers)

Circular `$ref`s are resolved once. Unsupported OAS extensions are ignored with a warning.

## Validate before import

```bash
acme lint ./openapi.yaml
```

Exit code `0` means the spec is ready for mock + contract testing.
