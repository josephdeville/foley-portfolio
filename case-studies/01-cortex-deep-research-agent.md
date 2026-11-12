# Deep Research + Hermes — the end-to-end GTM agent system

**Context:** Cortex. First in-house GTM engineer. The two agents below ran as one connected pipeline.

**🎮 Try them live:** [`/demo`](../demo/index.html) — three pre-loaded prospects, step through the full agent output

---

## The problem

AEs were booking meetings and walking in cold. Generic research, no persona read, no close plan. Marketing was generating content that was either safe-and-bland or on-brand-but-slow. Both problems had the same root: human attention was the bottleneck, and nothing scaled.

So I built two agents designed to run as one system.

---

## Deep Research — the brain

**What it does:** triggered on any calendar event with an external attendee, pulls a full research packet on the company + person + account history, writes a persona-aware close plan.

**The research packet:**

- Company signals (funding, hiring, tech stack, news, filings)
- Attendee profile (role, tenure, prior companies, posts, mutual connections)
- Prior touches: every email, meeting, product-usage event, and opportunity on the account

**The persona read:**

Not demographic. Behavioral. The agent infers: how this person makes decisions (consensus vs. decisive, data vs. story, cautious vs. bet-the-farm), what motivates them professionally, what they publicly care about, what to say, what *not* to say.

**The close plan:**

Which product angle to lead with. What objection they're statistically most likely to raise. What proof points land for this persona. Where the deal is likely to stall and what pre-empts it.

Delivered as a one-page brief in Slack, 30 minutes before every meeting.

---

## Hermes — the hands

**What it does:** turns the research packet into actual outbound. Cold emails, follow-ups, LinkedIn messages, nurture content.

**The copy:**

- Personalized to the research packet, not merge-fielded ({{first_name}} + hope-this-finds-you-well does nothing)
- Written in the voice of the sender (tone cloned from their actual sent mail, not a default template)
- Tuned to the persona Deep Research surfaced — decisive buyers get a different frame than consensus buyers
- A/B variants generated in parallel, with the agent biasing toward whatever's converting in the current quarter

**The nuance:**

Hermes isn't a template-filler. It writes something new per prospect and tests whether that something worked. Reply = positive signal. Meeting booked = stronger signal. Deal progression = strongest. The agent re-weights its own choices against those signals continuously.

---

## Why this is a self-improving system, not a task pipeline

Scoring agents, routing agents, enrichment agents are task agents. They do one thing against a schema and self-improvement adds no value.

Deep Research + Hermes has to decide what to say to this person right now. That decision has to get better as we see more responses. The learning loop:

1. Hermes writes copy variant A, B, C → sends
2. Reply / open / meeting / opportunity events flow back
3. Persona model updates: "decisive buyers in payments at Series B companies respond 2.3x to variant B this quarter"
4. Deep Research's next close plan biases Hermes toward variant B for that persona
5. Repeat

LangFuse holds every prompt version, every output, every reply event, tied back to the pipeline event. That's what makes it auditable, not just automated.

---

## Stack

- **Orchestration:** Crew AI for multi-agent handoff (researcher → persona-analyzer → copywriter → brief-assembler)
- **Languages:** TypeScript + Python
- **LLM observability + prompt versioning:** LangFuse
- **Framework:** LangChain for retrieval + tool-calling
- **Jobs:** trigger.dev — calendar webhook → agent run, scheduled refresh for ongoing accounts
- **Data:** Clay waterfalls for enrichment, Salesforce for account + opportunity history, LinkedIn Sales Navigator, company news APIs
- **Delivery:** Slack brief to the AE, copy drafts to the sender's outbox, Salesforce activity + custom object write-back

---

## Measurable impact

- Part of the systems credited with **$1.57M in pipeline influence** at Cortex
- AEs stopped spending 30–45 minutes of manual pre-call research per meeting
- First-to-second meeting conversion lifted (figure available in the next round)
- Reply rates on Hermes-generated outbound tracked per persona segment with a kill-rule at 500 sends

---

## Try the agents

Three pre-loaded prospects, each a different persona × company type. Walk through what Deep Research surfaces and what Hermes writes for each:

**→ [Open the live demo](../demo/index.html)**

Each example shows:
1. The research packet Deep Research pulls
2. The persona read + close plan
3. Three Hermes-generated outbound variants
4. What the agent would re-weight toward based on simulated reply signal

---

## Why this matters for Foley

Ashby's exact words on the call: *"someone that can create things that are continuously learning and iterating because we are evolving and our tooling is going to need to evolve with us."*

This is that pattern. I've built it once. The second build is faster, and the architecture generalizes — the same research + persona + copy + learning loop works for legal-services outbound as cleanly as it worked for dev-tools outbound.
