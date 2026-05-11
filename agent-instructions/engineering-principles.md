# Engineering Principles

## 1. Correctness first

Code should do the right thing in normal cases, edge cases, and failure cases.

Do not optimize, abstract, or polish code that is still incorrect.

## 2. Security is a default requirement

Every change must preserve or improve security.

Inputs are untrusted. Permissions must be checked. Secrets must stay secret.

## 3. Small changes are safer

Prefer small, reviewable patches.

Do not combine unrelated work.

## 4. Explicit is better than implicit

Make assumptions visible through:

- Types
- Validation
- Tests
- Names
- Documentation
- Assertions where appropriate

## 5. Boring code is good code

Prefer simple, predictable code over clever abstractions.

Optimize for the next engineer reading the code.

## 6. Tests should prove behavior

Tests should verify user-visible or system-visible behavior, not internal implementation details.

## 7. Dependencies are liabilities

Every dependency adds maintenance, security, and supply-chain risk.

Use existing utilities or standard library when appropriate.

## 8. Fail safely

When something goes wrong:

- Do not corrupt data.
- Do not leak sensitive information.
- Do not silently pretend success.
- Do not leave the system in an inconsistent state.

## 9. Preserve compatibility

Avoid breaking public APIs, data formats, migrations, CLI behavior, or configuration without explicit approval.

## 10. Leave a trail

Important decisions should be understandable later.

Use comments for non-obvious reasoning, not for restating code.
