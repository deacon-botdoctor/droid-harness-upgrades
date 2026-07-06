# Drop-in Agent Operating System

This page is the install target. Give it to a coding agent and tell it to adapt the harness to the current repo.

## Mission

Turn a terminal coding agent from a one-off code generator into a disciplined engineering worker.

The harness should make the agent:

- gather live context before acting
- plan before non-trivial work
- ask a focused question when requirements are unclear
- edit in small reversible steps
- run validators before claiming success
- review diffs before commit or push
- capture handoffs for long-running work
- route durable lessons to the right memory layer
- avoid leaking private context into public artifacts

## Install order

1. **Inventory**: inspect repo layout, scripts, tests, docs, hooks, CI, and local instructions.
2. **Session start**: add a compact active-context primer or equivalent.
3. **Planning gate**: add the compound engineering loop for non-trivial work.
4. **Clarification gate**: add grill-me mode for fuzzy plans or high-blast-radius design.
5. **Implementation gate**: add minimal implementation review.
6. **Validation gate**: require test, lint, typecheck, or scoped validator proof before closeout.
7. **Release gate**: require diff review, secret scan, status check, and remote-impact check before commit or push.
8. **Closeout gate**: require verified, remaining risk, next action, and loop delta.
9. **Session end**: write a sanitized handoff, not raw transcripts.
10. **Patrols**: add read-only scheduled checks only after manual commands prove useful.

## The minimum viable harness

If you only install five things, install these:

1. `AGENTS.md` or equivalent local agent instructions.
2. A validator closeout checklist.
3. A release checklist.
4. A sanitized handoff template.
5. A read-only repo hygiene patrol.

## Agent instruction

```text
Before editing anything, inspect the repo and identify its validators.
For non-trivial work, maintain a todo list.
Before claiming completion, run the relevant validators and summarize proof.
Before any commit or push, inspect git status, staged diff, and secrets risk.
If validation cannot run, say exactly what could not be checked.
Do not delete, clean, reset, or overwrite untracked work without explicit approval.
```

## Success criteria

The harness is working when a new agent can:

- explain the repo's validation path
- make a small change and prove it
- stop before destructive git commands
- produce a useful handoff
- identify where a durable lesson should be stored
- separate public-safe notes from private operational detail
