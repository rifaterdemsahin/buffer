# 🧪 Hypotheses

> **Stage 1: Real Unknown** — Document your initial assumptions and how they will be validated in Stage 7.

---

## 🔍 Core Hypotheses

### Hypothesis 1: A single YouTube video contains enough material to derive posts for all 6 target channels
- **Rationale:** Long-form video (transcript + description + title + thumbnail) typically covers several ideas, quotes, and takeaways — enough raw material to be reshaped per channel without needing additional source input.
- **Validation Method:** Run the pipeline against a real published video and confirm a usable draft is produced for each of LinkedIn, X.com, Reddit, Skool, YouTube, and Email.
- **Linked Test:** [7_Testing_Known/validation_report.md](../7_Testing_Known/validation_report.md)
- **Status:** ⏳ Pending Validation

---

### Hypothesis 2: Per-channel formatting rules can be encoded as reusable templates rather than one-off manual edits
- **Rationale:** Each channel has stable structural constraints (length, tone, hashtag/format conventions) that don't change per video, so a template + fill-in approach should generalize.
- **Validation Method:** Generate posts for 2+ different source videos and confirm the same channel template produces correctly-formatted output each time.
- **Linked Test:** [7_Testing_Known/validation_report.md](../7_Testing_Known/validation_report.md)
- **Status:** ⏳ Pending Validation

---

### Hypothesis 3: Human-in-the-loop review before posting is acceptable overhead for v1
- **Rationale:** Fully automated posting risks brand-voice drift and per-channel ToS violations; a review step trades some automation for safety while the system is new.
- **Validation Method:** Confirm the workflow includes an explicit draft/review state before any scheduling or posting action, and that no channel API call posts without that gate.
- **Linked Test:** [7_Testing_Known/validation_report.md](../7_Testing_Known/validation_report.md)
- **Status:** ⏳ Pending Validation
