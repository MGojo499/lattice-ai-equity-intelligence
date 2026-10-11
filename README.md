# Lattice

Personalized AI research desk for tokenized U.S. equities.

**Bitget AI Base Camp S2** · AI Trading Desk · Personalized Research Workbench

Lattice helps active retail and prosumer investors research tokenized U.S. equities without turning an AI narrative into an unchecked trading decision. It grounds the question in portfolio context, exposes evidence receipts, runs adversarial Bull/Bear reasoning, stress-tests the key assumption, and returns a conditional action for human approval.

## Demo

- Live demo: https://6mh9u44e.mule.page/
- Final subtitled walkthrough: `Lattice_Demo_Final_Subtitled.mp4.`
- https://youtu.be/zO7TUm4WndM
- Use the **Guided demo** button for the required question-to-action research flow.

All prices, instruments, portfolio values, AI responses, and orders in the public static demo are simulated.

## What makes it different

- **Orbit:** a personalized “market friend” that challenges confirmation bias and position-size mistakes.
- **Thesis Court:** separate Bull, Bear, and Judge roles produce a conditional verdict and invalidation rule.
- **Signal receipts:** evidence categories expose freshness, confidence, and provenance rather than hiding the research trail.
- **Scenario Lab:** traces one changed assumption through the existing basket and checks risk guardrails.
- **Basket Composer:** converts a research result into a simulated tokenized-equity allocation while keeping the human in control.

## End-to-end research task

1. Ask whether to add NVDAx before the next earnings cycle.
2. Load portfolio constraints and risk rules.
3. Reconcile cloud capex, supply-chain, and options evidence.
4. Debate the thesis through Bull, Bear, and Judge roles.
5. Stress hyperscaler capex growth.
6. Return a size-aware action with an explicit invalidation condition.

## Architecture

```text
Browser UI → /api/orbit → Bitget Qwen Responses API
     │                         │
     ├─ portfolio context      ├─ extraction / synthesis
     ├─ scenario controls      ├─ adversarial reasoning
     └─ human approval         └─ risk-aware explanation
```

The Node server keeps the Qwen credential off the client. If no credential is configured, Orbit clearly falls back to deterministic demo mode.

## Access the demo

Open the live demo: https://6mh9u44e.mule.page/

Use the Guided Demo button to follow the research workflow.

Important: The public demo uses simulated data and responses. It does not execute real trades.

This repository contains the available project files, validation materials, and demo recordings. The complete server-side application is not included.

## Validation

The repository includes:

- `VALIDATION_PLAN.md` — task protocol and success criteria
- `results-template.csv` — blank participant-level results sheet

No external-user, trading-return, volume, or AUM result is claimed yet. Record results only after real sessions and label every metric observed, estimated, or targeted.

## Security and product safeguards

- API keys remain server-side.
- Request bodies are size limited.
- User input is rendered as text, not executable HTML.
- Static paths are normalized to prevent traversal.
- A restrictive Content Security Policy is included.
- The product does not submit orders and keeps the human as final decision-maker.
- Demo and financial-risk disclosures are visible in the interface.

## Current limitations

- The public static deployment uses deterministic data and responses.
- Bitget MCP market data and authenticated wallet execution are not connected.
- Evidence-receipt source URLs and persistent user memory are not implemented.
- The Qwen route becomes live only when a valid credential is provided to the server environment.

## Roadmap

1. Activate Qwen reasoning through the included server route.
2. Connect Bitget MCP read-only U.S. stock and ETF data.
3. Add source-level receipts and timestamped evidence snapshots.
4. Persist user theses and risk preferences with explicit consent controls.
5. Run the documented user study and publish observed metrics.

## License

Hackathon prototype. All third-party names and marks belong to their respective owners.
