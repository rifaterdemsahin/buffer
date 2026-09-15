# Project Risks

> **Stage 1: Real Unknown** — Track active risks, solved risks, and the risk update log. Add new risks with every project update and mention those that are solved.

## Risk Matrix

| Severity | Symbol | Meaning |
|----------|--------|---------|
| Critical | 🔴 | Blocks delivery — must resolve immediately |
| High | 🟠 | Significantly impacts quality or timeline |
| Medium | 🟡 | Should be addressed in current milestone |
| Low | 🟢 | Monitor — address when convenient |

---

## ⚠️ Active Risks

### R-001: Per-Channel API Rate Limits and Terms of Service
- **Status:** 🟠 Active
- **Severity:** High
- **Likelihood:** High (each of LinkedIn, X.com, Reddit, Skool, YouTube, Email has its own limits and ToS)
- **Impact:** Automated posting could be throttled, rejected, or result in account suspension if a channel's rate limits or content policies are violated.
- **Trigger:** Bulk/automated posting without respecting per-channel API quotas or content rules
- **Mitigation:** Document each channel's rate limits and posting policy in `2_Environment`; start with draft-only/manual-post for higher-risk channels (Reddit, Skool) before enabling automated posting.
- **Last Updated:** 2026-09-15

### R-002: OAuth Complexity Across Six Channels
- **Status:** 🟠 Active
- **Severity:** High
- **Likelihood:** High (six separate OAuth/API integrations)
- **Impact:** Each channel requires its own auth flow, token refresh, and scopes — integration and maintenance effort scales with channel count.
- **Trigger:** Adding or maintaining a channel integration
- **Mitigation:** Build one shared credential-storage pattern (Azure Key Vault) and a common adapter interface; onboard channels incrementally rather than all at once.
- **Last Updated:** 2026-09-15

### R-003: Content Quality / Brand Voice Drift
- **Status:** 🟡 Active
- **Severity:** Medium
- **Likelihood:** Medium (LLM-generated repurposing can drift from intended tone)
- **Impact:** Posts that don't match brand voice could damage credibility across channels.
- **Trigger:** Automated post generation without a review step, or prompt drift over time
- **Mitigation:** Require human review/edit before scheduling (see `hypotheses.md` H3); keep a style guide in `4_Formula` that the generation pipeline references.
- **Last Updated:** 2026-09-15

### R-004: Reddit / Skool Community-Guideline Risk
- **Status:** 🟠 Active
- **Severity:** High
- **Likelihood:** Medium
- **Impact:** Reddit and Skool communities are sensitive to self-promotion; violating community rules can get the account banned or the domain blacklisted.
- **Trigger:** Cross-posting the same promotional content without adapting to community norms
- **Mitigation:** Treat Reddit/Skool as manual-review-required channels initially; tailor content per-community rather than blindly cross-posting.
- **Last Updated:** 2026-09-15

### R-005: Credential Security Across Channel Integrations
- **Status:** 🟡 Active
- **Severity:** Medium
- **Likelihood:** Low (mitigated by design, but high impact if it occurs)
- **Impact:** Leaked OAuth tokens/API keys for any channel could allow unauthorized posting or account takeover.
- **Trigger:** Credentials committed to git, logged, or stored outside Key Vault
- **Mitigation:** All channel credentials load from Azure Key Vault at runtime (RULE-003/RULE-004); `.env.example` stays placeholder-only; secrets scan runs in smoke tests.
- **Last Updated:** 2026-09-15

### R-006: Single LLM Model Dependency for Agent Generation
- **Status:** 🟡 Active
- **Severity:** Medium
- **Likelihood:** Medium (LLMs are switched frequently)
- **Impact:** If `agents.md` coordinator rules aren't consistently applied when generating persona files for a new LLM, the new agent may miss critical rules.
- **Trigger:** Switching to a new LLM without thorough persona file generation
- **Mitigation:** Follow the documented persona file generation process in `agents.md`. Always include the full 7-stage execution flow in every persona file.
- **Last Updated:** 2026-09-15

---

## ✅ Solved Risks

*No risks solved yet — this is a fresh project bootstrap.*

---

## 📋 Risk Update Log

| Date | Update | Risk ID | Change |
|------|--------|---------|--------|
| 2026-09-15 | Bootstrap from delivery-pilot-template; initial risk assessment for buffer | R-001 → R-006 | 6 active risks identified for the marketing/repurposing project |

---

## Risk Review Cadence

- **Every project update** — Add new risks, update existing ones, move solved risks to the Solved section
- **Every milestone completion** — Review all active risks, re-evaluate severity/likelihood
- **Smoke test failures** — If a smoke test catches a new class of error, create a risk entry
- **Channel integration changes** — When adding or changing a channel adapter, evaluate and log new risks
- **LLM switch** — When switching the LLM model, review R-006 and update mitigation if needed
