# Skills and Memory

## Skills

Skills are reusable operating procedures for agents. They are more durable than one-off prompts because they encode:

- when to use the workflow
- what inputs matter
- what output format is expected
- what safety or verification rules apply
- what local conventions should be preserved

Examples from the broader workspace include:

| Skill Family | Purpose |
| --- | --- |
| Lead research | Discover, qualify, normalize, and exhaust contact paths |
| Website audits | Run passive-first security, mobile UX, and evidence capture workflows |
| Documents | Produce DOCX, PDF, slides, spreadsheets, and coauthored drafts |
| Browser automation | Use Playwright and screenshots for live UI checks |
| Memory/docs | Keep durable context concise and synchronized |
| Remote edits | Preserve backups and rollback paths for live-server changes |

The skill layer turns "do this again" into an explicit workflow.

## Memory

Memory is not a place for secrets. It is a continuity layer for:

- durable preferences
- repo conventions
- active context
- blockers
- recurring decisions
- environment facts

A useful memory system stays small. It should answer: "What does the next agent need to know so they do not waste time or break something?"

## Why This Matters for AI Work

Without skills and memory, AI work becomes fragile:

- every task starts from zero
- the same mistakes repeat
- local conventions drift
- private context gets pasted into prompts
- no one can tell which rules are durable

With skills and memory, the operator can build momentum across days and projects without relying on model recall.

## Public-Safe Principle

The public portfolio should show the pattern, not the private data. Publish:

- workflow diagrams
- sanitized examples
- architecture notes
- guardrails
- verification habits

Do not publish:

- secrets
- client data
- lead records
- inbox exports
- raw CRM databases
- private memory files
