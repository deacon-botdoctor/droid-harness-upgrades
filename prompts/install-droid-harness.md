# Install Droid Harness Prompt

Copy this into your coding agent.

```text
You are installing a disciplined coding-agent harness into this repo or workspace.

First, inspect live state:
- current directory
- git status
- repo files
- existing agent instructions
- package/test/build scripts
- CI config
- hooks or automations
- existing docs and checklists

Do not edit yet.

Then produce a short install plan with:
1. current validators
2. current release path
3. existing instructions or gaps
4. proposed harness files to add or update
5. risks and approval boundaries

After approval or if the user explicitly told you to proceed:
1. add or update local agent instructions
2. add validation closeout rules
3. add commit/push gate rules
4. add session handoff template
5. add public-safety scan for public repos
6. add read-only patrol checklist
7. run validators
8. inspect diff before commit or push

Hard rules:
- do not delete, clean, reset, or overwrite user work without explicit approval
- do not enable recurring automations without an approval card and first-run proof
- do not publish secrets, private hosts, customer data, raw transcripts, or account routing
- do not claim completion without verification output

Final response must include:
- Verified
- Remaining risk
- Next action
- Loop delta
```
