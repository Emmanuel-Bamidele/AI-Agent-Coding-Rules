# Agent Task Template

Use this template when asking an AI coding agent to make a change.

```text
Read `agent-instructions/AGENT.md` before making changes.

Task:
<describe the task>

Context:
<include relevant requirements, links, logs, screenshots, or examples>

Constraints:
- Keep the change focused.
- Do not refactor unrelated code.
- Do not add dependencies unless justified.
- Preserve existing public behavior unless explicitly changed.
- Add or update tests.
- Run relevant checks.
- Report failures honestly.

Before editing:
- Inspect relevant files.
- Explain the likely change.
- Identify risks.
- Identify tests to add or run.

After editing:
- Summarize changed files.
- List tests/checks run.
- Explain remaining risks.
- Use `agent-instructions/agent-response-format.md`.
```
