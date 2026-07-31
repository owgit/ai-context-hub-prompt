# Open Questions

Everything this hub could not verify.

Each item is a claim an AI must not make until it is answered. Nothing here is a guess waiting to be confirmed — it is a gap that was left honest on purpose.

## automation-worker

Mapped indirectly from `crm-system/docs/integrations.md`. The repo itself was never scanned.

- [ ] Local path unknown — confirm by locating the repo on disk
- [ ] Stack unknown — confirm from the repo's package manifest
- [ ] Env sources and secret refs unknown — confirm from env filenames in the repo
- [ ] Auth source locations unknown — confirm from the repo README
- [ ] Staging URL unknown — confirm with whoever owns deployment

## mail-automation

Mapped indirectly from `crm-system/docs/workflows.md`. The repo itself was never scanned.

- [ ] Local path, local URL, and production URL all unknown — confirm by locating the repo on disk
- [ ] Stack unknown — confirm from the repo's package manifest
- [ ] Env sources and secret refs unknown — confirm from env filenames in the repo
- [ ] Auth source locations unknown — confirm from the repo README

## crm-system

- [ ] Staging environment unknown — confirm with whoever owns deployment, or record that no staging exists

## How To Close An Item

1. Verify the fact from a real local source.
2. Write it into the hub.
3. Add the source to that project's `sources` list in `system-index.yaml`.
4. Delete the item from this file.

Do not close an item by inference.
