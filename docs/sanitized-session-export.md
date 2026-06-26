# Sanitized session export

Coding sessions should compound, but raw transcripts can contain secrets. Export sanitized markdown instead.

## Pattern

- Read local coding-agent session stores.
- Remove model-private reasoning if present.
- Redact secret-like values.
- Truncate giant tool outputs.
- Write markdown summaries by source/date.
- Forward sanitized artifacts to the central memory/brain pipeline.

Raw JSONL should stay local unless there is an explicit reason to move it.
