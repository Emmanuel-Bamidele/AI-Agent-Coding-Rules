# Example Feature Prompt

```text
Read `agent-instructions/AGENT.md`.

Feature:
Add a user profile display name field.

Requirements:
- Display name is optional.
- Maximum length is 80 characters.
- It must be editable from account settings.
- It must be returned from the current user API.

Constraints:
- Add validation on client and server.
- Add or update tests.
- Include migration if needed.
- Do not change unrelated account settings behavior.

After editing:
- Use `agent-instructions/agent-response-format.md`.
```
