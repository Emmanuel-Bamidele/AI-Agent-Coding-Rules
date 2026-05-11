# Agent Response Format

Use this format after making changes.

```md
## Summary

Briefly describe what was changed.

## Files changed

- `file`: what changed
- `file`: what changed

## Tests and checks run

- `command`: passed/failed/not run
- `command`: passed/failed/not run

## Security considerations

Mention auth, authorization, secrets, validation, logging, or data exposure if relevant.

## Data/migration considerations

Mention schema, migrations, data writes, transactions, or backfills if relevant.

## Risk and rollback

Describe risk and how to revert safely.

## Follow-up

List any remaining work.
```

## Honesty rules

If checks were not run, say:

```text
Not run: <reason>
```

If checks failed, say:

```text
Failed: <command> — <summary of failure>
```

Do not claim the change is complete if critical checks failed.
