# Automation Hooks

Hooks should make the agent safer. They should not hide side effects.

## Hook policy

Default to read-only hooks until the manual workflow is proven.

Allowed early hooks:

- session-start context primer
- session-end sanitized handoff
- validator suggestion
- repo hygiene report
- stale branch report
- public-safety scan

Avoid early hooks that:

- delete files
- run `git clean`
- reset branches
- rewrite config
- rotate credentials
- switch model providers
- post externally
- push to remotes

## Session-start hook

Purpose:

- show active repo
- show branch and dirty state
- show relevant local instructions
- show recent handoff if present
- show validator commands if known

Output should be short. A giant context dump becomes noise.

## Session-end hook

Purpose:

- capture what changed
- capture validators run
- capture unresolved risks
- capture next resume command or path
- strip secrets and raw logs

Use `templates/session-handoff.md`.

## Repo patrol hook

Purpose:

- read-only scan after a repo changes
- report dirty state, stale generated files, docs drift, or missing validators
- never auto-fix unless the operator explicitly grants it

## Automation approval card

Before enabling any recurring job, write:

```text
Automation:
- Name:
- Cadence:
- Command:
- Working directory:
- Reads:
- Writes:
- External side effects:
- Log path:
- Kill switch:
- First-run validation:
- Owner:
```

## First-run proof

Every enabled hook or cron needs proof:

- command ran once manually
- output was inspected
- logs are known
- failure behavior is known
- disable path is documented

If a hook cannot be proven manually, it is not ready for recurrence.
