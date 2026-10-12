# Tokenomy Analysis: Developer AI Usage vs. Engineering Output (2024–2026)

Interactive Executive Briefing and empirical research analyzing how internal AI adoption across Google, Microsoft, Amazon, Stripe, and Meta, plus an expansion set (FactSet, Zeta Global, Compass, N-able, Cognizant, Accenture, MercadoLibre, Shopify), translated into software delivery output, pull request throughput, and system modernization.

## 🚀 Live Briefing
👉 **[View the Live Executive Briefing](https://sujalpradhan.github.io/Tokenomy-Analysis/)**

---

### Core Findings
1. **Code share is rising; delivery evidence is not:** Google's AI-generated share of new code rose from >25% (Oct 2024) to 75% (Apr 2026), and Zeta Global reports 89.6% (Q2 2026). Almost no company ties these figures to end-to-end delivery metrics; our reading is that the bottleneck has shifted to **code review, architectural validation, and automated testing**.
2. **The Modernization Dividend:** Amazon estimates Amazon Q Developer saved **4,500 developer-years** on Java 17 upgrades (~50 developer-days → a few hours per app); developers shipped 79% of the auto-generated code reviews without additional changes (Andy Jassy, Aug 2024).
3. **Autonomous Agent Shipping:** Over **1,000 merged pull requests per week** at Stripe are completely produced by its one-shot **Minions** coding agents, most often started from Slack; at Shopify, 1 in 8 merged PRs is co-authored by its River agent.
4. **Pull Request Velocity:** An observational study of 16,223 Microsoft engineers (Feb–Dec 2025; arXiv preprint) estimated **+40.5% more PRs** in highest- vs zero-Copilot-usage weeks.

---

### Repository Structure
- `index.html`: Standalone, interactive Executive Briefing (root entry point for GitHub Pages).
- `token-cost-faang/presentation/all_in_one.html`: Interactive briefing mirror.
- `token-cost-faang/data/`: Empirical facts, telemetry figures, and verified primary sources (`facts.csv`, `sources.csv`, `pyramid.csv`).
- `token-cost-faang/findings.md`: Detailed empirical findings matrix and full primary citations.

---

### Verified Sources
Every verified data point traces to a primary source: company earnings transcripts and filings, official company or engineering blogs, CEO posts, or the study itself (arXiv preprints are labelled as such). Targets and media-only claims are marked separately. All sources were re-audited on 2026-10-12; see the audit log in `token-cost-faang/findings.md`.
