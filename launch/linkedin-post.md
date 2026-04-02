# Launch Post

I kept hitting the same AI problem:

my AI IDE understood the repo I had open, but not the real system around it.

So I made a simple prompt that tells Codex, Claude Code, or Cursor to build a read-only cross-repo context hub:

- `BOOTSTRAP.md`
- `system-index.yaml`
- project cards
- integration cards
- environment map
- secret references only

The point is simple:

**Your AI knows your repo. This helps it understand your system.**

I packaged the prompt here:

`ai-context-hub-prompt`

If you work across multiple repos, internal tools, and external services, this gives your AI a much better map without exposing secrets or changing app code.
