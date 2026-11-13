# Joseph DeVille — working GTM prototypes (Foley)

**Role:** [GTM Forward Deployed Engineer](https://jobs.ashbyhq.com/foley/91ed4c27-47fe-44e1-a501-78de7bcdfdae/application) · Misha Sulpovar (CAIO)

This repo is a **landing page**. The portfolio is [github.com/josephdeville](https://github.com/josephdeville): live apps, not a brochure.

At Cortex: first in-house GTM engineer, **17 builds**, **$1.57M** pipeline influence, **10,000+** leads scored. Anchor Browser and Crux started from my own outbound.

### Open these (no login)

| Foley 90-day need | Live URL |
|---|---|
| Research + personalization on a booking-style trigger | **[Hermes walkthrough](https://josephdeville.github.io/foley-portfolio/demo/)** |
| Eval-gated account briefs for reps | **[jd-sanity-gtm-brief.netlify.app](https://jd-sanity-gtm-brief.netlify.app/)** · [repo](https://github.com/josephdeville/sanity-gtm-account-intelligence) |
| Measure pipeline (claim vs evidence) | **[forecast-evidence-engine.vercel.app](https://forecast-evidence-engine.vercel.app/)** · [repo](https://github.com/josephdeville/forecast-evidence-engine) |
| Signal catalog → scored queue | [ITAD sample](https://planitroi-itad-signal-engine-hp.vercel.app/) · [Neo job-post signals](https://neo-signal-engine.vercel.app/) |
| Evidence-gated SDR (clone, `DRY_RUN=1`, `/traces`) | [ai-sdr-engine](https://github.com/josephdeville/ai-sdr-engine) |

Cortex attribution write-up: [joseph-deville-gtm-systems.vercel.app](https://joseph-deville-gtm-systems.vercel.app/)

### Agent philosophy (as discussed on our call)

- **Task agents** (routing, scoring, enrichment): deterministic schema work. Ship, measure, optimize rules. Self-learning adds little.
- **Learning agents** (research, personalization, copywriting, nuanced CRM flows): decisions need continual feedback (replies, meetings, stage progression) so the system re-weights what works.
- **Operating mode:** one foot in **pipeline**, one in **process**.

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

## First 90 days (draft — matches what we discussed)

Foley needs someone to **validate or kill GTM hypotheses quickly**, **prioritize the backlog and ship**, **measure from day one**, and **iterate**. Concrete plan:

1. **Weeks 1–2:** Inventory hypotheses with marketing + sales; pick one **high-reversibility** experiment (signal or messaging) with a pre-agreed metric and kill rule.
2. **Weeks 2–4:** Stand up a **signal-driven daily feed** prototype (enrichment waterfall + CRM suppression + Slack delivery)—Foley’s analog to DOT authority / fleet growth / renewal triggers.
3. **Weeks 3–6:** Ship a **calendar-triggered research brief agent** for reps, with platform-native logging for auditability (LangFuse-style traceability).
4. **Ongoing:** Own **deliverability** before outbound volume scales; keep a **learning log** so failed experiments aren’t repeated.

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

TypeScript, Python · LangChain, **Crew AI**, LangFuse, **trigger.dev**, **AI SDK** · Salesforce (Certified Administrator), HubSpot, Marketo · Clay, ZoomInfo, LinkedIn Sales Navigator · Smartlead, Instantly · AWS, Azure

---

## Contact

Joseph DeVille · Houston, TX  
[joseph.deville@cloudanditservices.com](mailto:joseph.deville@cloudanditservices.com) · (337) 802-6686  
[LinkedIn](https://www.linkedin.com/in/joseph-deville/) · [GitHub](https://github.com/josephdeville)

**Share:** [github.com/josephdeville](https://github.com/josephdeville) · landing: [josephdeville.github.io/foley-portfolio](https://josephdeville.github.io/foley-portfolio/)
