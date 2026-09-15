# 📋 Project Kanban Board

> **Stage 1 of 7 (Real Unknown):** Track setup tasks, ongoing development, and pilot status.
> This file is a live Kanban board. AI agents and human developers must keep this updated as they do their work.

---

## 📖 How to Use This Kanban

1. **Move Tasks**: Move task items between sections (`Backlog 📥`, `Planned 📋`, `In Progress 🔄`, `In Review 👀`, `Done ✅`) as work progresses.
2. **Assignee**: Designate who is working on the task (e.g., `Gemini`, `Claude`, `Copilot`, `Kilo Code`, or `Human`).
3. **Traceability**: Link each task to its relevant stage documentation or source code (e.g., referencing a setup guide in `2_Environment` or a validation check in `7_Testing_Known`).
4. **Update Logs**: When an AI agent performs a task, they must update this kanban board in the same commit to ensure real-time status accuracy.

---

## 📥 Backlog
*Tasks that are defined but not yet scheduled.*

- [ ] **TSK-002: Define YouTube Ingestion Approach**
  - **Assignee:** Environment Agent
  - **Details:** Decide how buffer pulls video metadata/transcripts from our YouTube channel.
  - **Stage Reference:** [2_Environment](../2_Environment/)

- [ ] **TSK-005: Per-Channel Post Templates**
  - **Assignee:** Formula Agent
  - **Details:** Define format rules for LinkedIn, X.com, Reddit, Skool, YouTube, Email posts.
  - **Stage Reference:** [4_Formula](../4_Formula/)

- [ ] **TSK-008: OAuth/API Credential Flow Per Channel**
  - **Assignee:** Environment Agent
  - **Details:** Design how buffer authenticates against each channel's API.
  - **Stage Reference:** [2_Environment](../2_Environment/)

---

## 📋 Planned / To Do
*Tasks scheduled for implementation.*

- [ ] **TSK-003: Pull Video Metadata + Transcript**
  - **Assignee:** Symbols Agent
  - **Details:** Implement ingestion for a single given video as the first working slice.
  - **Stage Reference:** [5_Symbols](../5_Symbols/)

- [ ] **TSK-006: Content-to-Post Generation Pipeline**
  - **Assignee:** Symbols Agent
  - **Details:** Implement the source video → per-channel draft transformation.
  - **Stage Reference:** [5_Symbols](../5_Symbols/)

---

## 🔄 In Progress
*Active tasks currently being worked on.*

*No active tasks in progress.*

---

## 👀 In Review
*Tasks completed and awaiting validation/review.*

*No tasks in review.*

---

## ✅ Done
*Verified and completed tasks.*

- [x] **TSK-001: Bootstrap buffer from delivery-pilot-template**
  - **Assignee:** Claude
  - **Details:** Replaced template placeholders, reset stage content for buffer's actual purpose, synced navigation, ran smoke tests.
  - **Stage Reference:** [README.md](../README.md)

---

## ⚙️ Maintenance

- [ ] Go over git commits periodically, reread changed files, and create/update Kanban tasks to stay on track
- [ ] Update the environment folder > 1_Real_Unknown
- [ ] Update the environment folder > 2_Environment
- [ ] Add new features incoming as visuals folder > 3_Simulation
- [ ] Add new ways of doing the implementation to formula folder > 4_Formula
- [ ] Update the Symbols and pay technical debt > 5_Symbols
- [ ] Add new errors in semblance > 6_Semblance
- [ ] Update the tests folder > 7_Testing_Known
