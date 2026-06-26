# Auto-resume stall watchdog

Long-running coding agents stall. Some stalls are transient and safe to nudge; others require human action.

## Safe auto-resume candidates

- transient provider outage;
- network hiccup;
- rate-limited temporary failure after backoff;
- interrupted stream with no code mutation in progress.

## Do not auto-resume

- auth failures;
- bad request/schema errors;
- terminal command waiting for input;
- destructive operations;
- ambiguous state.

The watchdog should rate-limit nudges and log every resume.
