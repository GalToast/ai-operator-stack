# Verification Loop

## Principle

AI output is a draft until verified.

The operator loop is:

1. Ask what would make this wrong.
2. Find the highest-risk assumption.
3. Verify through source, code, browser, tests, or direct API.
4. Preserve the evidence.
5. State what was verified versus inferred.
6. Make the final claim smaller if evidence is weaker than expected.

## Common Verification Surfaces

| Surface | Example |
| --- | --- |
| Git diff | Check exactly what changed |
| Tests | Run focused tests when behavior changed |
| Browser snapshot | Prefer DOM/text snapshots for UI state |
| Screenshot | Capture visual proof when layout or rendering matters |
| Console/network logs | Verify runtime errors and API behavior |
| GitHub API | Confirm public repo metadata after publishing |
| Source links | Keep file paths and line references close to claims |

## Adversarial Pass

Before presenting work as finished, ask:

- What would embarrass this answer later?
- What did I not actually verify?
- Did I publish private or noisy material?
- Did I overclaim the result?
- Did I accidentally optimize for volume instead of clarity?
- Does a recruiter know what to click first?

## Claim Discipline

Weak claim:

> AI built this whole thing.

Stronger claim:

> I operate AI agents inside a structured workflow with scoped tasks, persistent context, tool access rules, and verification gates. The resulting systems are inspectable through code, docs, evidence, and public repos.

The second claim is more accurate and more defensible.
