# BOOTSTRAP

## Purpose

This context hub helps an AI understand the wider system across multiple repos, environments, and integrations.

## Read Order

1. Read `system-index.yaml`.
2. Read the relevant file in `PROJECTS/`.
3. Read the relevant file in `INTEGRATIONS/`.
4. Read `ENVIRONMENTS.md` and `SECRETS_INDEX.md` if the task touches config or auth.

## Routing

- deploy tasks -> `RUNBOOKS/deploy.md`
- data-flow tasks -> `SYSTEM_MAP.md` + relevant `PROJECTS/*.md`
- environment tasks -> `ENVIRONMENTS.md` + `SECRETS_INDEX.md`
- integration tasks -> relevant `INTEGRATIONS/*.md` + related `PROJECTS/*.md`

## Guardrails

- read-only docs only
- verified facts only
- never expose plaintext secrets
- never assume missing values

