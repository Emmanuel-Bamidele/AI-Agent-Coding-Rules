# Observability Rules

## Goal

Production issues should be diagnosable.

## Logging

Use structured logs where available.

Include useful context:

- Request ID
- User ID or tenant ID when safe
- Resource ID
- Operation name
- Error object
- Duration for slow operations

Do not log sensitive data.

## Metrics

Consider metrics for:

- Request count
- Error rate
- Latency
- Job success/failure
- Queue depth
- External API latency
- Database latency
- Cache hit rate
- Rate limit events
- Webhook failures

## Tracing

For distributed or multi-step flows, preserve correlation IDs.

## Health checks

Separate:

- Liveness: process is alive
- Readiness: service can handle traffic

Readiness may check:

- Database connection
- Queue connection
- Required migrations
- Critical dependencies

## Audit logs

Use audit logs for sensitive actions:

- Permission changes
- Account changes
- Data exports
- Billing changes
- Security settings
- Admin actions

Audit logs should be durable and safe.
