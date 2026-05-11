# Git Rules

## Branches

Use focused branches.

Good names:

```text
fix/authz-invoice-access
test/payment-webhook-regression
chore/remove-unused-deps
```

## Commits

Commits should be focused and descriptive.

Good:

```text
fix: enforce organization scope on invoice lookup
test: add regression coverage for invalid webhook signatures
chore: remove unused date dependency
```

Bad:

```text
fix stuff
updates
agent changes
final
```

## Pull requests

Pull requests should:

- Explain what changed
- Explain why
- Link findings or issues
- Include tests run
- Call out risks
- Mention migrations
- Mention security-sensitive changes
- Be small enough to review

## Avoid

- Mixing formatting with logic changes
- Combining unrelated changes
- Huge generated diffs
- Silent dependency upgrades
- Force pushing over reviewer feedback without explanation
