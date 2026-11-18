# Outbound infrastructure for consulting clients — Anchor Browser & Crux

**Context:** Post-Cortex consulting. Both clients landed from me outbounding, then building what they asked for once the conversation started.

## Why these two are in the portfolio

Not for the logos. Because they show a GTM engineer who runs the GTM motion well enough to source pipeline directly, then builds the production infrastructure that scales it.

If I can't do it for myself, I can't do it for a company.

## Anchor Browser — browser automation SaaS

**What I built:**

- Outbound infrastructure from scratch: multi-domain sending pool (22 mailboxes across 5 domains, Google + Azure), warmup orchestration, per-mailbox daily caps
- Fit-gated lead pipeline with multi-source verification (LinkedIn + company data + behavioral signals)
- Scanner-click correction logic (filtering out the ~89% of clicks that are corporate security scanners, not humans)
- Microsegment-based campaign routing so segments get hit with the angle that fits them, not a generic mail-merge

**Scale:** 55+ distinct microsegments mapped, thousands of contacts routed, reply rates benchmarked at ~1.7–1.9% across the active sends.

**Discipline:** every campaign built against a measurable kill rule. At 500 sends per variant, if positive reply <0.5%, kill and rotate. Winners keep going.

## Crux — payments

**What I built:**

- Outbound stack tuned for the payments buyer (finance / payments operators, high-consideration decision)
- CRM instrumentation so reply quality and meeting conversion were measurable per segment
- Enrichment waterfall built against the specific ICP, not a generic ZoomInfo pull

## Stack across both

- TypeScript, Python
- Smartlead, Instantly, custom sending infrastructure
- Clay for enrichment waterfalls
- HubSpot for CRM instrumentation (Crux), custom pipelines (Anchor)
- trigger.dev for scheduled jobs
- SPF / DKIM / DMARC configuration, custom tracking domains

## Takeaway

Walking into an early-stage GTM team without a pre-written playbook means figuring out what to ship first, instrumenting it from day one, and cutting variants that miss so effort compounds on what converts.

