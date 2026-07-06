# Memory and Session Lifecycle

Long-running coding agents need continuity, but not every detail deserves durable memory.

## Lifecycle

1. **Start**: load compact context and repo instructions.
2. **Plan**: define scope, validators, and risks.
3. **Work**: edit in small steps and keep todos current.
4. **Verify**: run relevant checks.
5. **Review**: inspect diff, secrets risk, and unrelated changes.
6. **Closeout**: summarize proof, risk, and next action.
7. **Handoff**: write a sanitized session note if work may continue later.
8. **Learn**: promote reusable lessons to docs, skills, or memory.

## What to remember

Use compact memory for:

- stable preferences
- recurring mistakes to avoid
- durable decisions
- handoff pointers
- reusable lessons

Do not store:

- raw transcripts
- secrets
- full logs
- temporary task noise
- stale command output
- customer-private material in shared memory

## Handoff standard

A handoff should let the next agent resume without rereading the whole transcript.

It should include:

- task
- repo and path
- branch
- files changed
- validators run
- current blockers
- next exact command
- residual risk

Use `templates/session-handoff.md`.

## Lesson promotion

Only promote a lesson if it is:

- reusable
- verified by outcome
- not secret-bearing
- not customer-specific unless stored in the right customer scope
- short enough to help future sessions

## Stale memory warning

Memory is a lead, not proof. For current process, git, file, repo, spend, public visibility, or runtime state, inspect the live source before answering or acting.
