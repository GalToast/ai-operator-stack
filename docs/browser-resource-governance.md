# Browser Resource Governance

## Problem

AI agents often need browsers for real work: testing UIs, checking live pages, filling forms, capturing screenshots, reading console errors, and inspecting network activity.

When multiple agents share the same browser resources, naive automation gets brittle:

- tabs multiply
- state leaks between tasks
- one worker closes another worker's page
- Chrome DevTools access collides
- screenshots and console reads come from the wrong context
- a "successful" check verifies the wrong thing

## Pattern

The workspace uses a browser-resource governance model:

| Control | Reason |
| --- | --- |
| Small tab limits | Prevent hidden browser sprawl |
| Auto-close after checks | Keep sessions clean |
| Retained tabs | Preserve intentional long-running context |
| Chrome DevTools mutex | Ensure only one worker owns DevTools at a time |
| Explicit collision-risk override | Make unsafe bypasses deliberate |
| Status reporting | Show tab counts, mutex holder, queue length, and sessions |

## Simplified TypeScript Sketch

```ts
type TabInfo = {
  id: number
  createdAt: number
  retained: boolean
  purpose: string
}

type BrowserResourceConfig = {
  maxTabs: number
  autoCloseAfterCheck: boolean
  chromeDevToolsMutexEnabled: boolean
  mutexTimeoutMs: number
  allowCollisionRisk: boolean
}
```

The important idea is not the exact implementation. The important idea is that shared browser tools need policy.

## Gatekeeper Model

For parallel work, Chrome DevTools should be treated as a single-lane resource:

```text
worker requests DevTools access
  -> if free, access is granted
  -> if busy, worker waits or uses Playwright/direct HTTP checks
  -> after operation, worker releases access
```

This lets workers continue in parallel without pretending that every browser tool is safely parallel.

## Recruiter Signal

This pattern shows the kind of AI-adjacent engineering that matters in production:

- tool access control
- reliability under concurrency
- state isolation
- explicit unsafe-mode handling
- operational observability

Agent systems are only useful when their tools are governed.
