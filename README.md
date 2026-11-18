# Joseph DeVille — GTM Engineering Portfolio

Live site: **[josephdeville.com](https://josephdeville.com)** · Interactive walkthrough: **[/demo](https://josephdeville.com/demo/)** · Case studies: **[/case-studies](https://josephdeville.com/case-studies/)**

Former IT and cloud admin turned GTM engineer with 8+ years across B2B SaaS (SDR, CRM admin, RevOps, GTM engineer). I build the systems reps and marketers actually use: signal feeds, scoring, routing, enrichment agents, personalized outbound, and deliverability infrastructure, measured against pipeline and conversion.

At **Cortex** I was the first in-house GTM engineer (**17 shipped builds**), with systems credited for **$1.57M in pipeline influence** and **10,000+ leads scored**. Alongside Cortex, I cut hard bounces **40%** at **Rainforest QA** and built outbound and research engines for B2B teams including **Anchor Browser** and **Crux**.

### Architecture split

- **Task systems** (routing, scoring, enrichment waterfalls, CRM sync, suppression): deterministic schema work where strict rules, idempotency, and observability beat open-ended prompting.
- **Learning agents** (account research, buyer persona reads, outbound copy): decisions that improve when reply rates, booked meetings, and stage progression feed back into prompt framing, gated by eval rubrics and human review.
- **Operating cadence:** one foot in **pipeline** (revenue this quarter), one in **process** (compounding hours saved for sales and marketing).

---

## Core builds & writeups

| # | Build | Outcome | Links |
|---|-------|---------|-------|
| 1 | **Deep Research + Hermes** — calendar-booking trigger → research packet → persona/close plan → learning outbound | Part of **$1.57M** pipeline influence; pre-call brief in Slack ~30 min before the meeting | **[Interactive demo](./demo/index.html)** · [Case study](./case-studies/01-cortex-deep-research-agent.md) |
| 2 | **Signal-driven BDR feed** — Clay waterfalls, daily signal scoring, Salesforce suppression & routing | **10,000+** leads scored; replaced static Salesforce queues | [Case study](./case-studies/02-cortex-signal-driven-bdr-feed.md) |
| 3 | **Deliverability infrastructure** (Rainforest QA) | **40%** drop in hard bounces; cross-platform suppression sync | [Case study](./case-studies/03-rainforest-qa-deliverability.md) |
| 4 | **Outbound + experiment discipline** (Anchor Browser, Crux) | Self-sourced engagements; **kill rule at 500 sends/variant**; ~1.7–1.9% reply benchmark | [Case study](./case-studies/04-anchor-browser-crux-outbound.md) |
| 5 | **GTM account intelligence** | Scored accounts + coded **eval rubric** before rep queue | [Repo](https://github.com/josephdeville/sanity-gtm-account-intelligence) · [Live app](https://jd-sanity-gtm-brief.netlify.app) |
| 6 | **Forecast Evidence Engine** | MEDDICC Commit vs. evidence-backed Commit executive view | [Repo](https://github.com/josephdeville/forecast-evidence-engine) · [Live app](https://forecast-evidence-engine.vercel.app) |

**Open-source code:** [ai-sdr-engine](https://github.com/josephdeville/ai-sdr-engine) · [ClaudeGTM](https://github.com/josephdeville/ClaudeGTM) · [hermes-superagent](https://github.com/josephdeville/hermes-superagent) · [context-mode](https://contextmode.ai)

---

## Case studies

1. [Deep Research + Hermes](./case-studies/01-cortex-deep-research-agent.md)
2. [Signal-driven BDR lead feed](./case-studies/02-cortex-signal-driven-bdr-feed.md)
3. [Email deliverability — 40% bounce drop](./case-studies/03-rainforest-qa-deliverability.md)
4. [Anchor Browser & Crux outbound](./case-studies/04-anchor-browser-crux-outbound.md)
5. [Operating principles](./case-studies/05-operating-principles.md)

---

## Stack

TypeScript, Python · LangChain, CrewAI, LangFuse, Trigger.dev, AI SDK · Salesforce (Certified Administrator), HubSpot RevOps, Marketo · Clay, ZoomInfo, LinkedIn Sales Navigator · Smartlead, Instantly · AWS, Azure

---

## Contact

Joseph DeVille · Houston, TX  
[LinkedIn](https://www.linkedin.com/in/joseph-deville/) · [GitHub](https://github.com/josephdeville) · [josephdeville.com](https://josephdeville.com)
