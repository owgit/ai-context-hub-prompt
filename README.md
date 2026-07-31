# AI Context Hub Prompt

Your AI knows your repo.

This prompt helps it understand your system.

`AI Context Hub Prompt` is a copy-paste prompt for Codex, Claude Code, and Cursor that tells an AI IDE to build a read-only cross-repo context hub from verified local sources.

The point is simple:

- stop repeating your architecture in every session
- stop losing context between repos
- give your AI a system map instead of a folder view

## What Problem This Solves

Most AI coding tools are repo-native.

They work well inside one codebase, then fall apart when the task touches:

- multiple repos
- local and production environments
- internal tools
- third-party integrations
- auth and secret boundaries

That is where teams start re-explaining the same system over and over again.

This prompt tells the AI to build a small, machine-readable context layer so it can understand the wider stack without touching app code or exposing secrets.

## What It Generates

The prompt tells the AI to generate:

- `README.md`
- `BOOTSTRAP.md`
- `SYSTEM_MAP.md`
- `system-index.yaml`
- `ENVIRONMENTS.md`
- `SECRETS_INDEX.md`
- `OPEN_QUESTIONS.md`
- `REFRESH.md`
- `PROJECTS/*.md`
- `INTEGRATIONS/*.md`
- `RUNBOOKS/*.md`

It also tells the AI to generate optional bridge snippets for:

- `AGENTS.md`
- `CLAUDE.md`
- Cursor memory files

## Safety Model

This is intentionally conservative.

- read-only docs only
- verified facts only
- no plaintext secrets
- no passwords, tokens, or copied connection strings
- secret values are never even read into context, only variable names
- ask before patching existing AI instruction files
- do not modify application code

The generated hub is a map, not an automation system.

## Who This Is For

This is for people who work across more than one repo and want their AI IDE to understand:

- where systems live
- how they connect
- what depends on what
- which environment is which
- where auth comes from

It is especially useful for:

- founders
- operators
- technical generalists
- indie hackers
- teams with internal tools and external services

## Works With

- Codex
- Claude Code
- Cursor

## How To Use

1. Open your AI IDE in any relevant repo.
2. Copy the prompt from [`PROMPT.md`](PROMPT.md).
3. Paste it into Codex, Claude Code, or Cursor.
4. Point the AI at the repos and systems you want mapped.
5. Let it scan docs, configs, workflow files, env filenames, and env key names.
6. When asked `Where should the hub be saved?`, choose the target folder.
7. Review the generated hub before allowing any bridge patches.

## Example Output

The `examples/` folder shows the shape of the generated hub:

- [`examples/BOOTSTRAP.md`](examples/BOOTSTRAP.md)
- [`examples/system-index.yaml`](examples/system-index.yaml)
- [`examples/SYSTEM_MAP.md`](examples/SYSTEM_MAP.md)
- [`examples/ENVIRONMENTS.md`](examples/ENVIRONMENTS.md)
- [`examples/SECRETS_INDEX.md`](examples/SECRETS_INDEX.md)
- [`examples/OPEN_QUESTIONS.md`](examples/OPEN_QUESTIONS.md)
- [`examples/REFRESH.md`](examples/REFRESH.md)
- [`examples/PROJECTS/frontend-app.md`](examples/PROJECTS/frontend-app.md)
- [`examples/PROJECTS/crm-system.md`](examples/PROJECTS/crm-system.md)
- [`examples/PROJECTS/automation-worker.md`](examples/PROJECTS/automation-worker.md)
- [`examples/PROJECTS/mail-automation.md`](examples/PROJECTS/mail-automation.md)
- [`examples/INTEGRATIONS/vercel.md`](examples/INTEGRATIONS/vercel.md)
- [`examples/RUNBOOKS/deploy.md`](examples/RUNBOOKS/deploy.md)
- [`examples/RUNBOOKS/local-dev.md`](examples/RUNBOOKS/local-dev.md)

## Included Files

- [`PROMPT.md`](PROMPT.md): the main copy-paste prompt
- [`examples/`](examples/): sample output structure
- [`launch/linkedin-post.md`](launch/linkedin-post.md): short launch copy

## One-Line Pitch

Your AI knows your repo. This prompt helps it understand your system.
