# Outbound infrastructure for consulting clients — Anchor Browser & Crux

**Context:** Post-Cortex consulting. Both clients landed from me outbounding, then building what they asked for once the conversation started.

## Why these two are in the portfolio

Not for the logos. Because they prove the same thesis Foley is hiring for: a GTM engineer who runs the GTM motion well enough to generate their own pipeline, then builds the infrastructure that scales it.

If I can't do it for myself, I can't do it for a company.

## Anchor Browser — browser automation SaaS

**What I built:**

- Outbound infrastructure from scratch: multi-domain sending fleet (22 mailboxes across 5 domains, Google + Azure), warmup orchestration, per-mailbox daily caps
- Fit-gated lead pipeline with multi-source verification (LinkedIn + company data + behavioral signals)
- Scanner-click correction logic (filtering out the ~89% of clicks that are corporate security scanners, not humans)
- Microsegment-based campaign routing so segments get hit with the angle that fits them, not a generic mail-merge

**Scale:** 55+ distinct microsegments mapped, thousands of contacts routed, reply rates benchmarked at ~1.7–1.9% across the active sends.

**Discipline:** every campaign built against a measurable kill rule. At 500 sends per variant, if positive reply <0.5%, kill and rotate. Winners keep going. This is the "validate or kill hypothesis" pattern Foley specifically asked for.

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

## Why this matters for Foley

The role is "first true go-to-market engineer." That means walking into a situation without a defined playbook and figuring out what to build first, build it, measure it, and adjust. That's what consulting is, done well. Both Anchor and Crux got value delivered against a measurable outcome, not a project plan written by someone else.
