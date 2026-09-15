# Tasks & Phases

> **Stage 1: Real Unknown** — Project phases and task breakdown managed by the **Real Agent**. Each task is assigned to a specific agent. Complex tasks are coordinated by the Real Agent across multiple agents.

## Phase 0: Bootstrap (Completed)

| ID | Task | Agent | Done |
|----|------|-------|------|
| TSK-001 | Bootstrap `buffer` from `delivery-pilot-template` (placeholders, stage content reset, nav sync, smoke test) | Claude | [x] |

## Phase 1: Content Ingestion (Planned)

| ID | Task | Agent | Done |
|----|------|-------|------|
| TSK-002 | Define YouTube channel ingestion approach (API polling vs. webhook vs. manual trigger) | Environment Agent | [ ] |
| TSK-003 | Pull video metadata + transcript for a given video | Symbols Agent | [ ] |
| TSK-004 | Store ingested source content (Azure project-based storage, per RULE-004) | Environment Agent | [ ] |

## Phase 2: Per-Channel Post Formatting (Planned)

| ID | Task | Agent | Done |
|----|------|-------|------|
| TSK-005 | Define post template/format rules per channel (LinkedIn, X.com, Reddit, Skool, YouTube, Email) | Formula Agent | [ ] |
| TSK-006 | Implement content-to-post generation pipeline (source video → per-channel draft) | Symbols Agent | [ ] |
| TSK-007 | Build draft review/edit UI or flow before scheduling | Symbols Agent | [ ] |

## Phase 3: Auth & Channel Integration (Planned)

| ID | Task | Agent | Coordination | Done |
|----|------|-------|-------------|------|
| TSK-008 | Design OAuth/API credential flow per channel | Environment Agent | Real Agent coordinates: Environment documents each channel's auth model → Formula specs the credential storage → Symbols implements | [ ] |
| TSK-009 | Store channel credentials securely (Azure Key Vault) | Environment Agent | [ ] |
| TSK-010 | Implement per-channel posting/publishing adapter | Symbols Agent | [ ] |

## Phase 4: Scheduling & Posting Mechanism (Planned)

| ID | Task | Agent | Done |
|----|------|-------|------|
| TSK-011 | Define scheduling mechanism (queue, cron, manual approve-and-send) | Formula Agent | [ ] |
| TSK-012 | Implement scheduler and post-history tracking | Symbols Agent | [ ] |

## Phase 5: Testing & Deployment (Planned)

| ID | Task | Agent | Coordination | Done |
|----|------|-------|-------------|------|
| TSK-013 | Run full smoke test suite on all pages | Test Agent | Real Agent coordinates: opens all pages → Test Agent scans for errors → Semblance logs findings → reports back to Real Agent | [ ] |
| TSK-014 | Deploy to GitHub Pages / backend (Fly.io or Cloudflare Workers per RULE-003) and verify | Symbols Agent | [ ] |
| TSK-015 | Publish retrospective in `6_Semblance/lessons_learned.md` | Semblance Agent | [ ] |

## Task Management Rules

1. **Real Agent owns this file** — breaks the project into phases and tasks, assigns agents, coordinates complex tasks
2. **Every task names its agent** — the Agent column identifies which stage agent is responsible for execution
3. **Complex tasks describe coordination** — tasks involving 2+ agents include a Coordination column explaining how the Real Agent orchestrates the workflow
4. **Status tracking**: `[ ]` Pending, `[x]` Completed, `[~]` In Progress, `[!]` Blocked
5. **Link to specs** — tasks that implement a spec should reference the SPEC-XXX number
6. **Task granularity** — a task should be completable in a single coding session
7. **Real Agent as coordinator** — for complex tasks, the Real Agent defines the scope, dispatches to agents, and validates the result against OKRs
