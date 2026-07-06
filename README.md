# Droid Harness Upgrades

A public operator kit for people who use Droid, Codex, Claude Code, or other terminal coding agents as long-running engineering workers.

This is meant to be drop-in usable. Hand the repo to an agent and have it install the habits, prompts, hooks, checklists, and review loops that keep coding agents from drifting, overbuilding, losing context, or claiming success without proof.

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

1. **Compound Engineering loop**: plan → work → review → learn.
2. **Grill me**: ruthless design interview before building.
3. **Minimal Implementation Review**: anti-overbuild diff review and delete-list.
4. **Post-ship patrol**: scheduled read-only scan when repo HEAD changes.
5. **Repo hygiene guardian**: clean worktrees, stale branches, backups, generated artifacts, docs drift.
6. **Auto-resume stall watchdog**: recover from transient provider/network stalls without babysitting.
7. **Sanitized session export**: move markdown summaries, not raw secret-bearing transcripts.
8. **Active-context primer**: start sessions with compact continuity.
9. **Knowledge routing**: memory vs durable library vs skills.
10. **Worker closeout discipline**: real verification, not vibes.
11. **Harness architecture**: the control surfaces a serious agent runner should wire together.
12. **Verification gates**: concrete proof before commit, push, PR, deploy, or closeout.
13. **Automation hooks**: safe hook patterns for session start, session end, validators, and patrols.
14. **Session lifecycle**: start, work, handoff, resume, close, archive.

## Start here

- [`docs/drop-in-agent-operating-system.md`](docs/drop-in-agent-operating-system.md)
- [`docs/harness-architecture.md`](docs/harness-architecture.md)
- [`docs/verification-gates.md`](docs/verification-gates.md)
- [`docs/automation-hooks.md`](docs/automation-hooks.md)
- [`docs/memory-and-session-lifecycle.md`](docs/memory-and-session-lifecycle.md)
- [`docs/compound-engineering-loop.md`](docs/compound-engineering-loop.md)
- [`docs/grill-me-design-interview.md`](docs/grill-me-design-interview.md)
- [`docs/minimal-implementation-review.md`](docs/minimal-implementation-review.md)
- [`docs/post-ship-patrol.md`](docs/post-ship-patrol.md)
- [`prompts/install-droid-harness.md`](prompts/install-droid-harness.md)
- [`templates/AGENTS.droid.example.md`](templates/AGENTS.droid.example.md)
- [`examples/harness-config.example.yaml`](examples/harness-config.example.yaml)

## Fast install shape

1. Copy `prompts/install-droid-harness.md` into your agent.
2. Point it at your repo, agent config, and allowed automation surfaces.
3. Require a read-only inventory first.
4. Install one control surface at a time.
5. Run a test session and require proof that each hook or checklist is actually used.
6. Keep secrets, private repo lists, account routing, and customer data out of public docs.

## What a good harness gives you

- a session starts with the right context
- a task gets a plan when it is non-trivial
- fuzzy requirements trigger a design interview
- code changes run validators before closeout
- commits and pushes review diffs for secrets and scope
- long-running workers produce handoff notes
- recurring patrols are read-only unless explicitly approved
- learnings are routed to the right memory layer
- public output is sanitized before publishing

## Public-safety note

Do not publish your real repo lists, private hostnames, account routing, provider auth state, secrets, secret formats, client data, or raw transcripts. Keep this kit generic and configurable.
