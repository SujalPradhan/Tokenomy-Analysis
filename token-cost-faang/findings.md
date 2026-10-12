# Internal Developer AI Usage vs. Engineering Output: Findings & Empirical Analysis

> **Validation status (re-audited 2026-10-12):** every figure below was re-checked against its source. ✅ = verified in a primary source (company filing/transcript/blog/CEO post or the study itself). ⚠️ = management target, or known only through media reports. Figures that could not be traced to any source were **removed**, not relabelled. See the audit log at the end of this file.

## 1. Executive Summary

**The Core Question:** When internal software engineers and employees consume AI tokens, how does that translate into measurable output and workforce productivity?

**The Core Finding:** Disclosed AI share of code is rising fast, but almost no company links it to end-to-end delivery output. What is verifiable:
*   **Google:** AI-generated share of new code rose from **>25% (Oct 2024)** to **50% (fall 2025)** to **75% (Apr 2026)**, all stated by CEO Sundar Pichai on blog.google ✅. No org-wide velocity metric. One anecdote: a complex migration completed 6x faster than a year earlier.
*   **Microsoft:** Observational study (arXiv preprint by Microsoft authors) of **16,223 Cloud+AI engineers, Feb–Dec 2025**: **+40.5% PRs** in highest- vs zero-Copilot-usage weeks, holding measured effort constant ✅. CEO Satya Nadella said "maybe 20 to 30 percent" of repo code is AI-written (Apr 2025, media-reported ⚠️). The often-cited **55.8% faster** result is a 2022 GitHub RCT of **95 recruited developers** (not Microsoft staff) on one task ✅.
*   **Amazon:** Java 17 upgrades fell from **~50 developer-days to a few hours**; Amazon estimates **4,500 developer-years** saved, **>50% of production Java systems** upgraded in under six months, **79% of auto-generated code reviews** shipped without changes, and **$260M** in annualized efficiency gains (Andy Jassy, Aug 2024) ✅.
*   **Stripe:** Over **1,000 merged pull requests per week** are completely Minion-produced (Stripe engineering blog, Feb 2026) ✅. InfoQ's ~1,300 figure is secondary and not used.
*   **Meta:** **Targets only** ⚠️. Zuckerberg projected ~half of development by AI "in the next year" (Apr 2025); a leaked document shows the creation org targeting 65% of engineers writing >75% of committed code with AI in H1 2026.
*   **Klarna (customer service, not engineering):** AI assistant did the work of **700 full-time agents** and cut resolution time from 11 to under 2 minutes in its first month (Feb 2024) ✅. 853 FTEs and $60M saved (Q3 2025) is media-reported ⚠️.

**Expansion set (2025–2026):** A second tier of companies now disclose AI code share on earnings calls:
*   **Zeta Global:** **89.6%** of new code automated in Q2 2026 (75% in Q1) via internal tool Spade.
*   **Compass:** **50%–60%** of new code produced by AI (Q2 2026), up from 30%–40% in Q1, when management cited **+20% product development velocity** with flat tech OpEx.
*   **N-able:** **47%** of all committed code AI-generated (Q2 2026).
*   **Cognizant:** **~30%** of internal code AI-generated (Q3 2025) → **>40%** of software development AI-*assisted* (Q2 2026); 50% stated as a target.
*   **FactSet:** Coding agents author **27%** of committed code *in the teams using them*; ~10% technology workforce reduction.
*   **Shopify:** **1 in 8** merged PRs co-authored by the internal River agent (3,536 merged in 30 days).
*   **Accenture:** Randomized Copilot trial: **+8.69% PRs**, +15% merge rate, +84% successful builds (vendor-published).
*   **MercadoLibre:** 9,000+ developers on Copilot; **~50% less time writing code** (GitHub vendor case study, undated).

**The Telemetry Gap:** Most disclosures are *input* metrics (share of code written by AI). Output-side numbers are rarer and none is an end-to-end delivery metric (lead time, deployment frequency). Apple, Netflix, Salesforce, Cisco and GitLab disclose no internal engineering output metric. Non-disclosure is itself the finding. Our **working hypothesis (not a disclosed metric)** is that review-bottlenecked, end-to-end organisational shipping gains sit around 5%–15%.

---

## 2. Multi-Year Historical Trajectory Matrix (2024–2026), verified rows only

