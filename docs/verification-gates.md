# Verification Gates

Agent work is not complete because the edit looks right. It is complete when the right checks pass, or when skipped checks are named honestly.

## Standard closeout block

Every behavior-bearing change should end with:

```text
Verified:
- <command or source check>: <result>

Remaining risk:
- <none or specific risk>

Next action:
- <done or exact next step>

Loop delta:
- <what this teaches the next run>
```

## Validator selection

Choose the smallest validator that proves the changed path during iteration, then run the full expected gate before release.

| Change type | Minimum checks |
|---|---|
| Markdown/docs | file exists, links or anchors if relevant, public-safety scan if public |
| Frontend code | lint, typecheck, relevant tests, visual smoke if UI changed |
| Backend code | unit tests, integration or smoke test, config validation |
| CLI/tooling | help output, dry-run, fixture test |
| Automation | dry-run, manual one-shot proof, log path, kill switch |
| Config | parser validation, dependent-path smoke test |
| Public repo content | diff review, secret/private term scan, link verification |

## Commit and push gate

Before committing:

1. `git status`
2. `git diff`
3. `git diff --cached`
4. Review untracked files.
5. Check for secrets, credentials, logs, generated noise, and unrelated work.
6. Run validators.

Before pushing:

1. Confirm branch and remote.
2. Confirm push target is intended.
3. Confirm public/private visibility if the repo contains public-facing content.
4. Confirm no private details are being published.

## Skip language

If something cannot be checked, say:

```text
Not verified:
- <check>: <why it could not be run>
Residual risk:
- <what could be wrong because this was skipped>
```

Never replace missing proof with confidence language.

## Safety scans

A simple public-safety scan should look for:

- API key prefixes
- private keys
- private IP ranges
- private hostnames
- customer names
- chat IDs
- raw logs
- local absolute paths
- secret file names

The scan is not a guarantee. It is a backstop before human review.
