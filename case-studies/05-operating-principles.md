# How I work — GTM engineering operating principles

Not a case study. The frame I use to scope and prioritize so a 90-day plan actually ships something measurable.

## One foot in pipeline, one in process

Every week has two kinds of work:

- **Pipeline work.** Something that, if it ships, directly generates revenue this quarter. A lead feed, a scoring model, an outbound agent, a sequence that converts better.
- **Process work.** Something that lets the people around me (AEs, SDRs, marketers) stop losing time to the things they shouldn't be doing manually. A follow-up draft that lands in Slack when an AE goes silent on six opportunities. An auto-enriched meeting brief. Suppression hygiene that no one has to think about.

If a week is all pipeline, I've under-invested in the compounding stuff. If it's all process, I've gone invisible to revenue. The ratio changes with the quarter, but both are always there.

## Measure in pipeline language, not activity language

Builds don't get credit for existing. They get credit for moving a number that shows up in the forecast. "Agent shipped" is not a metric. "Meeting conversion from the booked-meeting population lifted X%" is.

At Cortex this was the discipline that got $1.57M in pipeline credited to the systems I built — not because it was a marketing claim, but because every system was instrumented against the pipeline event it was supposed to influence, and the attribution model was agreed with RevOps before the build started.

## Prioritize against reversibility and blast radius

Foley has a backlog of AI ideas. Not all of them are equal. I rank them on two axes:

- **Reversibility:** can I ship this, measure it, and kill it in 2 weeks if it doesn't work? Fast-reversible ideas go first.
- **Blast radius:** who does this touch? A tool that only affects one BDR's workflow is lower-stakes than one that gates every outbound send from the company.

High-reversibility, low-blast-radius: ship this week, measure next, keep or kill in 30 days.

High-reversibility, high-blast-radius: pilot on a segment first, expand only on signal.

Low-reversibility (regulated data, customer-facing, legal review required): slow down, scope precisely, design the measurement before you build.

## Build tools that learn, when the task warrants it

Not every agent needs to be a learning agent. An integrator, a router, a scorer, a simple enrichment call: those are task agents. They do one thing against a schema, and self-improvement adds no value.

Learning agents are for the decisions that need nuance: what to say, when to say it, which frame lands, which signal matters this month. Those decisions get better with feedback loops — reply rates, stage progression, revenue attribution — and the agent should be re-weighting itself against those signals continuously.

Deciding which is which is half the engineering work.

## Communicate in writing, early

Every build gets:

- A one-paragraph problem statement before I start
- A measurable outcome (pipeline event, conversion metric, time saved)
- A kill rule (if X doesn't happen by Y date, we kill it)
- A post-ship note: what worked, what didn't, what I learned

This is how a small team keeps up with a shipping GTM engineer without needing to be in every build decision. Also how I'd expect to work with Misha.
