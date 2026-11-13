# Joseph DeVille — GTM Engineering Portfolio (Foley)

**Role:** [GTM Forward Deployed Engineer](https://jobs.ashbyhq.com/foley/91ed4c27-47fe-44e1-a501-78de7bcdfdae/application) · Hiring manager: Misha Sulpovar (CAIO)

Former IT / cloud admin turned GTM engineer. 8+ years across SaaS (SDR, admin, GTM engineer). I build the systems reps and marketers actually use—scoring, routing, enrichment agents, outbound infrastructure, deliverability—and measure everything against pipeline and conversion.

At **Cortex** I was the first in-house GTM engineer (**17 builds**). Systems credited with **$1.57M pipeline influence** and **10,000+ leads scored**. Post-Cortex I consult on **Anchor Browser** and **Crux**; both engagements started from my own outbound.

---

## Start here (5 builds)

| # | Build | Outcome | Try it |
|---|--------|---------|--------|
| 1 | **Deep Research + Hermes** — research → persona → outbound + learning loop | Part of **$1.57M** pipeline influence; pre-call research automated | **[Interactive demo](./demo/index.html)** · [case study](./case-studies/01-cortex-deep-research-agent.md) |
| 2 | **Signal-driven BDR feed** — Clay waterfalls, daily signal scoring, CRM routing | **10,000+** leads scored; replaced static Salesforce queues | [case study](./case-studies/02-cortex-signal-driven-bdr-feed.md) |
| 3 | **Outbound + experiment discipline** (Anchor Browser, Crux) | Self-sourced clients; **kill rule at 500 sends/variant**; ~1.7–1.9% reply benchmark | [case study](./case-studies/04-anchor-browser-crux-outbound.md) |
| 4 | **Deliverability infrastructure** (Rainforest QA) | **40%** drop in hard bounces; cross-platform suppression | [case study](./case-studies/03-rainforest-qa-deliverability.md) |
| 5 | **GTM account intelligence** (public reference build) | Scored accounts + **eval rubric** before rep queue (grounding, consistency) | [Repo](https://github.com/josephdeville/sanity-gtm-account-intelligence) · [Live demo](https://jd-sanity-gtm-brief.netlify.app) |

**Open-source sibling to the Cortex agent stack:** [ai-sdr-engine](https://github.com/josephdeville/ai-sdr-engine) (multi-agent research, human-in-the-loop approval, reply classification). Cortex production code (`cortexai-sdr`, `centralbrain`) is private; architecture and output shape are documented in case study 1 and the demo.

---

## Interactive demo (recommended first click)

**[Open Deep Research + Hermes →](./demo/index.html)**

Three personas × verticals—including a **consensus, risk-aware buyer in a regulated services firm** (prospect 2), which mirrors how Foley sells into fleet compliance (committee, audit trail, reversibility). Walk research packet → persona → close plan → Hermes variants → simulated learning signal. Static HTML, no API keys.

---

## How this maps to Foley’s GTM FDE role

| Foley priority (from role description) | Evidence in this portfolio |
|----------------------------------------|------------------------------|
| **Generator, not coordinator** — hypothesis → experiment → ship → read result | Anchor/Crux: outbound first, then build; kill rules on every variant |
| **Research & enrichment agents** before the rep does | Deep Research + Hermes; [ai-sdr-engine](https://github.com/josephdeville/ai-sdr-engine) |
| **Signal / trigger detection** (e.g. DOT authority, fleet growth, renewals) | Signal-driven BDR feed pattern—same loop, different signal catalog |
| **Scoring, qualification, routing** | Daily Clay waterfall → Salesforce/Slack; sanity-gtm eval-gated queue |
| **Personalized outbound + deliverability you own** | Hermes + Rainforest suppression/throttling + Anchor multi-domain fleet |
| **Attribution & experimentation** | LangFuse prompt/reply linkage; monthly signal re-rank; 500-send kill rule |
| **Regulated market judgment** | Demo prospect 2 + deliverability guardrails; consent/PII called out in operating principles |
| **Platform evals / observability** | LangFuse at Cortex; coded eval rubric on [GTM account intelligence demo](https://jd-sanity-gtm-brief.netlify.app) |

---

## First 90 days (draft)

1. **Weeks 1–2:** Inventory GTM hypotheses with marketing + sales; pick one **high-reversibility** experiment (signal or messaging) with a pre-agreed metric and kill rule.
2. **Weeks 2–4:** Stand up a **signal-driven daily feed** prototype (enrichment waterfall + CRM suppression + Slack delivery)—Foley’s analog to DOT authority / fleet growth / renewal triggers.
3. **Weeks 3–6:** Ship a **research brief agent** for top-of-funnel and mid-market reps (calendar- or queue-triggered), with LangFuse or platform-native logging for auditability.
4. **Ongoing:** Own **deliverability** primitives before outbound volume scales; document a learning log so failed experiments aren’t repeated.

Full operating frame: [How I work](./case-studies/05-operating-principles.md).

---

## Case studies (detail)

1. [Deep Research + Hermes](./case-studies/01-cortex-deep-research-agent.md)
2. [Signal-driven BDR lead feed](./case-studies/02-cortex-signal-driven-bdr-feed.md)
3. [Email deliverability — 40% bounce drop](./case-studies/03-rainforest-qa-deliverability.md)
4. [Anchor Browser & Crux outbound](./case-studies/04-anchor-browser-crux-outbound.md)
5. [Operating principles](./case-studies/05-operating-principles.md)

---

## Stack

TypeScript, Python · LangChain, Crew AI, LangFuse, trigger.dev · Salesforce (Certified Administrator), HubSpot, Marketo · Clay, ZoomInfo, LinkedIn Sales Navigator · Smartlead, Instantly · AWS, Azure

---

## Contact

Joseph DeVille · Houston, TX  
[joseph.deville@cloudanditservices.com](mailto:joseph.deville@cloudanditservices.com) · (337) 802-6686  
[LinkedIn](https://www.linkedin.com/in/joseph-deville/) · [GitHub](https://github.com/josephdeville)

**Share this portfolio:** [github.com/josephdeville/foley-portfolio](https://github.com/josephdeville/foley-portfolio) · after GitHub Pages is enabled: `https://josephdeville.github.io/foley-portfolio/`
