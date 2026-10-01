# FAQ

## Does Acme call my live customer APIs?

No. Contract tests hit the `baseUrl` you pass. Snippet checks in Syndraft use the ingested OpenAPI only.

## Can I share mocks across a team?

Yes — create a [workspace](./workspaces.md) and invite editors.

## How do I skip a flaky operation?

Mark it with `x-acme-skip: true` in the OpenAPI operation. Skips appear in the weekly summary.
