# Frontend App

## Purpose

Public site and user-facing application.

## Entrypoints

- Local path: `/Users/example/Sites/frontend-app`
- Local URL: `http://localhost:3000`
- Production URL: `https://example.com`

## Integrations

| Integration | Direction | Touchpoint |
| --- | --- | --- |
| CMS | inbound | content fetch |
| Supabase | inbound | data reads |
| Vercel | hosting | deployment target |

## Inbound Data Flows

- CMS content -> page rendering
- Supabase data -> frontend UI

## Outbound Data Flows

- user actions -> API calls
- deployment builds -> Vercel

## Auth Source Locations

- `.env.local`
- Vercel project environment

## Read First Inside Repo

- `README.md`
- `AGENTS.md`
- `docs/architecture.md`

