# Example Refactor Prompt

```text
Read `agent-instructions/AGENT.md` and `agent-instructions/architecture-rules.md`.

Refactor task:
Consolidate duplicate API client logic.

Constraints:
- Do not change public API behavior.
- Do not modify unrelated modules.
- Add tests or update existing tests.
- Keep the diff small enough to review.
- Explain why the selected API client pattern is preferred.

Before editing:
- List duplicate implementations.
- Identify callers.
- Propose a migration plan.

After editing:
- Use `agent-instructions/agent-response-format.md`.
```
