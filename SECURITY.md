# Security Policy

ClaudeCodeAccounts is currently a public Next.js prototype. The checked-in app
does not implement accounts, authentication, uploads, payments, customer data
storage, or a public write API.

Report suspected vulnerabilities through
[GitHub private vulnerability reporting](https://github.com/ChristFollower873461/ClaudeCodeAccounts/security/advisories/new),
not a public issue.

## Maintained Boundary

- Locked dependencies must pass `npm audit` without an exception list.
- Pull requests and `main` must pass lint, typecheck, production build, response
  smoke, and audit gates.
- GitHub Actions are pinned to immutable commit SHAs with read-only repository
  permissions.
- Secrets, local environment files, build output, and generated credentials do
  not belong in Git history.
- Public responses set CSP, frame, content-type, referrer, opener, and permissions
  policies. HSTS remains intentionally unset until a real HTTPS production
  hostname and rollback path are verified.

Any future account, authentication, storage, upload, payment, or write behavior
requires a new threat review before release.
