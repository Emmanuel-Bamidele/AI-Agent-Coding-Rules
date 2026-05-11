# Quickstart

## 1. Copy files

Copy `agent-instructions/` into your codebase.

Optional: also copy `cursor/`, `claude/`, `codex/`, `vscode/`, and `github/` integrations depending on your tools.

## 2. Tell your agent

```text
Before editing, read `agent-instructions/AGENT.md`.
Follow all rules in `agent-instructions/`.
```

## 3. Use task template

For every non-trivial change, ask the agent to follow:

```text
agent-instructions/task-template.md
```

## 4. Require final response format

Ask the agent to respond using:

```text
agent-instructions/agent-response-format.md
```

## 5. Review against definition of done

Before merging, compare the result with:

```text
agent-instructions/definition-of-done.md
```
