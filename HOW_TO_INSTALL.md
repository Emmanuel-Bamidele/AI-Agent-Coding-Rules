# How to Install

This ZIP uses visible folder names so the files are easy to see on your computer.

## Recommended folder name

Put the main rules folder in your codebase as:

```text
agent-instructions/
```

Recommended project layout:

```text
your-codebase/
  agent-instructions/
    AGENT.md
    engineering-principles.md
    coding-style.md
    security-rules.md
    testing-rules.md
    architecture-rules.md
    ...
```

Then tell your coding agent:

```text
Before editing this repository, read `agent-instructions/AGENT.md` and follow all rules in `agent-instructions/`.
```

## Should you add it to `.gitignore`?

You have two options.

### Option A: Commit the folder

Commit `agent-instructions/` if you want the rules to be shared by everyone working on the repository.

This is best for teams, open-source projects, and projects where you want consistent agent behavior.

### Option B: Keep the folder local

Add `agent-instructions/` to `.gitignore` if the instructions are only for your personal workflow.

Add this to your `.gitignore`:

```gitignore
# Local AI agent instructions
agent-instructions/
```

Do not forget this step if you do not want the folder committed.

## Optional tool-specific folders

This ZIP also includes visible versions of tool-specific folders:

```text
github/
cursor/
claude/
codex/
vscode/
```

Some tools expect dotfolders. If you want native tool support, rename these after copying:

```text
github  -> .github
cursor  -> .cursor
claude  -> .claude
codex   -> .codex
vscode  -> .vscode
```

The main folder can also be renamed if you prefer hidden instructions:

```text
agent-instructions -> .agent
```

## Showing hidden folders

On macOS Finder:

```text
Command + Shift + .
```

On Windows File Explorer:

```text
View -> Show -> Hidden items
```
