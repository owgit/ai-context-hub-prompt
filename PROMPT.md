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
- Never read env file contents wholesale: extract names only, e.g. `cut -d= -f1 .env`
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
   - env var names only, never the values
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
- OPEN_QUESTIONS.md
- REFRESH.md
- PROJECTS/*.md
- INTEGRATIONS/*.md
- RUNBOOKS/*.md

system-index.yaml must include at the top level:
- schema_version
- generated_at: the date the hub was built

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
- sources: the files this entry was built from, so any fact can be re-checked

system-index.yaml must also include a top-level externals list for services and actors I do not own:
- id
- name
- kind
- owned: false

Referential integrity:
- Every id in depends_on and used_by must resolve to a project id or an externals id
- Never reference a node that is not defined

Each PROJECT file must include:
- purpose
- entrypoints
- integrations
- inbound data flows
- outbound data flows
- auth source locations
- constraints: what must never be done in or to this system
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

OPEN_QUESTIONS.md must list every unverified item as a checklist:
- what is unknown
- which system it belongs to
- what would confirm it: a file, a command, or a person
Write this to disk. Do not only report it in chat.

REFRESH.md must explain how to keep the hub true:
- read generated_at first and treat an old hub as claims, not facts
- re-verify a fact against its sources entry before relying on it
- re-run this prompt when systems, repos, or environments change
- move answered items out of OPEN_QUESTIONS.md and into the hub

When the hub is done:
- validate it first: every local_path, key_doc, and env_source must exist on disk, and every depends_on / used_by id must resolve to a defined node
- mark every miss as unverified and report it
- show me the full folder tree
- summarize what was verified
- write everything that remained unverified to OPEN_QUESTIONS.md, then list it for me
- generate optional bridge snippets for AGENTS.md / CLAUDE.md / Cursor memory
- do not apply bridge snippets unless I explicitly approve it
```