| Company | Period | Internal Tool | AI Adoption / Code Share | Measurable Output | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Google** | Oct 2024 | Internal AI coding tools | **>25%** of new code AI-generated | Not disclosed | ✅ |
| | Fall 2025 | Internal AI coding tools | **50%** of new code (restated Apr 2026) | Not disclosed | ✅ |
| | Apr 2026 | Agentic workflows | **75%** of new code AI-generated & approved by engineers | One complex migration 6x faster (anecdote) | ✅ |
| **Microsoft** | Apr 2025 | GitHub Copilot | 20%–30% of repo code (CEO, via Mashable) | — | ⚠️ media |
| | Feb–Dec 2025 | GitHub Copilot | 16,223 Cloud+AI engineers studied | **+40.5% PRs**, highest vs zero usage weeks (preprint) | ✅ |
| **GitHub (Microsoft)** | 2022 | GitHub Copilot | RCT, 95 recruited developers | One task **55.8% faster** (71 vs 161 min) | ✅ |
| **Amazon** | 2024 | Amazon Q Developer | **>50%** of production Java systems upgraded in <6 months | **4,500 dev-years** saved; 50 dev-days → hours; 79% of auto-generated code reviews shipped unchanged; $260M/yr | ✅ |
| **Stripe** | Feb 2026 | Minions (one-shot agents) | Not disclosed | **>1,000 merged PRs/week** fully Minion-produced, human-reviewed | ✅ |
| **Meta** | Apr 2025 | — | ~half of development by AI "in the next year" | — | ⚠️ target |
| | H1 2026 | — | Creation org: 65% of engineers writing >75% of committed code with AI | — | ⚠️ target (leaked doc) |
| **Klarna** | Feb 2024 | OpenAI-powered assistant | 2.3M chats, two-thirds of support chats | **700 FTE** equivalent; resolution 11 → <2 min | ✅ |
| | Q3 2025 | AI assistant | — | 853 FTE equivalent; $60M saved | ⚠️ media |

**Removed in the 2026-10-12 audit (no source found anywhere):** Google "+20%/+40% velocity" and "cycle times down 35%"; Microsoft "Copilot Workspace >90% DAU", "security remediation 62% faster", 2026 "multi-agent" row; Amazon 2025 "30,000+ production apps" (source says "tens of thousands"), 2026 "lead times down 90%+"; Stripe 2025 "500 PRs/week"; Meta 2024 "Code Llama 20% acceptance", 2025 "MetaCode 40% of code AI-assisted"; Klarna 2025 "80% of support volume" and 2026 "hybrid rebalance".

### 2b. Cross-Company Empirical Comparison: Expansion Set

| Company | Period | Internal Tool | AI Adoption / Code Share (as defined by company) | Output / Productivity Metric | Status | Source Type |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Zeta Global** | Q1 2026 | Spade | 75% of new code automated | Not disclosed | ✅ | Earnings call |
| | Q2 2026 | Spade | **89.6%** of new code (rounded to 90%) | Added engineers; AI cost <1% of revenue | ✅ | Earnings call |
| **Compass** | Q1 2026 | AI coding tools | 30%–40% of new code | **+20% product dev velocity**, tech OpEx flat | ✅ | Earnings call |
| | Q2 2026 | AI coding tools | **50%–60%** of new code | Not re-quantified | ✅ | Earnings call |
| **N-able** | Q2 2026 | AI coding tools | **47%** of committed code | "Some features" 10–12x faster (anecdotal) | ✅ | Earnings call |
| **Cognizant** | Q3 2025 | Code-assist platforms | ~30% of internal code AI-generated | Not disclosed | ✅ | IR transcript |
| | Q1 2026 | Claude, Gemini, Copilot, Devin, Codex | ~40% of code AI-*assisted* | Not disclosed | ✅ | IR transcript |
| | Q2 2026 | Same | >40% of software development AI-assisted | Not disclosed | ✅ | IR transcript |
| | Target | — | 50% "in the years ahead" | — | ⚠️ target | IR transcript |
| **FactSet** | Q3 FY26 (Jul 2026) | Coding agents | **27%** of committed code (adopting teams only) | Token use 5x QoQ; ~10% tech workforce cut | ✅ | Earnings call |
| **Shopify** | May 2026 | River (Slack agent) | **1 in 8** merged PRs co-authored | 3,536 merged agent PRs / 30 days | ✅ | Engineering blog |
| **Accenture** | May 2024 | GitHub Copilot (RCT) | >80% of participants adopted | **+8.69% PRs**; +15% merge rate; +84% successful builds | ✅ (vendor-published) | Research blog |
| **MercadoLibre** | Undated | GitHub Copilot | 9,000+ of 10,000+ developers | **~50% less time writing code** | ✅ (vendor case study) | Customer story |
| **Cisco** | — | — | Executive AI-coding targets appear only in trade-press interviews; not verified (source blocked) | None | Telemetry gap | — |
| **GitLab** | Q1 FY27 | — | Customer metrics only (Zillow +40% code/engineer) | None for own R&D | Telemetry gap | IR prepared remarks |
| **Apple / Netflix / Salesforce** | — | — | No internal engineering metric found (Salesforce: CEO media claim of "30–50% of the work") | None | Telemetry gap | — |

