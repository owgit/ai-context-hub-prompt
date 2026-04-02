# Environments

| System | Local | Staging | Production |
| --- | --- | --- | --- |
| frontend-app | `http://localhost:3000` | `https://staging.example.com` | `https://example.com` |
| crm-system | `https://crm.local:4443` | unverified | `https://crm.example.com` |
| automation-worker | `http://localhost:5001` | unverified | `https://automation.example.com` |

## Notes

- mark missing data as `unverified`
- keep local and production clearly separated
- do not infer staging if it is not documented

