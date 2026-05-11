# Agent Code Standards

> Drop-in instructions, rules, and checklists that help AI coding agents write safer, cleaner, more maintainable code inside your repository.

AI coding agents can move quickly, but without clear rules they often produce inconsistent architecture, shallow tests, weak security, unnecessary dependencies, and broad risky diffs.

**Agent Code Standards** gives you a ready-to-copy set of files you can place in a codebase so agents understand how to work in the repository.

Use it with Codex, Claude Code, Cursor, GitHub Copilot, Devin-style agents, or any AI coding assistant that can read repository files.

---

## What this repository is for

This repository is for teams and solo developers who want AI agents to follow consistent engineering practices when editing code.

It helps agents:

- Understand project rules before making changes
- Keep patches small and reviewable
- Avoid invented requirements
- Avoid broad rewrites
- Add meaningful tests
- Preserve security boundaries
- Respect architecture decisions
- Avoid dependency bloat
- Document risky changes
- Run quality checks before claiming success
- Produce better pull request summaries

---

## Recommended files to copy into your codebase

For most repositories, copy this directory into your codebase:

```text
agent-instructions/
  AGENT.md
  engineering-principles.md
  coding-style.md
  security-rules.md
  testing-rules.md
  architecture-rules.md
  dependency-rules.md
  performance-rules.md
  database-rules.md
  frontend-rules.md
  backend-rules.md
  ci-cd-rules.md
  observability-rules.md
  documentation-rules.md
  git-rules.md
  review-checklist.md
  definition-of-done.md
  task-template.md
  pr-summary-template.md
  agent-response-format.md
  forbidden-patterns.md
  troubleshooting.md
```

Optional integrations:

```text
github/
  pull_request_template.md
  ISSUE_TEMPLATE/agent-task.md

cursor/
  rules/agent-code-standards.mdc

claude/
  CLAUDE.md

codex/
  instructions.md

vscode/
  copilot-instructions.md
```

---


## Where to put these files

Recommended visible layout inside your project:

```text
your-codebase/
  agent-instructions/
    AGENT.md
    security-rules.md
    testing-rules.md
    ...
```

Then tell your agent:

```text
Before editing this repository, read `agent-instructions/AGENT.md` and follow all rules in `agent-instructions/`.
```

## Should this folder be committed?

You have two good options.

### Option A: Commit it

Commit `agent-instructions/` if you want the rules to be shared by the whole team.

This is recommended for teams.

### Option B: Keep it local

Add it to `.gitignore` if these are personal instructions or you do not want them in the repository.

```gitignore
# Local AI agent instructions
agent-instructions/
```

If you keep the folder local, remember to copy it manually into each project where you want to use it.

## Quickstart

Copy the `agent` directory into your repository.

Then tell your coding agent:

```text
Before making changes, read `agent-instructions/AGENT.md`.

Follow all rules in `agent-instructions/`.

Do not modify files until you understand the task, constraints, risks, and required checks.
```

For a bug fix:

```text
Read `agent-instructions/AGENT.md` and `agent-instructions/task-template.md`.

Fix this bug with the smallest safe change.

Add a regression test.

Run relevant checks.

Return your response using `agent-instructions/agent-response-format.md`.
```

For a feature:

```text
Read `agent-instructions/AGENT.md`.

Implement this feature without broad rewrites.

Follow the architecture, security, testing, dependency, and documentation rules.

Keep the patch reviewable.
```

For a security-sensitive change:

```text
Read:
- `agent-instructions/AGENT.md`
- `agent-instructions/security-rules.md`
- `agent-instructions/testing-rules.md`
- `agent-instructions/review-checklist.md`

Before editing, identify the security boundary and the required negative tests.
```

---

## Suggested agent instruction

Add this to your coding agent's custom instructions:

```text
When working in this repository, always read `agent-instructions/AGENT.md` first.
Follow the repository-specific rules in `agent-instructions/`.
Do not make broad rewrites unless explicitly requested.
Prefer the smallest safe change.
Add tests for behavior changes.
Run relevant quality checks.
Report failures honestly.
```

---

## Why these files help

Agents perform better when rules are local, explicit, and actionable.

Instead of repeatedly telling your agent:

> “Please write good code, add tests, don’t break security, don’t refactor everything”

you can put those standards directly in the repo.

The agent can then read them every time it works.

---

## Best practices

Use these files as living documentation.

Update them when:

- Your architecture changes
- Your test strategy changes
- Your deployment process changes
- You add a new framework
- You add security requirements
- You discover repeated agent mistakes

---

## Repository title suggestion

```text
Agent Code Standards
```

## Repository description suggestion

```text
Drop-in rules and checklists that help AI coding agents write safer, cleaner, production-ready code.
```

## Tagline suggestion

```text
Give your AI coding agents a rulebook before they touch your code.
```

## Suggested GitHub topics

```text
ai
ai-agents
coding-agents
ai-code
code-quality
code-review
software-engineering
developer-tools
prompt-engineering
best-practices
testing
security
devsecops
ci-cd
technical-debt
```

---

## License

MIT is recommended if you want people to freely copy these files into their repositories.
