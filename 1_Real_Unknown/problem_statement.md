# 🎯 Problem Statement

> **Stage 1: Real Unknown** — Clearly define the pain point, gap, or opportunity before starting.

---

## 🔍 Core Problem / Pain Point

- **Current State:** We publish long-form video content to our YouTube channel, but that content stops there. Turning a single video into posts for LinkedIn, X.com, Reddit, Skool, and Email is a manual, repetitive, error-prone process (re-watching, re-writing, re-formatting per channel) that rarely happens consistently.
- **Ideal State:** A marketing application (**buffer**) that ingests our YouTube channel's content and automatically produces channel-appropriate draft posts for LinkedIn, X.com, Reddit, Skool, YouTube (community posts/shorts descriptions), and Email — ready for review and scheduling.
- **The Gap:** No system currently connects "video published" to "repurposed, channel-native posts drafted." Outreach is limited by manual authoring time, not by the amount of source content available.

## 👥 Target Audience & Stakeholders

- **Primary User:** The channel owner / marketing operator (us) who wants wider distribution of existing YouTube content without a proportional increase in authoring effort.
- **Secondary Stakeholders:** Audience members on each target channel (LinkedIn, X.com, Reddit, Skool, Email subscribers) who receive more consistent, higher-quality repurposed content; future team members who may manage outreach.

## 💡 Proposed Value Proposition

- Turns one piece of source content (a YouTube video) into many channel-native posts, multiplying reach without multiplying manual effort.
- Keeps brand voice and message consistent across channels by deriving all posts from the same source of truth.
- Creates a repeatable, auditable pipeline (ingest → repurpose → review → schedule/post) instead of ad hoc copy-pasting.

## 🚀 Constraints & Scope Boundaries

- Scope for v1: content **sourced from our YouTube channel only** (no other input sources yet).
- Target channels for v1: LinkedIn, X.com, Reddit, Skool, YouTube, Email.
- Out of scope initially: paid ad management, influencer outreach/DMs, analytics dashboards beyond basic post tracking, and any channel not in the list above.
- Each channel has its own API/ToS/rate-limit constraints (see `risks.md`) that shape what "posting" can mean per channel (e.g., some channels may start as draft-only/manual-post rather than fully automated).
