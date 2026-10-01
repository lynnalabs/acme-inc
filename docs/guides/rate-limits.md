# Rate limits

Acme enforces per-workspace rate limits on the public API.

| Plan | Requests / minute |
| ---- | ----------------- |
| Free | 60 |
| Team | 600 |
| Enterprise | Custom |

When you exceed the limit, the API returns `429` with `Retry-After`.

```http
HTTP/1.1 429 Too Many Requests
Retry-After: 12
X-RateLimit-Limit: 60
X-RateLimit-Remaining: 0
```

Use exponential backoff in clients. Workspace admins can view usage in the dashboard under **Settings → Usage**.
