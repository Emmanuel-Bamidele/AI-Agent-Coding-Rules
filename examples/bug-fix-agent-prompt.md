# Example Bug Fix Prompt

```text
Read `agent-instructions/AGENT.md`.

Bug:
Users can sometimes see invoices from another organization.

Task:
Find the root cause and fix it.

Constraints:
- Do not refactor unrelated code.
- Add a regression test proving cross-organization access is denied.
- Preserve existing API response format.
- Run relevant backend tests.

Before editing:
- Identify affected routes/services/queries.
- Explain the authorization boundary.

After editing:
- Use `agent-instructions/agent-response-format.md`.
```
