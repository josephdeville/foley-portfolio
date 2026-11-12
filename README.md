# Joseph DeVille — GTM Engineering Portfolio

Built for the GTM Forward Deployed Engineer role at Foley, under Misha.

---

## Positioning

I'm a former IT / cloud admin turned GTM engineer. 8+ years across SaaS: SDR, admin, GTM engineer. I build the systems reps and marketers actually use (scoring, routing, enrichment agents, outbound infrastructure, email deliverability) and measure everything against pipeline and conversion.

At Cortex I was the first in-house GTM engineer. 17 builds shipped. The systems I put in place influenced **$1.57M in pipeline** and scored **10,000+ leads**. Most recent builds were June / July before an executive change cut the single-person function.

Since Cortex I've been consulting on Anchor Browser (browser automation SaaS) and Crux (payments), both landed from my own outbound.

---

## Why this matches what Foley needs in 90 days

| Foley's requirement | What I bring |
|---|---|
| Validate or kill GTM hypotheses quickly | I scope every build against a measurable pipeline or conversion outcome. See the Cortex BDR feed below. |
| Prioritize the AI build backlog and ship immediately | 17 builds in ~6 months at Cortex is the pace. Prioritization is "what moves pipeline this week." |
| Measure impact of everything built from day one | Every case study below leads with the measurable outcome, not the architecture. |
| Build tools that continuously learn and iterate | The Deep Research agent (case study 1) is exactly this pattern: reads context, writes personalized outreach, builds a persona-aware playbook per prospect. |

---

## Try the agents live

**🎮 [Open the interactive demo →](./demo/index.html)**

Three pre-loaded prospects (different persona × vertical). Walk through what Deep Research pulls, what Hermes writes, and what the learning loop re-weights toward based on reply signal. Static, no API keys needed. Also deployable to GitHub Pages or any static host.

---

## Case studies

1. [**Deep Research + Hermes — the end-to-end GTM agent system**](./case-studies/01-cortex-deep-research-agent.md)
   The "continuously learning" build. Deep Research pulls context + builds a persona-aware close plan; Hermes turns that into personalized outbound that re-weights against reply signal. Cortex.

2. [**Signal-driven BDR lead feed**](./case-studies/02-cortex-signal-driven-bdr-feed.md)
   Replaced static Salesforce queues with a daily feed scored off signals (Clay waterfalls, LinkedIn, ZoomInfo), routed into Salesforce / HubSpot / Marketo. Part of systems credited with $1.57M in pipeline influence. Cortex.

3. [**Email deliverability infrastructure — 40% bounce drop**](./case-studies/03-rainforest-qa-deliverability.md)
   Owned email sending across several marketing platforms, built automated bounce handling and suppression workflows, added throttling and ISP-specific sending rules. Rainforest QA.

4. [**Outbound infrastructure for consulting clients**](./case-studies/04-anchor-browser-crux-outbound.md)
   Built the outbound + enrichment stack for Anchor Browser and Crux. Both landed from me outbounding first, then building what they needed.

5. [**How I work — GTM engineering operating principles**](./case-studies/05-operating-principles.md)
   One foot in pipeline, one in process optimization. How I scope, prioritize, and measure.

---

## Stack

- **Languages:** TypeScript, Python
- **Agent frameworks:** LangChain, LangFuse, Crew AI (multi-agent orchestration), AI SDK
- **Jobs & scheduling:** trigger.dev
- **CRM / GTM platforms:** Salesforce (Certified Platform Administrator), HubSpot (5 years), Marketo
- **Enrichment:** Clay (waterfalls, dedup, scoring), ZoomInfo, LinkedIn Sales Navigator, FullEnrich
- **Sending / deliverability:** Smartlead, Instantly, GMass, custom tracking domains, SPF/DKIM/DMARC
- **Infra:** AWS, Azure (prior Azure Administrator background), serverless

---

## Contact

Joseph DeVille
Houston, TX
joseph.deville@cloudanditservices.com
(337) 802-6686
LinkedIn: [to add]
