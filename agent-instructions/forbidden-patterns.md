# Forbidden Patterns

Avoid these patterns unless explicitly justified.

## Security

```text
Hardcoded secrets
Trusting client-provided user IDs
Authorization only in frontend
Raw SQL interpolation
Shell command interpolation
Unsafe innerHTML
eval on user input
Logging tokens or cookies
```

## Error handling

```text
Empty catch blocks
Returning success after failure
Throwing strings
Catching every error without rethrowing or logging
Leaking stack traces to users
```

## Testing

```text
Deleting failing tests without replacement
Mocking the function under test
Tests with no assertions
Tests that only assert implementation details
Production credentials in tests
```

## Architecture

```text
Adding a second auth system
Adding a second config loader
Adding duplicate API clients
Circular dependencies
Business logic scattered across UI/controllers
Large unrelated rewrites
```

## Dependencies

```text
Adding packages for trivial helpers
Silent major upgrades
Runtime dependency for dev-only use
Unmaintained packages
Ignoring lockfile updates
```

## Data

```text
Destructive migrations without staged rollout
Adding NOT NULL columns without backfill
Dropping data without backup
Missing tenant filters in queries
Unbounded table reads
```
