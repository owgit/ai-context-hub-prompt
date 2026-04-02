# Secrets Index

## Rules

- names and locations only
- never include secret values

| Env Var | Location | Owner | Usage Note |
| --- | --- | --- | --- |
| `NEXT_PUBLIC_SUPABASE_URL` | `.env.local` | frontend-app | public client configuration |
| `NEXT_PUBLIC_SUPABASE_ANON_KEY` | `.env.local` | frontend-app | public read access |
| `CRM_API_KEY` | shell profile | crm-system | API auth for automation flows |
| `SMTP_PASSWORD` | secret manager | crm-system | outbound mail delivery |

