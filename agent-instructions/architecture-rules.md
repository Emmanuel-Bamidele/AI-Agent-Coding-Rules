# Architecture Rules

## Respect existing architecture

Before adding a new pattern, inspect existing patterns.

Use existing architecture unless it is clearly unsafe or unsuitable.

## Avoid architecture drift

Do not introduce a second way to do the same thing without justification.

Watch for duplicate:

- API clients
- Auth helpers
- Config loaders
- Loggers
- Validators
- Error types
- Database wrappers
- State managers
- Formatting helpers
- Permission checks

## Boundaries

Keep boundaries clear.

Typical backend boundaries:

```text
routes/controllers
application services
domain logic
repositories/persistence
external integrations
```

Typical frontend boundaries:

```text
routes/pages
features
components
hooks
api clients
state
utils
```

Adapt to the existing project.

## Business logic

Do not scatter business logic across:

- UI components
- Controllers
- Database models
- Utility files
- Inline route handlers

Prefer central service/domain functions.

## Dependency direction

Higher-level code may depend on lower-level abstractions.

Avoid circular dependencies.

Avoid low-level modules importing UI, route, or framework-specific code unless that is the established pattern.

## Refactoring

Refactor only when:

- It directly supports the task
- It reduces clear risk
- It improves testability
- It removes duplication safely
- It is small enough to review

Do not rewrite entire subsystems unless explicitly requested.

## Deleting code

Delete code only when you can show it is unused or replaced.

If unsure, mark as follow-up instead of deleting.
