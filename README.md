# AI Context Hub Prompt

A copy-paste prompt that helps an AI IDE build a read-only cross-repo context hub.

The goal is simple: your AI should understand the real system around your code, not just the current repo.

## Works with

- Codex
- Claude Code
- Cursor

## What it creates

The prompt tells the AI to generate a context hub with:

- `README.md`
- `BOOTSTRAP.md`
- `SYSTEM_MAP.md`
- `system-index.yaml`
- `ENVIRONMENTS.md`
- `SECRETS_INDEX.md`
- `PROJECTS/*.md`
- `INTEGRATIONS/*.md`
- `RUNBOOKS/*.md`

It also tells the AI to generate optional bridge snippets for `AGENTS.md`, `CLAUDE.md`, or Cursor memory files.

## Safety rules

- read-only docs only
- no plaintext secrets
- no passwords, tokens, or copied connection strings
- verified facts only
- ask before patching existing AI instruction files
- do not modify application code

## How to use

1. Open your AI IDE in any relevant repo.
2. Copy the prompt from [`PROMPT.md`](/Users/uygarduzgun/Sites/ai-context-hub-prompt/PROMPT.md).
3. Paste it into Codex, Claude Code, or Cursor.
4. Point the AI to the repos and systems you want mapped.
5. Let it scan docs, configs, and env key names.
6. When asked `Where should the hub be saved?`, choose the target folder.
7. Review the generated hub before applying any bridge snippets.

## Included files

- [`PROMPT.md`](/Users/uygarduzgun/Sites/ai-context-hub-prompt/PROMPT.md): the main copy-paste prompt
- [`examples/BOOTSTRAP.md`](/Users/uygarduzgun/Sites/ai-context-hub-prompt/examples/BOOTSTRAP.md): sample bootstrap router
- [`examples/system-index.yaml`](/Users/uygarduzgun/Sites/ai-context-hub-prompt/examples/system-index.yaml): sample machine-readable index
- [`examples/SYSTEM_MAP.md`](/Users/uygarduzgun/Sites/ai-context-hub-prompt/examples/SYSTEM_MAP.md): sample architecture map
- [`examples/ENVIRONMENTS.md`](/Users/uygarduzgun/Sites/ai-context-hub-prompt/examples/ENVIRONMENTS.md): sample environment matrix
- [`examples/SECRETS_INDEX.md`](/Users/uygarduzgun/Sites/ai-context-hub-prompt/examples/SECRETS_INDEX.md): sample secret references file
- [`examples/PROJECTS/frontend-app.md`](/Users/uygarduzgun/Sites/ai-context-hub-prompt/examples/PROJECTS/frontend-app.md): sample project card
- [`examples/PROJECTS/crm-system.md`](/Users/uygarduzgun/Sites/ai-context-hub-prompt/examples/PROJECTS/crm-system.md): sample project card
- [`examples/INTEGRATIONS/vercel.md`](/Users/uygarduzgun/Sites/ai-context-hub-prompt/examples/INTEGRATIONS/vercel.md): sample integration card
- [`examples/RUNBOOKS/deploy.md`](/Users/uygarduzgun/Sites/ai-context-hub-prompt/examples/RUNBOOKS/deploy.md): sample deploy runbook
- [`examples/RUNBOOKS/local-dev.md`](/Users/uygarduzgun/Sites/ai-context-hub-prompt/examples/RUNBOOKS/local-dev.md): sample local dev runbook
- [`launch/linkedin-post.md`](/Users/uygarduzgun/Sites/ai-context-hub-prompt/launch/linkedin-post.md): short launch copy

## One-line pitch

Your AI knows your repo. This prompt helps it understand your system.
