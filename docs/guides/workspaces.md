# Team workspaces

Workspaces let multiple engineers share mocks, specs, and test runs.

## Create a workspace

```bash
acme workspace create frontend-sandbox
```

## Invite teammates

```bash
acme workspace invite teammate@company.com --role editor
```

Roles: `viewer`, `editor`, `admin`.

## Share a mock URL

Every workspace mock gets a stable URL:

```
https://mock.acme-inc.dev/<workspace>/<project>
```

Rotate credentials with `acme workspace rotate-token`.
