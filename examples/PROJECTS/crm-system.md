# CRM System

## Purpose

Operational source of truth for customers, internal workflows, and ticket state.

## Entrypoints

- Local path: `/Users/example/Sites/crm-system`
- Local URL: `https://crm.local:4443`
- Production URL: `https://crm.example.com`

## Integrations

| Integration | Direction | Touchpoint |
| --- | --- | --- |
| SMTP | outbound | mail delivery |
| automation-worker | outbound | workflow trigger |
| mail-automation | outbound | ticket and outreach sync |

## Inbound Data Flows

- internal users -> CRM updates
- webhooks -> lead and ticket updates

## Outbound Data Flows

- lead state -> automation worker
- CRM ticket -> mail automation

## Auth Source Locations

- `.env`
- shell profile
- secret manager

## Constraints

- this is the source of truth for customer data — no other system may write it
- never run migrations against the production database
- outbound mail is triggered by real ticket state — never test against production

## Read First Inside Repo

- `README.md`
- `docs/integrations.md`
- `docs/workflows.md`

