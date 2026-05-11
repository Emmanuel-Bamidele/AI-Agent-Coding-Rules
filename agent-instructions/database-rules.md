# Database Rules

Database changes are high risk.

## Schema changes

Before changing schema, consider:

- Existing data
- Migration order
- Downtime risk
- Rollback plan
- Backfill strategy
- Index build impact
- Compatibility with old application versions

## Migration safety

Avoid unsafe migrations such as:

- Adding `NOT NULL` columns without defaults/backfill
- Dropping columns immediately
- Renaming columns without compatibility
- Rewriting large tables in one step
- Deleting data without backup
- Changing enum values unsafely
- Adding blocking indexes on large tables

## Safer pattern

Use phased migrations:

1. Add nullable column/table.
2. Deploy compatible code.
3. Backfill in batches.
4. Verify.
5. Enforce constraints.
6. Remove old path later.

## Transactions

Use transactions for multi-step changes that must be atomic.

Examples:

- Payment updates
- Inventory updates
- Account creation
- Permission changes
- Multi-table writes
- Audit log plus sensitive mutation

## Constraints

Prefer database constraints for important invariants:

- Foreign keys
- Unique constraints
- Not-null constraints
- Check constraints
- Indexes for uniqueness and lookup

## Query safety

Avoid:

- Raw SQL interpolation
- Unbounded queries
- Missing tenant/org filters
- Loading large tables into memory
- Silent write failures

## Data types

Be careful with:

- Currency and decimal precision
- Time zones
- Case-insensitive uniqueness
- JSON columns
- Soft deletes
- Enum evolution
