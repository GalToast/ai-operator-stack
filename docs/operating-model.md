# Operating Model

## Role Split

The stack works because responsibility is split explicitly:

| Layer | Responsibility |
| --- | --- |
| Human operator | Goal selection, risk judgment, taste, final review, public claims |
| Main agent | Planning, context management, implementation coordination, synthesis |
| Subagents | Bounded research, validation, implementation, audit, or test slices |
| Tools | Browser automation, shell commands, GitHub, file operations, MCP servers |
| Memory/docs | Durable context, operating rules, project state, reusable decisions |

This is not "ask a chatbot for code." It is closer to operating a small technical team where the team members are model-backed workers with tools.

## Working Loop

1. Define the outcome in plain language.
2. Inspect local context before assuming the system shape.
3. Break the work into bounded slices.
4. Use agents or tools for the slices that can run independently.
5. Keep evidence close: logs, screenshots, tests, diffs, source links.
6. Review the result as if the first answer is probably incomplete.
7. Publish only the cleaned, scoped artifact.

## Parallel Work Pattern

Parallelism is useful only when ownership is clear. A typical pattern:

```text
main lane
  - frames the objective
  - assigns bounded tasks
  - keeps the final product coherent

worker lane A
  - inspects implementation surface

worker lane B
  - validates behavior or evidence

worker lane C
  - drafts documentation or summary
```

The main lane does not blindly merge outputs. It reconciles them against the goal.

## Operator Judgment

The human value is not typing every character. The human value is knowing:

- what is worth building
- what would make the result embarrassing in hindsight
- what claims are actually supported
- which outputs are private, noisy, or unsafe to publish
- when an agent has produced plausible nonsense
- what a recruiter, client, or user needs to understand first

That judgment is the work.
