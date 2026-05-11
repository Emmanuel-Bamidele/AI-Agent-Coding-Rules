# Coding Style Rules

## General

- Match the existing style of the repository.
- Prefer clear names over short names.
- Prefer simple functions with one responsibility.
- Avoid deeply nested logic.
- Avoid clever one-liners when readability suffers.
- Remove dead code when it is clearly unused.
- Do not add comments that merely repeat the code.
- Add comments when explaining non-obvious decisions or tradeoffs.

## Naming

Use names that describe intent:

Good:

```text
validateInvoiceOwner
calculateRetryDelay
sendPasswordResetEmail
```

Bad:

```text
handleThing
doStuff
processData
finalFix
newLogic
```

## Functions

A function should generally:

- Do one thing
- Have clear inputs and outputs
- Avoid hidden global state
- Validate assumptions at boundaries
- Return meaningful errors or results
- Be testable without excessive mocking

## Error handling

- Do not swallow errors.
- Do not throw strings.
- Do not expose internal stack traces to users.
- Convert internal errors to safe external responses at the boundary.
- Include enough context in logs to debug.
- Redact sensitive data.

## Types

When using typed languages:

- Prefer precise types.
- Avoid `any` unless unavoidable.
- Avoid unsafe casts.
- Avoid suppressing type errors.
- Model impossible states as impossible where practical.
- Validate runtime input even if static types exist.

## Comments

Good comments explain why:

```text
// We use a stable sort here because invoice ordering is part of the public export contract.
```

Bad comments restate what:

```text
// Increment i by 1
```

## Formatting

Use the existing formatter.

Do not reformat unrelated files.
