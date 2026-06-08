# Granite

**An interactive walkthrough of an enterprise AI-assistant architecture for a regulated bank.**

Granite is an interactive walkthrough of how you build an AI assistant a large, regulated financial
institution can actually trust. Pick an example question and trace it through the system — intent
classification, an entitlements gate, deterministic data, grounded synthesis, an LLM-as-judge — and watch
it *refuse rather than guess* when it isn't sure.

It answers a two-fold problem: a **user** problem (information fragmented across legacy and modern systems —
"workflow collapse") and an **environment** problem (a regulated, archaic-data setting whose constraints
*generated* the architecture rather than merely limiting it).

## Real vs. simulated
Drawn from real product work and fully sanitized.

- **Real:** the architecture patterns, the design principles, and the regulated-finance reasoning — each
  validated against current research and standards (see the References section on the page).
- **Simulated:** there is no live AI here. Every example and data point is fabricated, and no real
  institution, product, or vendor is named.

## The architecture, in one line
Chat overlay → orchestration → confidence-routed intent → entitlements gate → deterministic supervisor →
domain lanes (deterministic API + RAG + synthesis) → LLM-as-judge → response assembly — with a fail-closed
refusal on any failure and audit/telemetry throughout.

The organizing principle: **a wrong answer is worse than no answer.**

## Build
Vanilla HTML/CSS/JS — a single self-contained `index.html`, no build step, no backend. Deployed static to
Vercel. Design tokens are shared with the rest of the portfolio for cohesion when embedded.

---
Illustrative concept by Michael Cerpa.
