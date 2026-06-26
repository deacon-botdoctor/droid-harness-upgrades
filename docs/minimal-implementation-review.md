# Minimal Implementation Review

Minimal Implementation Review is the anti-overbuild lane. It asks: did the agent build the smallest thing that proves the outcome?

## Review dimensions

- Reused existing code?
- Used standard library/native platform before new dependency?
- Avoided speculative abstractions?
- Avoided unnecessary workers, migrations, auth, billing, permissions, schemas, Docker, CI, or cron changes?
- Produced a delete-list?
- Ran the right tests or smoke checks?

## Report shape

- **Verdict:** pass / revise / block.
- **Smallest path:** what should have been enough.
- **Delete-list:** code/files/deps that should be removed or inlined.
- **Risk flags:** sharp surfaces touched.
- **Verification:** what passed and what remains.
