# Review Checklist

Use this before considering a change complete.

## Scope

- [ ] Does the change solve the requested task?
- [ ] Is the diff focused?
- [ ] Are unrelated refactors avoided?
- [ ] Are public behavior changes documented?

## Correctness

- [ ] Are edge cases handled?
- [ ] Are null/empty/error states handled?
- [ ] Are async operations handled correctly?
- [ ] Are errors surfaced appropriately?
- [ ] Is the code deterministic?

## Security

- [ ] Are inputs validated?
- [ ] Is authentication preserved?
- [ ] Is authorization enforced?
- [ ] Are secrets protected?
- [ ] Are logs redacted?
- [ ] Are injection risks avoided?
- [ ] Are sensitive operations tested negatively?

## Tests

- [ ] Are tests added or updated?
- [ ] Do tests verify behavior?
- [ ] Is there a regression test for bug fixes?
- [ ] Are flaky or fake tests avoided?
- [ ] Were relevant tests run?

## Data

- [ ] Are migrations safe?
- [ ] Are transactions used where needed?
- [ ] Are constraints correct?
- [ ] Is rollback considered?

## Dependencies

- [ ] Are new dependencies justified?
- [ ] Is the lockfile updated?
- [ ] Are vulnerabilities considered?

## Performance

- [ ] Are queries bounded?
- [ ] Is pagination used where needed?
- [ ] Are external calls timed out?
- [ ] Is caching safe if added?

## Operations

- [ ] Are logs useful?
- [ ] Are metrics/alerts considered?
- [ ] Are health checks affected?

## Documentation

- [ ] Are docs updated when needed?
- [ ] Are new commands/configs documented?
