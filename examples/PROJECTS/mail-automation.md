# Mail Automation

## Purpose

Outbound mail and outreach sequencing driven by CRM ticket state.

## Entrypoints

- Local path: unverified
- Local URL: unverified
- Production URL: unverified

## Integrations

| Integration | Direction | Touchpoint |
| --- | --- | --- |
| crm-system | inbound | ticket and outreach state |
| SMTP | outbound | mail delivery |

## Inbound Data Flows

- CRM ticket -> outbound mail

## Outbound Data Flows

- mail delivery -> SMTP provider

## Auth Source Locations

- unverified

## Constraints

- this system sends real mail to real people — never trigger it from a test or local run
- never write back to `crm-system`

## Read First Inside Repo

- unverified
