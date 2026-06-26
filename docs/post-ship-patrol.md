# Post-ship patrol

A post-ship patrol is a scheduled read-only scan across active repos.

## Pattern

1. Keep a repo list.
2. Track last reviewed HEAD per repo.
3. When HEAD changes, review the new commit range.
4. Write a local report and latest summary.
5. Do not mutate code by default.

## What to flag

- Overbuilt abstractions.
- New dependencies without justification.
- Unused workers/scripts.
- Risky surfaces added casually.
- Missing tests/proof.
- Cleanup opportunities.

Exception-only reporting keeps this from becoming alert spam.
