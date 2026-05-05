# Agent Safety Model

This repo describes an AI-assisted operating model, not an unattended production agent. The default posture is human-in-the-loop: agents can inspect, draft, test, and propose changes, but sensitive access and final claims stay under human review.

## Boundaries

- Agents are assigned scoped tasks with explicit ownership and forbidden areas.
- Secrets, credentials, tokens, private memory, inbox data, client data, and production configuration are not public artifacts and should not be pasted into prompts.
- Browser sessions, remote edits, deploys, and outreach paths require explicit task intent and verification.
- Edit-capable agents are expected to preserve unrelated user or peer work and report blockers instead of editing around them.
- Public repos contain sanitized examples and documentation, not raw private sessions or private datasets.

## Approval Gates

Agent output is not treated as complete until it has passed the relevant human and mechanical checks:

1. Scope check: did the agent stay inside the assigned files, task, and data boundary?
2. Evidence check: did it preserve the proof needed to verify the claim?
3. Safety check: did it avoid secrets, private data, unauthorized targets, and live side effects?
4. Verification check: did tests, screenshots, CLI checks, or manual review support the result?
5. Review check: would a skeptical reviewer understand what changed and what is still uncertain?

## Threat Model

The main risks are not treated as theoretical:

- over-broad file access
- credential exposure through prompts or logs
- accidental live-site or browser-session side effects
- agent-generated code that looks plausible but is wrong
- private data leaking into public docs
- multiple agents colliding over the same resource

The controls are scoped prompts, repo-local rules, no-secret memory policy, browser resource governance, switchboard coordination, test-first verification, and human review before public claims.

## Public Claim

The claim is not that agents are trusted to act independently. The claim is that AI-assisted work can be made reviewable when agents have boundaries, evidence requirements, and human-controlled approval gates.
