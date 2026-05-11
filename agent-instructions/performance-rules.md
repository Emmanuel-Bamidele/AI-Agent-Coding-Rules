# Performance Rules

## Correctness first

Do not sacrifice correctness or security for speed.

## Measure when possible

Before optimizing, identify evidence:

- Slow query
- Slow endpoint
- Large bundle
- High memory use
- Repeated computation
- N+1 query
- Re-render loop

## Common risks

Avoid:

- Unbounded database queries
- N+1 queries
- Loading entire tables into memory
- Unbounded parallelism
- Blocking work in request paths
- Large JSON responses
- Repeated expensive computation
- Missing pagination
- Cache without invalidation
- Frontend lists without virtualization
- Unoptimized image loading

## Database performance

Prefer:

- Pagination
- Selective columns
- Appropriate indexes
- Batching
- Joins/includes instead of loops
- Query limits
- Explain plans for complex queries

## API performance

Use:

- Timeouts for external calls
- Bounded retries
- Backoff
- Circuit breakers where appropriate
- Response size limits
- Streaming for large payloads where appropriate

## Frontend performance

Watch for:

- Large bundles
- Unnecessary re-renders
- Expensive calculations on every render
- Waterfall requests
- Unvirtualized large lists
- Images without sizing or optimization

## Caching

Only add caching when:

- Data freshness requirements are known
- Invalidation strategy is clear
- Cache key is correct
- Permission boundaries are respected
- Failure behavior is safe
