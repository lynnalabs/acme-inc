# Mock webhooks

Acme can simulate inbound webhooks so your handlers are testable before the real provider is live.

## Register an endpoint

```bash
acme webhook create --url https://localhost:3000/hooks/stripe
```

## Replay an event

```bash
acme webhook replay --fixture stripe.invoice.paid
```

> Prefer OpenAPI `webhooks:` blocks when available. The REST `/webhooks/endpoints` path is deprecated.
