# 💰 Cost Tracker & Model/Tool Comparisons

> **Stage 1: Real Unknown** — Managed by the **Environment Agent**. Tracks infrastructure costs, LLM token costs, and compares models/tools to suggest the most cost-effective options.

## Purpose

The Environment Agent checks costs for all environments (including LLM costs), understands what needs to be done, compares different models and tools, gives cost-saving suggestions, and records all findings here.

---

## 🏗 Infrastructure Costs

| Service | Provider | Tier | Est. Monthly | Actual Monthly | Status |
|---------|----------|------|-------------|----------------|--------|
| Azure Key Vault | Microsoft | Standard | $0.03/10k ops | $0.00 | ✅ Active |
| GitHub Pages | GitHub | Free | $0.00 | $0.00 | ✅ Active |
| Azure Project Storage | Microsoft | Pay-per-use | TBD | $0.00 | 📋 Planned |
| Fly.io / Cloudflare Workers | Fly.io / Cloudflare | Free tier | $0.00 | $0.00 | 📋 Planned |

**Total estimated monthly:** $0.00 (nothing deployed yet — fresh bootstrap)

---

## 🤖 LLM Model Cost Comparison

*To be filled in as buffer's content-generation pipeline is built and specific models are chosen for repurposing tasks.*

| Model | Provider | Input / 1M tokens | Output / 1M tokens | Context Window | Best For | Cost Rating |
|-------|----------|-------------------|-------------------|----------------|----------|-------------|
| — | — | — | — | — | — | — |

---

## 🛠 Tool Cost Comparison — Free vs Paid Tiers

*To be filled in as per-channel API tools and infrastructure are selected.*

| Tool | Free Tier Limit | Paid Starts At | Scale Trigger | Suggestion |
|------|----------------|---------------|---------------|------------|
| — | — | — | — | — |

---

## 📊 LLM Token Consumption Log

| Date | Agent | Model | Tokens In | Tokens Out | Est. Cost | Task |
|------|-------|-------|-----------|------------|-----------|------|
| — | — | — | — | — | — | — |

---

## 🚨 Token Usage Monitoring & Spike Alerts

The Environment Agent monitors LLM token consumption and warns on cost spikes.

### Alert Thresholds
- **Daily spike warning**: >$2/day above running 7-day average
- **Session spike warning**: >$0.50 in a single agent session above normal
- **Monthly overrun warning**: >80% of projected monthly budget used before day 20

### Spike Alert Log
| Date | Alert | Trigger | Action Taken | Status |
|------|-------|---------|--------------|--------|
| — | — | — | — | — |

---

## 📈 Summary

| Metric | Value |
|--------|-------|
| Current monthly cost | **$0.00** |
| Projected cost at scale | TBD |
| Largest saving this session | N/A |
| Most expensive active component | None yet |
| Next likely paid switch | TBD |
