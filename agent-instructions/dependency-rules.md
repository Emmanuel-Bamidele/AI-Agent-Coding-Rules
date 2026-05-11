# Dependency Rules

## Dependencies are not free

Every dependency adds:

- Security risk
- Maintenance cost
- Install time
- Bundle size or runtime size
- Supply-chain exposure
- Version compatibility risk

## Before adding a dependency

Answer:

1. Is this already solved in the codebase?
2. Is this available in the standard library?
3. Is the dependency actively maintained?
4. Is the license acceptable?
5. Is the package size reasonable?
6. Does it add install scripts or native code?
7. Does it introduce many transitive dependencies?
8. Is it needed in production or only development?

## Prefer

- Existing project utilities
- Standard library
- Small maintained packages
- Well-known ecosystem libraries
- Explicit versioning
- Lockfiles

## Avoid

- Abandoned packages
- Packages for trivial helpers
- Multiple libraries for the same purpose
- Unpinned versions in critical environments
- Runtime dependencies for build-only tasks
- Large packages for small features
- Packages with suspicious install scripts

## When changing dependencies

- Update lockfiles.
- Run dependency install from scratch if possible.
- Run tests and build.
- Mention dependency changes in final response.
- Explain why the dependency is needed.

## Security

Run applicable audits when dependency changes are made:

```bash
npm audit
pnpm audit
pip-audit
cargo audit
govulncheck ./...
```
