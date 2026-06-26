# Droid Harness Upgrades

A public operator kit for people who use Droid, Codex, Claude Code, or other terminal coding agents as long-running engineering workers.

This repo collects the patterns I use to make coding agents compound instead of drift: compound engineering loops, “grill me” design interviews, minimal-implementation review, repo hygiene patrols, post-ship debt scans, auto-resume for transient provider stalls, sanitized session export, active-context primers, and worker closeout discipline.

It does **not** include private credentials, personal infrastructure, client workflows, raw session transcripts, or account-specific provider routing. It is the public-safe layer another operator can adapt for their own coding harness.

## What I am trying to do

I use coding agents for more than one-off prompts. I want them to run for a long time, clean up after themselves, remember what matters, and become better at my engineering standards.

That means the harness needs triggers and rails around the coding model:

- a planning loop before work starts;
- a “grill me” mode when requirements are fuzzy;
- anti-overbuild review before and after ship;
- repo hygiene sweeps;
- session forwarding into a durable memory loop;
- auto-resume for transient stalls;
- clear closeout proof instead of vague “done.”

Most readers will skim this page or drop the repo into their cloud agent. So the docs are written as copyable patterns: what the trigger does, why it matters, and what to adapt locally.

## Upgrade map

1. **Compound Engineering loop** — plan → work → review → learn.
2. **Grill me** — ruthless design interview before building.
3. **Minimal Implementation Review** — anti-overbuild diff review and delete-list.
4. **Post-ship patrol** — scheduled read-only scan when repo HEAD changes.
5. **Repo hygiene guardian** — clean worktrees, stale branches, backups, generated artifacts, docs drift.
6. **Auto-resume stall watchdog** — recover from transient provider/network stalls without babysitting.
7. **Sanitized session export** — move markdown summaries, not raw secret-bearing transcripts.
8. **Active-context primer** — start sessions with compact continuity.
9. **Knowledge routing** — memory vs durable library vs skills.
10. **Worker closeout discipline** — real verification, not vibes.

## Start here

- [`docs/compound-engineering-loop.md`](docs/compound-engineering-loop.md)
- [`docs/grill-me-design-interview.md`](docs/grill-me-design-interview.md)
- [`docs/minimal-implementation-review.md`](docs/minimal-implementation-review.md)
- [`docs/post-ship-patrol.md`](docs/post-ship-patrol.md)
- [`templates/AGENTS.droid.example.md`](templates/AGENTS.droid.example.md)

## Public-safety note

Do not publish your real repo lists, private hostnames, account routing, provider auth state, secrets, secret formats, client data, or raw transcripts. Keep this kit generic and configurable.
