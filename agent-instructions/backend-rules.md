# Backend Rules

Apply these rules when editing backend code.

## Request handling

Every endpoint should:

- Authenticate when protected
- Authorize resource access
- Validate inputs
- Return safe errors
- Log useful context
- Avoid leaking internals
- Use consistent response formats

## Authorization

Check permissions close to the data or service boundary.

Never trust:

- Client-provided user IDs
- Client-provided organization IDs
- Frontend-only checks
- Hidden form fields
- Unverified headers

## Services

Service functions should:

- Encapsulate business logic
- Avoid direct HTTP assumptions unless they are transport-specific
- Be testable
- Return meaningful results or errors
- Use transactions when needed

## External integrations

External calls should have:

- Timeouts
- Bounded retries
- Backoff
- Error handling
- Safe logging
- Idempotency where side effects exist

## Webhooks

Webhook handlers should:

- Verify signature
- Validate payload
- Be idempotent
- Handle retries
- Avoid duplicate side effects
- Log event IDs

## Jobs

Background jobs should:

- Be idempotent
- Have bounded retries
- Record failure reasons
- Avoid infinite loops
- Avoid unbounded concurrency
- Expose operational visibility

## Errors

Do not expose internal exceptions to users.

Map internal errors to safe external responses.

## Rate limits

Consider rate limits for sensitive or expensive endpoints.
