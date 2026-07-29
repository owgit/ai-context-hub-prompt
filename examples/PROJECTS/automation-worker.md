# Automation Worker

## Purpose

Downstream workflow processor that reacts to CRM state changes.

## Entrypoints

- Local path: unverified
- Local URL: `http://localhost:5001`
- Production URL: `https://automation.example.com`

## Integrations

| Integration | Direction | Touchpoint |
| --- | --- | --- |
| crm-system | inbound | lead and ticket state |
| CMS | outbound | content updates |

## Inbound Data Flows

- CRM lead state -> workflow execution

## Outbound Data Flows

- workflow output -> CMS content update

## Auth Source Locations

- unverified

## Constraints

- never write back to `crm-system` — it is the source of truth, this worker is downstream
- never run against production CRM state while testing

## Read First Inside Repo

- unverified
