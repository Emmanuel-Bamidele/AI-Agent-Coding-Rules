# CI/CD Rules

## Required quality gates

CI should run applicable checks:

- Install from lockfile
- Format check
- Lint
- Type check
- Unit tests
- Integration tests
- Build
- Secret scan
- Dependency audit
- Container scan where applicable

## CI principles

- CI must be reproducible.
- CI should not require production secrets.
- CI should fail on real quality problems.
- CI should match documented local commands.
- Deployment should require passing checks.
- Untrusted forks should not receive sensitive secrets.
- Security scans should block critical issues.

## Local commands

If the repo has a unified command, prefer it:

```bash
make check
```

or:

```bash
npm run check
```

If no unified command exists, run the relevant individual checks.

## Deployment safety

Deployment should include:

- Passing CI
- Migration safety
- Rollback plan
- Health checks
- Smoke tests
- Environment-specific config validation

## Agent behavior

When modifying CI:

- Explain why the workflow changed.
- Avoid exposing secrets.
- Avoid disabling checks to make CI pass.
- Avoid making required checks optional without approval.
