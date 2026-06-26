# Compound Engineering loop

Compound Engineering is the harness pattern for making coding agents improve over time.

```text
Plan → slice → implement → verify → review → learn → update the harness
```

## Plan

Write the target outcome, constraints, non-goals, acceptance proof, and rollback path.

## Slice

Break work into independently verifiable issues or steps. Each slice should be shippable or safely discardable.

## Implement

Use the smallest path that satisfies the acceptance proof. Prefer existing code, standard library, native platform features, and installed dependencies before adding new abstractions.

## Verify

Run the real tests, lint, smoke checks, or live probes. If a tool fails, report that honestly.

## Review

Run minimal-implementation review and delete-list review.

## Learn

If the same mistake will recur, turn the lesson into a skill, checklist, or repo guard.
