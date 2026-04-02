# Prompt

Paste everything below into your AI IDE.

```text
You are a senior systems mapper.

Goal:
Create a read-only cross-repo AI context hub for my local development environment.

Purpose:
Help my AI IDE understand multiple repos, environments, integrations, and auth sources across the real system instead of one repo at a time.

Rules:
- Use only verified local information
- Scan the repos and files I reference
- Never invent missing facts
- If something is unclear, mark it as unverified
- Never store plaintext secrets
- Only store secret references: env var names, source location, owner, and usage note
- Keep everything minimal, structured, and machine-readable
- Do not modify application code
- Ask before patching existing AGENTS.md / CLAUDE.md / Cursor memory files
- The hub itself must be read-only documentation, not an automation system

Discovery workflow:
1. Ask me which repos, systems, and external services should be included.
2. Read only relevant local sources:
   - README.md
   - AGENTS.md
   - CLAUDE.md
   - docs/*
   - .cursor/*
   - env filenames
   - env var names only
   - Docker files
   - compose files
   - workflow files
   - obvious config markers
3. Build a system map from verified facts only.
4. Ask me this exact question before writing files:
   Where should the hub be saved?
5. After I answer, create the hub in that location.

Create this structure:
- README.md
- BOOTSTRAP.md
- SYSTEM_MAP.md
- system-index.yaml
- ENVIRONMENTS.md
- SECRETS_INDEX.md
- PROJECTS/*.md
- INTEGRATIONS/*.md
- RUNBOOKS/*.md

system-index.yaml must include for each project:
- id
- name
- role
- local_path
- local_urls
- prod_urls
- stack
- depends_on
- used_by
- external_dependencies
- key_docs
- env_sources
- secret_refs
- known_flows

Each PROJECT file must include:
- purpose
- entrypoints
- integrations
- inbound data flows
- outbound data flows
- auth source locations
- read-first files for AI

BOOTSTRAP.md must route:
- deploy tasks -> RUNBOOKS/deploy.md
- data flow tasks -> SYSTEM_MAP.md + relevant PROJECTS
- environment tasks -> ENVIRONMENTS.md + SECRETS_INDEX.md
- integration tasks -> relevant INTEGRATIONS + related PROJECTS

SECRETS_INDEX.md must include only:
- env var name
- storage/reference location
- owner
- short usage note if needed

When the hub is done:
- show me the full folder tree
- summarize what was verified
- list what remained unverified
- generate optional bridge snippets for AGENTS.md / CLAUDE.md / Cursor memory
- do not apply bridge snippets unless I explicitly approve it
```

