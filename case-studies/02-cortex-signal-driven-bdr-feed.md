# Signal-driven BDR lead feed

**Context:** Cortex. Part of the GTM systems credited with **$1.57M in pipeline influence**.

## Problem

BDRs were working out of a static Salesforce queue: a list of accounts someone decided were a good fit a quarter ago. By the time a rep got to them, the signals that made them good (hiring, funding, tech adoption, product usage) were cold.

Every competitor was buying the same ZoomInfo list and running the same sequences. The way to stand out wasn't a better list. It was a feed built on signals.

## What it does

A daily lead feed that runs on signal, not a static ICP filter.

For each rep, every morning:

1. **Pulls from multiple enrichment sources through Clay waterfalls** — LinkedIn Sales Navigator, ZoomInfo, Clearbit, custom scrapers for intent signals (job postings, tech stack changes, recent funding).
2. **Scores against the current ICP model** — not a fixed scorecard, a model tuned against what was converting that month.
3. **Matches against Salesforce and internal databases** to suppress accounts already in active sequence, already a customer, already a closed-lost, or owned by a different rep.
4. **Routes the highest-priority accounts into the rep's daily workflow** (Salesforce queue + Slack card) with the signal that triggered the score. So the rep knows *why* this account showed up today.

## Scale

- **10,000+ leads scored** across the account population
- **17 builds** at Cortex total; this was the foundation several others plugged into
- Daily feed fed 3 BDRs across 2 segments (SMB + Mid-Market)

## Why signals instead of a static list

Shannon / Ashby's call frame: "validate or kill GTM hypotheses quickly." That's exactly what a signal-driven feed does. Every signal (job posting, funding event, tech adoption) is a testable hypothesis that correlates to buying intent. You run it for 60 days, measure meeting conversion against baseline, and keep what works.

Static lists can't be A/B tested like that. Signal feeds can.

## Stack

- **Enrichment waterfall:** Clay (primary), ZoomInfo, LinkedIn Sales Navigator, Clearbit
- **CRM routing:** Salesforce (Certified Platform Administrator), HubSpot (5 years), Marketo
- **Jobs:** trigger.dev for the daily refresh
- **Suppression + dedup logic:** Python + Clay tables
- **Delivery:** Salesforce custom object → BDR daily queue + Slack

## Measurable impact

- Part of systems credited with **$1.57M in pipeline influence**
- Replaced a hand-maintained static queue that was costing a BDR ~3 hours a week of list hygiene
- Signal categories ranked by actual meeting conversion rate, re-ranked monthly (the loop)

## Why this matters for Foley

The Foley role is explicitly "sales and marketing function, building tools, maintaining those tools, making sure they're working." A signal-driven lead feed is the first thing I'd be looking at in a 90-day plan: it compounds, it's measurable, and every follow-on build (routing, scoring, outreach agent) plugs into the same scaffolding.

**Foley signal catalog (same pattern, different inputs):** new DOT authority, fleet growth, safety events, Clearinghouse / renewal timing, self-serve vs enterprise intent—each becomes a testable hypothesis with a 60-day conversion read and a kill rule.
