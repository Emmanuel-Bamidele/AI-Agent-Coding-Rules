# Testing Rules

## Test behavior, not implementation

Tests should prove what the system does.

Prefer:

```text
User cannot access another organization's invoice.
```

Over:

```text
authorizeInvoiceAccess was called once.
```

## Required tests

Add or update tests when changing:

- Business logic
- API behavior
- Validation
- Authentication
- Authorization
- Database writes
- Migrations
- External integrations
- Error handling
- Frontend user flows
- Bug fixes

## Regression tests

Every bug fix should include a regression test unless impossible.

If no test is added, explain why.

## Test types

Use the right level:

- Unit tests for pure logic
- Integration tests for database and service boundaries
- API tests for request/response behavior
- End-to-end tests for critical user flows
- Security negative tests for permission boundaries
- Migration tests for schema changes

## Bad tests

Avoid tests that:

- Only assert mocks
- Mock the function being tested
- Duplicate implementation logic
- Have no meaningful assertion
- Depend on test order
- Depend on local hidden state
- Require production credentials
- Call real paid services unintentionally
- Use broad snapshots as the only assertion

## Test data

Use realistic data.

Include:

- Normal case
- Edge case
- Invalid input
- Unauthorized case where relevant
- Empty state where relevant
- Failure case where relevant

## Flaky tests

Do not ignore flaky tests.

Fix causes such as:

- Timing assumptions
- Shared state
- Random order
- Network dependency
- Timezone dependency
- Uncontrolled concurrency

## Running tests

Run the smallest relevant test first.

Then run broader checks when practical.

Report exactly what was run and what happened.