**Comparability warning:** the denominators differ: *new code* (Zeta, Compass), *committed code* (N-able, FactSet), *internal code / software development* (Cognizant), *merged PRs* (Shopify). FactSet's 27% covers adopting teams only. None of these is an end-to-end delivery metric.

---

## 3. Five Key Structural Discoveries

1.  **The Bottleneck Inversion (interpretation):** AI is drafting a large share of code (Google 75%, Zeta 89.6%), but delivery metrics have not followed in any disclosure. Faros AI telemetry summarised by Port (both vendors) found PRs merged +98% but review time +91% and delivery velocity flat. Our reading: the bottleneck moves to **code review, integration testing, and architectural validation**.
2.  **The Modernization Dividend (Amazon Q, Google):** The largest *quantified* gains disclosed are on mechanical upgrade and migration work (Amazon Java 17 upgrades: ~50 developer-days → hours; Google: one complex migration 6x faster). That testable, well-specified work suits AI is our interpretation, not a company claim.
3.  **The Autonomous Agent Leap (Stripe Minions, Shopify River):** Moving from passive autocomplete in an IDE to asynchronous background agents triggered from Slack yields >1,000 merged PRs/week at Stripe and 1 in 8 merged PRs at Shopify, without developers babysitting the generation process.
4.  **Who Benefits Most (unquantified):** The 2022 Copilot RCT reports heterogeneous effects that "show promise for AI pair programmers to help people transition into software development careers." No primary source in this dataset quantifies a seniority gap (the earlier "+50% to +80%" figure was unsourced and has been removed).
5.  **The Telemetry Gap:** Code-share disclosures are proliferating (Zeta 89.6%, Compass 50–60%, N-able 47%, Cognizant >40%, FactSet 27%), but almost no company ties them to cycle time or delivery throughput. A secondary review of 63 earnings calls found zero linking AI to DORA-style outcomes ([Port, Mar 2026](https://www.port.io/blog/63-earnings-calls-0-engineering-outcomes-tied-to-ai), vendor analysis).

---

## 4. Verified Primary Sources & Citations

1. **Google (>25% of new code, Oct 2024):**
   * *Source:* Sundar Pichai, Alphabet Q3 2024 earnings call remarks (October 29, 2024).
   * *URL:* [https://blog.google/company-news/inside-google/message-ceo/alphabet-earnings-q3-2024/](https://blog.google/company-news/inside-google/message-ceo/alphabet-earnings-q3-2024/)
   * *Quote:* "Today, more than a quarter of all new code at Google is generated by AI, then reviewed and accepted by engineers."
2. **Google (75% of new code, Apr 2026; 50% in fall 2025):**
   * *Source:* Sundar Pichai, Cloud Next 2026 remarks on blog.google (April 22, 2026).
   * *URL:* [https://blog.google/innovation-and-ai/infrastructure-and-cloud/google-cloud/cloud-next-2026-sundar-pichai/](https://blog.google/innovation-and-ai/infrastructure-and-cloud/google-cloud/cloud-next-2026-sundar-pichai/)
   * *Quote:* "Today, 75% of all new code at Google is now AI-generated and approved by engineers, up from 50% last fall." … "a particularly complex code migration done by agents and engineers working together was completed six times faster than was possible a year ago with engineers alone."
3. **Google (Goose internal model):**
   * *Source:* Business Insider, citing leaked internal documents (February 2024).
   * *URL:* [https://www.businessinsider.com/google-goose-ai-model-language-ai-coding-2024-2](https://www.businessinsider.com/google-goose-ai-model-language-ai-coding-2024-2)
   * *Quote:* Goose is a "descendant of Gemini" … "trained on the sum total of 25 years of engineering expertise at Google" … "Goose has a 28k token context window".
4. **Microsoft (+40.5% PRs, highest vs zero usage weeks):**
   * *Source:* arXiv:2606.00438, Heilman, Kyllo & Murphy-Hill (Microsoft), "GitHub Copilot and Developer Productivity: An Observational Dose-Response Analysis" (submitted May 30, 2026). Preprint, not peer-reviewed. 16,223 IC engineers in Microsoft Cloud+AI, 43 weeks (Feb 23 – Dec 21, 2025).
   * *URL:* [https://arxiv.org/abs/2606.00438](https://arxiv.org/abs/2606.00438)
   * *Quote:* "Engineers are estimated to complete 40.5% more PRs in their highest GHCP usage weeks relative to their zero-usage weeks, holding measured development effort constant."
5. **Microsoft (20%–30% of repo code, media-reported):**
   * *Source:* Satya Nadella at LlamaCon (April 29, 2025), as reported by Mashable.
   * *URL:* [https://mashable.com/article/llamacon-mark-zuckerberg-ai-writes-meta-code](https://mashable.com/article/llamacon-mark-zuckerberg-ai-writes-meta-code)
   * *Quote:* "Maybe 20 to 30 percent of the code that is inside of our repos today, and some of our projects, are probably all written by [AI] software."
6. **GitHub / Microsoft Research (55.8% faster on one task):**
   * *Source:* arXiv:2302.06590 (Peng, Kalliamvakou, Cihon, Demirer; Feb 13, 2023) & GitHub research blog (Sept 7, 2022). 95 recruited professional developers (not Microsoft employees), one task: an HTTP server in JavaScript.
   * *URL:* [https://arxiv.org/abs/2302.06590](https://arxiv.org/abs/2302.06590) & [https://github.blog/news-insights/research/research-quantifying-github-copilots-impact-on-developer-productivity-and-happiness/](https://github.blog/news-insights/research/research-quantifying-github-copilots-impact-on-developer-productivity-and-happiness/)
   * *Quote:* "The treatment group, with access to the AI pair programmer, completed the task 55.8% faster than the control group." GitHub: Copilot users "took on average 1 hour and 11 minutes … while the developers who didn't use GitHub Copilot took on average 2 hours and 41 minutes."
7. **Amazon (4,500 developer-years, 79% of auto-generated code reviews, $260M):**
   * *Source (primary):* Andy Jassy LinkedIn post (August 22, 2024). *Supporting:* AWS DevOps blog (August 1, 2024), which states the 4,500 years and $260M but **not** the 79% or 50-developer-day figures.
   * *URL:* [https://www.linkedin.com/posts/andy-jassy-8b1615_one-of-the-most-tedious-but-critical-tasks-activity-7232374162185461760-AdSz/](https://www.linkedin.com/posts/andy-jassy-8b1615_one-of-the-most-tedious-but-critical-tasks-activity-7232374162185461760-AdSz/) & [https://aws.amazon.com/blogs/devops/amazon-q-developer-just-reached-a-260-million-dollar-milestone/](https://aws.amazon.com/blogs/devops/amazon-q-developer-just-reached-a-260-million-dollar-milestone/)
   * *Quote:* "The average time to upgrade an application to Java 17 plummeted from what's typically 50 developer-days to just a few hours. We estimate this has saved us the equivalent of 4,500 developer-years of work (yes, that number is crazy but, real). In under six months, we've been able to upgrade more than 50% of our production Java systems to modernized Java versions … our developers shipped 79% of the auto-generated code reviews without any additional changes … providing an estimated $260M in annualized efficiency gains."
8. **Stripe (>1,000 Merged PRs/Week):**
   * *Source:* Stripe Developer Blog, Alistair Gray (February 9, 2026).
   * *URL:* [https://stripe.dev/blog/minions-stripes-one-shot-end-to-end-coding-agents](https://stripe.dev/blog/minions-stripes-one-shot-end-to-end-coding-agents)
   * *Quote:* "Over a thousand pull requests merged each week at Stripe are completely minion-produced."
   * *Note:* InfoQ (March 20, 2026) reports "over 1,300 pull requests per week, up from 1,000 in earlier trials" from Stripe engineers ([infoq.com](https://www.infoq.com/news/2026/03/stripe-autonomous-coding-agents/)); secondary, not used.
9. **Meta (targets only):**
   * *Source:* Zuckerberg at LlamaCon (April 29, 2025) via Mashable; leaked internal document reported by Business Insider, via Livemint (March 27, 2026).
   * *URL:* [https://mashable.com/article/llamacon-mark-zuckerberg-ai-writes-meta-code](https://mashable.com/article/llamacon-mark-zuckerberg-ai-writes-meta-code) & [https://www.livemint.com/companies/news/mark-zuckerberg-accelerates-metas-ai-native-overhaul-with-strict-ai-coding-targets-for-engineers-report-11774591169815.html](https://www.livemint.com/companies/news/mark-zuckerberg-accelerates-metas-ai-native-overhaul-with-strict-ai-coding-targets-for-engineers-report-11774591169815.html)
   * *Quote:* Zuckerberg: "our bet is sort of that in the next year... maybe half the development is going to be done by AI as opposed to people" (Mashable notes it is unclear whether he meant Llama or Meta overall). Livemint: the creation org "has set a target for the first half of 2026 for 65% of engineers to write more than 75% of their committed code using AI."
10. **Klarna (700 FTEs, resolution 11 → <2 min; customer service):**
   * *Source:* Klarna press release (February 27, 2024).
   * *URL:* [https://www.klarna.com/international/press/klarna-ai-assistant-handles-two-thirds-of-customer-service-chats-in-its-first-month/](https://www.klarna.com/international/press/klarna-ai-assistant-handles-two-thirds-of-customer-service-chats-in-its-first-month/)
   * *Quote:* "The AI assistant has had 2.3 million conversations, two-thirds of Klarna's customer service chats. It is doing the equivalent work of 700 full-time agents … Customers now resolve their errands in less than 2 mins compared to 11 mins previously."
11. **Klarna (853 FTEs, $60M; media-reported):**
   * *Source:* CX Dive (November 20, 2025), reporting the Q3 2025 earnings call; primary transcript not verified.
   * *URL:* [https://www.customerexperiencedive.com/news/klarna-says-ai-agent-work-853-employees/805987/](https://www.customerexperiencedive.com/news/klarna-says-ai-agent-work-853-employees/805987/)
   * *Quote:* The AI customer service agent "can now do the work of more than 853 full-time agents, according to Klarna CEO and co-founder Sebastian Siemiatkowski."
12. **FactSet (27% of Committed Code, Adopting Teams):**
   * *Source:* FactSet Q3 FY2026 Earnings Call, CEO Sanoke Viswanathan (July 1, 2026). Motley Fool verbatim transcript.
   * *URL:* [https://www.fool.com/earnings/call-transcripts/2026/07/01/factset-fds-q3-2026-earnings-call-transcript/](https://www.fool.com/earnings/call-transcripts/2026/07/01/factset-fds-q3-2026-earnings-call-transcript/)
   * *Quote:* "Coding agents now author 27% of committed code in the engineering teams using these tools." … "we initiated a roughly 10% reduction in our technology workforce"
13. **Zeta Global (89.6% of New Code):**
   * *Source:* Zeta Global Q2 2026 Earnings Call, CEO David Steinberg (August 4, 2026). Motley Fool verbatim transcript.
   * *URL:* [https://www.fool.com/earnings/call-transcripts/2026/08/11/zeta-global-zeta-q2-2026-earnings-call-transcript/](https://www.fool.com/earnings/call-transcripts/2026/08/11/zeta-global-zeta-q2-2026-earnings-call-transcript/)
   * *Quote:* "In the second quarter, 90% of our new code generated was automated." … "the actual number for Q2 was 89.6%." … "using our internal workflow management tool, Spade, we were able to literally automate 75% of all new code generated" (Q1).
14. **Compass (30–40% → 50–60% of New Code; +20% Velocity):**
   * *Source:* Compass Q1 2026 (May 5, 2026) and Q2 2026 (August 6, 2026) Earnings Calls, CEO Robert Reffkin. Motley Fool transcripts syndicated on AOL.
   * *URL:* [Q1 transcript](https://www.aol.com/articles/compass-comp-q1-2026-earnings-151715369.html) & [Q2 transcript](https://www.aol.com/articles/compass-comp-q2-2026-earnings-235837000.html)
   * *Quote:* Q1: "We now estimate that 30% to 40% of all new code written at Compass is produced by AI, which is helping accelerate product development velocity by 20%, while keeping our technology OpEx unchanged." Q2: "across the technology organization, 50% to 60% of all new code is now produced by AI"
15. **N-able (47% of Committed Code):**
   * *Source:* N-able Q2 2026 Earnings Call, CEO John Pagliuca (August 10, 2026). Motley Fool verbatim transcript.
   * *URL:* [https://www.fool.com/earnings/call-transcripts/2026/08/17/n-able-nabl-q2-2026-earnings-call-transcript/](https://www.fool.com/earnings/call-transcripts/2026/08/17/n-able-nabl-q2-2026-earnings-call-transcript/)
   * *Quote:* "AI-generated code accounting for 47% of all committed code in the second quarter" … "some features shipping 10x to 12x faster than prior road map estimates"
16. **Cognizant (~30% → >40%):**
   * *Source:* Cognizant IR-hosted corrected transcripts, CEO Ravi Kumar S: Q3 2025 (Oct 29, 2025), Q1 2026 (Apr 29, 2026), Q2 2026 (Jul 29, 2026).
   * *URL:* [Q3 2025](https://cognizant.q4cdn.com/123993165/files/doc_earnings/2025/q3/transcript/Transcript_CTSHQ3-2025-Earnings-Call.pdf) · [Q1 2026](https://cognizant.q4cdn.com/123993165/files/doc_earnings/2026/q1/transcript/Transcript_CTSHQ1-2026-Earnings-Call.pdf) · [Q2 2026](https://cognizant.q4cdn.com/123993165/files/doc_earnings/2026/q2/transcript/Transcript_CTSHQ2-2026-Earnings-Call.pdf)
   * *Quote:* "approximately 30% of our internal code was AI-generated, significantly improving productivity of our developers. We believe it could reach 50% in the years ahead." / "nearly 40% of our code to be AI-assisted." / "Over 40% of our software development is now AI assisted."
17. **Accenture (+8.69% PRs, +84% Successful Builds):**
   * *Source:* GitHub Research, "Quantifying GitHub Copilot's impact in the enterprise with Accenture" (May 13, 2024).
   * *URL:* [https://github.blog/news-insights/research/research-quantifying-github-copilots-impact-in-the-enterprise-with-accenture/](https://github.blog/news-insights/research/research-quantifying-github-copilots-impact-in-the-enterprise-with-accenture/)
   * *Quote:* "Accenture developers saw an 8.69% increase in pull requests." "Accenture saw a 15% increase to the pull request merge rate." "84% increase in successful builds." Vendor-published; an independent re-analysis reports the Accenture effects were not statistically significant.
18. **MercadoLibre (~50% Less Time Writing Code):**
   * *Source:* GitHub customer story (vendor case study, undated).
   * *URL:* [https://github.com/customer-stories/mercado-libre](https://github.com/customer-stories/mercado-libre)
   * *Quote:* "~50% reduction in time spent writing code with GitHub Copilot" · "9,000+ developers using Copilot" · "100,000 pull requests merged per day"
19. **Shopify (1 in 8 Merged PRs Co-Authored by River):**
   * *Source:* Shopify Engineering, "Under the River", Burke Libbey & Javier Moreno (May 28, 2026).
   * *URL:* [https://shopify.engineering/under-the-river](https://shopify.engineering/under-the-river)
   * *Quote:* "one in eight merged pull requests across Shopify is coauthored by it." In a recent 30-day period: 59,918 River sessions, 5,170 Slack channels, 7,000+ people, 3,536 River-coauthored PRs merged.
20. **GitLab (Telemetry Gap: Customer Metrics Only):**
   * *Source:* GitLab Q1 FY2027 Earnings Prepared Remarks (June 2, 2026).
   * *URL:* [https://s204.q4cdn.com/984476563/files/doc_financials/2027/q1/GitLab-Q1FY2027-Earnings-Prepared-Remarks.pdf](https://s204.q4cdn.com/984476563/files/doc_financials/2027/q1/GitLab-Q1FY2027-Earnings-Prepared-Remarks.pdf)
   * *Finding:* Cites customer outcomes only (Zillow: AI-assisted workflows help engineering teams "ship 40% more code per engineer"); no internal engineering output metric.

*All URLs above returned HTTP 200 when tested on 2026-10-12. Earnings-call quotes for FactSet, Zeta Global, Compass and N-able come from Motley Fool verbatim transcripts, because company IR sites did not serve accessible transcripts. Cognizant and GitLab quotes come from IR-hosted documents.*

---

## 5. Audit Log (2026-10-12)

Every original figure was re-checked against its source. Corrections made:

| Item | Was | Now | Why |
| :--- | :--- | :--- | :--- |
| Google 75% | "Unverified target" | ✅ Verified | Pichai states it on blog.google (Apr 22, 2026). **Note:** this overrides the stakeholder rule that locked Google to >25%; the rule predates the disclosure. |
| Google 50% (2025) | Unverified | ✅ Verified (restated) | Same post: "up from 50% last fall". |
| Google velocity (+20%/+40%/+65%, cycle time −35%) | Shown in chart | Removed | No source. |
| Microsoft +40.5% | 2024, "16,000+", "peer-reviewed", June 2026 | 2025 data, 16,223 engineers, preprint, May 30, 2026 | Paper's study window is Feb–Dec 2025; arXiv preprints are not peer-reviewed. |
| Microsoft 55.8% | Presented as Microsoft internal | GitHub RCT, 95 recruited developers, one task | Per the paper and GitHub blog. |
| Microsoft 2025/2026 (62% faster fixes, >90% DAU, 92% adoption, +75% velocity) | Shown | Removed | No source. |
| Amazon 79% | "79% of AI code accepted" | "79% of auto-generated code reviews shipped without additional changes" | Jassy's wording; it is not a general acceptance rate. |
| Amazon source | AWS blog dated 2024-08-22 | Jassy LinkedIn (2024-08-22) + AWS blog (2024-08-01) | The 79% and 50-day figures are only in Jassy's post. |
| Amazon "30,000+ apps", 2025/2026 nodes | Shown | Removed / "tens of thousands" | No source for 30,000 or later years. |
| Stripe 1,300/wk, 500/wk | Shown | >1,000/wk only | Stripe blog wording; 500/wk had no source; InfoQ date corrected to 2026-03-20. |
| Meta 2024/2025 (Code Llama 20%, "MetaCode" 40%) | Shown | Removed | No source. |
| Meta 2026 target | "Meta targets 65% of engineers >75%" | Creation org only, H1 2026, leaked doc via media | Livemint wording. |
| Meta quote | Paraphrase presented as quote | Verbatim from Mashable | — |
| Klarna 853 / $60M | "No primary source" | ⚠️ Media-reported (CX Dive, Q3 2025 call) | Source found; primary transcript not verified. |
| Klarna 2025/2026 chat-share nodes | Shown | Removed | No source. |
| "+50% to +80%" for junior developers | Shown | Removed | No source. |
| Cisco "85% of engineers" / "~70% of portfolio by 2027" | Media-only figures | Removed | Trade-press source returns 403; could not be verified. |
| "500 lines in 10s vs 25 min review" | Shown | Replaced with Faros AI telemetry via Port (labelled vendor) | Original figure had no source. |
| Business Insider Goose quote | Paraphrase | Verbatim | — |
| prices.csv | Several wrong rows | Corrected from official Google pricing page and AWS Price List API | Claude 3.5 Sonnet $6/$30 → $3/$15; Sonnet 4.6 cache $1.50 → $0.30; Gemini 3.1 Pro cache $1.00 → $0.20; Llama 3 70B $0.50/$0.50 → $2.65/$3.50 (Bedrock); Apple/Netflix zeros removed. |
| calc_outputs.csv | Q3 2024 value using a 2026 price; references to non-existent fact_01/02; five identical "company" rows | Anachronistic row removed; refs fixed; one generic row | Arithmetic re-verified (Lens 1: $3.0/$4.0/$5.0; Lens 2b: $0.15/$0.56/$2.78 per 1M). |
| pyramid.csv / coverage_matrix.csv | Cited non-existent fact IDs; "verified" labels with no source | Rewritten to reference existing rows; statuses corrected | — |

