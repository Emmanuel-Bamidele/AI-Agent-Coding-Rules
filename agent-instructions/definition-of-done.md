# Definition of Done

A change is done only when the following are true.

## Required

- [ ] The requested task is completed.
- [ ] The change is focused.
- [ ] Relevant tests were added or updated.
- [ ] Relevant checks were run.
- [ ] Failures are reported honestly.
- [ ] Security impact was considered.
- [ ] Data impact was considered.
- [ ] Documentation was updated if needed.
- [ ] Final response includes changed files, tests run, and risks.

## For bug fixes

- [ ] The bug is reproduced or explained.
- [ ] A regression test was added where practical.
- [ ] The fix addresses root cause, not only symptoms.

## For features

- [ ] Behavior matches requirements.
- [ ] Edge cases are handled.
- [ ] Tests cover main paths and failure paths.
- [ ] Docs or examples are updated if needed.

## For security changes

- [ ] Negative tests exist.
- [ ] No sensitive data is logged.
- [ ] Auth/authz is not weakened.
- [ ] Secrets are not committed.
- [ ] Risk is explained.

## For database changes

- [ ] Migration is safe for existing data.
- [ ] Rollback or recovery is considered.
- [ ] Constraints and indexes are appropriate.
- [ ] Backfills are safe if needed.

## For dependency changes

- [ ] Dependency is justified.
- [ ] Lockfile is updated.
- [ ] Audit impact is considered.
