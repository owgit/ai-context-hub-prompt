# Refresh

A context hub is a snapshot. Systems move; the snapshot does not. This file is how the hub stays true.

## Before Trusting This Hub

1. Read `generated_at` in `system-index.yaml`.
2. If the hub is older than the systems it describes, treat every entry as a claim rather than a fact.
3. Re-verify a fact against its `sources` entry before relying on it.

Every project in `system-index.yaml` carries a `sources` list. That is what makes re-checking cheap: you do not re-derive the fact, you re-read the one file it came from.

## When To Re-Run

- a repo is added, renamed, moved, or retired
- an environment or URL changes
- an integration is added or dropped
- an env var is introduced or rotated
- an item in `OPEN_QUESTIONS.md` gets answered

## How To Re-Run

1. Re-run the hub prompt against the same repos.
2. Compare the new output against this hub before overwriting anything.
3. Keep verified facts; replace stale ones; move newly discovered gaps into `OPEN_QUESTIONS.md`.
4. Update `generated_at`.

## Guardrails

- never keep a fact whose source file no longer exists
- never let an answered question stay in `OPEN_QUESTIONS.md`
- never let an unanswered one quietly disappear from it
