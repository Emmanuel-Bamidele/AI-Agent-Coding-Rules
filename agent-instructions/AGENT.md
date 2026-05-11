# AGENT.md

This file defines how AI coding agents must work in this repository.

Read this file before making changes.

## Core mission

Make small, correct, secure, maintainable changes that respect the existing codebase.

The goal is not to produce the largest diff or the most clever solution. The goal is to solve the task safely and leave the repository healthier than before.

## Required behavior

Before editing:

1. Understand the task.
2. Inspect relevant files.
3. Identify affected boundaries.
4. Identify required tests.
5. Identify security, data, and compatibility risks.
6. Prefer the smallest safe change.

During editing:

1. Keep changes focused.
2. Follow existing patterns unless they are clearly unsafe.
3. Avoid unrelated refactors.
4. Avoid unnecessary dependencies.
5. Preserve public behavior unless asked to change it.
6. Add or update tests for behavior changes.
7. Update docs when behavior, setup, or interfaces change.

After editing:

1. Run relevant checks.
2. Report exactly what passed and failed.
3. Summarize files changed.
4. Explain risks and follow-up work.
5. Do not claim success if checks were not run or failed.

## Must read when relevant

- `agent-instructions/engineering-principles.md`
- `agent-instructions/coding-style.md`
- `agent-instructions/security-rules.md`
- `agent-instructions/testing-rules.md`
- `agent-instructions/architecture-rules.md`
- `agent-instructions/dependency-rules.md`
- `agent-instructions/performance-rules.md`
- `agent-instructions/database-rules.md`
- `agent-instructions/frontend-rules.md`
- `agent-instructions/backend-rules.md`
- `agent-instructions/ci-cd-rules.md`
- `agent-instructions/observability-rules.md`
- `agent-instructions/documentation-rules.md`
- `agent-instructions/git-rules.md`
- `agent-instructions/review-checklist.md`
- `agent-instructions/definition-of-done.md`

## Non-negotiable rules

- Do not invent requirements.
- Do not hide failing checks.
- Do not delete tests just because they fail.
- Do not suppress lint, type, or security warnings without explaining why.
- Do not commit secrets.
- Do not hardcode credentials.
- Do not weaken authentication or authorization.
- Do not make broad rewrites unless explicitly requested.
- Do not add dependencies without justification.
- Do not change public APIs without documenting compatibility impact.
- Do not ignore database migration risk.
- Do not log sensitive data.
- Do not return internal errors or stack traces to users.
- Do not use production services in tests unless explicitly configured and safe.

## Change-size policy

Prefer small patches.

A good patch usually does one thing:

- Fix one bug
- Add one feature
- Refactor one bounded area
- Add tests for one behavior
- Update one integration
- Repair one security issue

If the task requires multiple unrelated changes, split the plan and explain the order.

## Default priority order

When tradeoffs exist, prioritize:

1. Security
2. Data safety
3. Correctness
4. Backward compatibility
5. Maintainability
6. Observability
7. Performance
8. Developer experience
9. Style

## Final response

Use `agent-instructions/agent-response-format.md` for final responses.
