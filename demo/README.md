# Interactive Demo

Static, self-contained walkthrough of Deep Research + Hermes output. No backend, no API keys, no tracking.

## View it

**Option 1 — Open the file directly**
Double-click `index.html` or drag it into your browser. Works offline.

**Option 2 — GitHub Pages (recommended for sharing)**
If this repo is on GitHub, enable Pages (Settings → Pages → source: main, folder: /root), then the demo is live at:
`https://josephdeville.github.io/foley-portfolio/demo/`

**Option 3 — Any static host**
Drop the whole `foley-portfolio/` folder into Netlify, Vercel, Cloudflare Pages, GitHub Pages — anything that serves static files.

## What the demo shows

Three pre-loaded prospects representing different personas × verticals:

1. **Technical Decisive** — VP of Engineering at a dev-tools SaaS
2. **Consensus Risk-aware** — Head of Operations at a mid-market law firm
3. **Numbers-First Analytical** — Director of Finance at a Series B payments company

For each prospect, you see:

- The research packet Deep Research would pull
- The persona read it would infer
- The close plan it would recommend
- Three Hermes-generated outbound variants

Click any variant to see the simulated learning signal that would re-weight it for future sends to that persona.

## What the demo doesn't do (and why)

This is a **static walkthrough**, not a live API that generates fresh outputs. Two reasons:

1. **Cost and abuse surface.** A live demo calling LLM APIs needs rate limits, auth, and ongoing spend. Not the right starting point for a portfolio piece.
2. **Fidelity of example.** The point of this demo is to show what the agent *produces*, not to prove the generator works. Hand-picked examples with full context are a better signal than live calls with no context.

If you want a live run against a real prospect, that's a 30-minute conversation and a shared screen — happy to do it on the next call.

## Full architecture

See [`../case-studies/01-cortex-deep-research-agent.md`](../case-studies/01-cortex-deep-research-agent.md) for the stack, the learning loop, and the measurable impact at Cortex.
