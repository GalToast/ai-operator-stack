# AI Operator Stack

Public case study of a terminal-first, human-in-the-loop AI operating system.

This repo explains how I use AI agents, local memory, MCP tools, browser automation, reusable skills, and verification loops to build real software and operational workflows. It is not presented as traditional solo hand-coding. It is presented as an AI-native operating practice: I act as architect, operator, reviewer, and quality controller while agents perform bounded implementation, research, testing, and documentation work.

## Why This Exists

Many people use AI as a chat window. My work is built around a deeper pattern:

- agents with explicit roles and boundaries
- terminal-first workflows that preserve state and evidence
- reusable skills for repeatable operations
- browser automation for real-world interaction and inspection
- local memory and repo notes for continuity
- verification loops that make weak assumptions visible
- resource controls so parallel agents do not collide over shared tools

The goal is not to hide that AI is involved. The goal is to show the operating system around it.

## Proof Artifacts

| Artifact | What it shows |
| --- | --- |
| `docs/operating-model.md` | How the human/operator role, agents, tools, and review loops fit together |
| `docs/skills-and-memory.md` | Reusable skills, durable memory, and continuity model |
| `docs/browser-resource-governance.md` | Shared browser/session controls for parallel agent work |
| `docs/verification-loop.md` | How claims are checked before work is treated as complete |
| `examples/session-slice.md` | Compact example of the operating style |

## The Throughline

I build AI-assisted systems that turn noisy real-world signals into bounded operational decisions.

That shows up in several public projects:

- `trading-bots`: state-aware research, telemetry, risk controls, and proof surfaces
- `website-audit-engine`: evidence-tiered website audit automation
- `leadops`: retrieval, mailbox parsing, lead normalization, and operator review queues
- `semantic-demo`: interactive semantic vector visualization
- `opencode-fork`: custom skills, launcher workflow, and agent orchestration notes

This repo is the meta-layer: how those projects get built and operated.

## Reading Path

1. [Operating Model](docs/operating-model.md)
2. [Skills and Memory](docs/skills-and-memory.md)
3. [Browser Resource Governance](docs/browser-resource-governance.md)
4. [Verification Loop](docs/verification-loop.md)
5. [Public Portfolio Map](docs/public-portfolio-map.md)

## What This Demonstrates

For AI and AI-adjacent roles, this repo is meant to show:

- AI workflow design
- prompt-to-production judgment
- agent coordination
- tool and context management
- browser automation literacy
- evidence discipline
- documentation hygiene
- product sense around operational systems

## What This Is Not

- Not a claim that I hand-wrote every line of every project.
- Not a claim that agents remove the need for engineering judgment.
- Not a dump of private workspace data.
- Not a replacement for reading the project repos themselves.

The claim is narrower and stronger: I can operate AI systems deeply enough to produce useful software, audits, workflows, research surfaces, and public-facing artifacts while keeping verification and human judgment in the loop.

## Vocabulary

The precise framing for this work:

- **AI-native systems operator**: someone who works through AI-enabled tools as the normal interface to software and operations.
- **Human-in-the-loop AI systems builder**: someone who designs the workflow, constraints, review gates, and outputs around AI work.
- **AI automation engineer**: someone who builds and operates automations where LLMs, scripts, browsers, data, and humans each have defined roles.

## Related Repos

- [trading-bots](https://github.com/GalToast/trading-bots)
- [website-audit-engine](https://github.com/GalToast/website-audit-engine)
- [leadops](https://github.com/GalToast/leadops)
- [semantic-demo](https://github.com/GalToast/semantic-demo)
- [opencode-fork](https://github.com/GalToast/opencode-fork)
