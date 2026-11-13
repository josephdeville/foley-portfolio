# Email deliverability infrastructure — 40% bounce drop

**Context:** Rainforest QA. Owned email sending across several marketing platforms.

## Problem

Hard bounces were climbing and putting the sender reputation at risk. When I traced it back, bad addresses were slipping into sends with nothing filtering them out. Not one broken system, several: list imports with no verification step, re-engagement sends to addresses that had been quiet for 12+ months, and no suppression workflow between platforms so a bounce on one tool didn't suppress on the others.

Left alone, this was a soft-landing-zone-to-blacklist curve measured in weeks, not months.

## What I built

Three layers:

1. **Automated bounce handling + cross-platform suppression.** A single suppression source of truth, synced out to every sending platform on a schedule. A bounce anywhere suppressed everywhere, immediately.
2. **Throttling.** Per-mailbox daily caps, per-domain-receiver (Gmail / Outlook / Yahoo) pacing, and ramp curves for anything new or reactivated.
3. **ISP-specific sending rules.** Separate send windows and warmup profiles per major receiver. What Gmail tolerates isn't what Microsoft tolerates, and sending the same way to both was part of the problem.

## Measurable impact

- **Hard bounces dropped 40%**
- Sender reputation recovered inside the quarter
- Suppression logic became the shared primitive for everything that came after (sequences, nurture, re-engagement)

## Stack

- **Languages:** Python (bounce parser, suppression sync), SQL for the single source of truth
- **Platforms:** multiple marketing + sending tools (names available on request)
- **Infrastructure:** scheduled jobs for cross-platform suppression sync, webhook handlers for real-time bounce events
- **Data:** SPF / DKIM / DMARC alignment check before volume, custom tracking domain, domain health monitoring

## Why this matters for Foley

Deliverability is the quiet, unglamorous half of GTM infrastructure that nobody wants to own until it breaks. Foley is scaling AI-driven outbound into a **regulated B2B market** (DOT / FMCSA, consent, PII)—sending volume and compliance complexity rise together. Someone has to own suppression, throttling, and receiver-specific rules before reputation damage shows up in pipeline. I've done the recovery once. I'd rather build it right from day one than clean it up later.
