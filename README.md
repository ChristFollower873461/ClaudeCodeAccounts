# ClaudeCodeAccounts

This repository currently contains a small, retained Next.js prototype. Despite
the repository name, the checked-in application does not implement Claude
account management, authentication, customer data storage, uploads, payments,
or a public write API.

## Status

- Classification: public prototype, not a production release.
- The UI remains the Create Next App starter while the intended product scope is
  decided.
- No deployment configuration is committed to the repository.
- Package and security maintenance is active even while the product scope is
  intentionally narrow.

See [STATUS.md](STATUS.md) for the maintenance decision and [SECURITY.md](SECURITY.md)
for private vulnerability reporting.

## Local verification

Use Node.js 22.13 or newer.

```bash
npm ci
npm run lint
npm run typecheck
npm run build
npm test
npm audit
```

The production response configuration removes the framework-identifying header
and sets CSP, frame, content-type, referrer, opener, and permissions policies.
HSTS should be added only after a real HTTPS production hostname and rollback
path have been verified.
