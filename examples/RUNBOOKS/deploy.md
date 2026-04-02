# Deploy Runbook

## Purpose

Describe the verified deployment path for each system.

## Example Steps

1. Confirm the target environment.
2. Read the relevant project card.
3. Read the deployment workflow file or platform docs.
4. Verify whether deploy is manual, CI-based, or CLI-based.
5. Stop if any part of the deploy path is unverified.

## Guardrails

- never assume production deploy steps
- never expose secret values
- keep platform-specific instructions in the owning repo when possible

