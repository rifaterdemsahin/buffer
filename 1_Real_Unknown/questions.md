# ❓ Open Questions

> **Stage 1: Real Unknown** — Document the specific questions and unknowns that this project must answer.

---

## 📋 Active Unknowns

*List the questions that need answers before or during the development process. As they are resolved, link to the formula, design, or code that answers them.*

| Question | Owner / Agent | Target Stage for Resolution | Resolution Notes / Link |
| :--- | :--- | :--- | :--- |
| **Q1:** How do we ingest content from the YouTube channel (API polling, webhook, manual trigger)? | Environment Agent | `2_Environment` | |
| **Q2:** Which channels get full OAuth-based auto-posting in v1 vs. draft-only/manual copy-paste? | Human / Real Agent | `1_Real_Unknown` | |
| **Q3:** What storage holds source transcripts, generated drafts, and post history? | Environment Agent | `2_Environment` | Default is Azure project-based storage per RULE-004 |
| **Q4:** How do we keep brand voice consistent across an LLM-generated post pipeline? | Human / Formula Agent | `4_Formula` | |
| **Q5:** What are Reddit's and Skool's community-specific posting rules we must respect (no spam, self-promotion limits)? | Human | `1_Real_Unknown` | |
| **Q6:** What scheduling mechanism triggers actual posting (cron, queue, manual approve-and-send button)? | Formula Agent | `4_Formula` | |
| **Q7:** [Add your question here...] | | | |

---

## 📌 Instructions
1. Document questions **before** writing code.
2. Update the "Resolution Notes" column as soon as a decision is made or implemented.
3. Move fully resolved questions to `1_Real_Unknown/_obsolete/questions.md` if the log gets too cluttered.
