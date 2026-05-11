# Security Rules

Security is mandatory for every change.

## Input trust

Treat all external input as untrusted:

- HTTP bodies
- Query parameters
- Path parameters
- Headers
- Cookies
- Webhooks
- CLI arguments
- File uploads
- Environment variables
- Third-party API responses
- Database values created by users
- Message queue payloads

Validate data at boundaries.

## Authentication

- Do not bypass authentication.
- Do not trust client-provided user IDs.
- Do not trust identity headers unless set by trusted infrastructure.
- Verify token signatures.
- Enforce session expiration.
- Use secure password hashing when passwords are handled.
- Keep reset tokens single-use and time-limited.

## Authorization

Authentication is not authorization.

For every read, update, delete, export, or share operation:

- Check object-level permissions.
- Enforce tenant, organization, workspace, or account boundaries.
- Do not rely only on frontend checks.
- Do not leak resource existence when access is forbidden.
- Add negative tests for unauthorized access.

## Secrets

Never commit:

- API keys
- Tokens
- Passwords
- Private keys
- OAuth secrets
- Database URLs with credentials
- Cloud credentials
- Webhook signing secrets

Use `.env.example` with fake values.

Ensure real `.env` files are ignored.

## Injection prevention

Avoid:

- Raw SQL string interpolation
- Shell command interpolation
- Unsafe template rendering
- Unsafe regular expressions from user input
- `eval`
- Dynamic imports from user input
- Unsafe HTML insertion

Use:

- Parameterized queries
- Allowlisted values
- Safe escaping
- Runtime validation
- `execFile` instead of shell strings

## File uploads

Validate:

- Size
- MIME type
- Extension
- Magic bytes where needed
- Storage location
- Path traversal
- Public/private access
- Filename normalization

Never trust the original filename.

## Webhooks

- Verify signatures.
- Validate timestamps where supported.
- Prevent replay attacks where possible.
- Make processing idempotent.
- Validate payload shape.
- Log safely.

## Logging

Do not log:

- Passwords
- Tokens
- Cookies
- Authorization headers
- Private keys
- Payment details
- Full sensitive request bodies
- Personal data unless necessary and safe

## Rate limiting

Consider rate limits for:

- Login
- Signup
- Password reset
- Invite flows
- File upload
- Search
- Expensive endpoints
- Webhook endpoints where appropriate

## Security-sensitive changes

If a change affects authentication, authorization, payments, secrets, encryption, user data, or infrastructure permissions, explicitly call it out in the final response.
