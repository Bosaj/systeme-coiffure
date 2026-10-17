# Système Coiffure

> Pick a haircut that suits your face, preview it, and send a clear brief straight to your barber.

**Status:** pre-alpha scaffold (no code yet). **Feasibility rating:** 3/10 as a new idea — previews are crowded; the barber workflow is the differentiator.
**Idea:** #05 in the owner's ideas backlog. **Author:** Oussama EL HADJI. Part of the Bosaj ideas portfolio (sibling repo: `dual_portfolio_hub`).

---

## Problem

Clients cannot explain the haircut they want, and barbers guess. Photos from the internet do not match the client's face or hair type.

## Why build it (gap analysis)

Many apps already generate hairstyle previews. The unmet part is the client-barber loop: a saved haircut profile, a structured brief (clipper guard numbers, length on top, fade height), and a barber-side view.

## Prior art & open bases to fork

- [google-ai-edge/mediapipe](https://github.com/google-ai-edge/mediapipe) — Face Landmarker for face-shape measurements.
- [huggingface/diffusers](https://github.com/huggingface/diffusers) — Inpainting pipelines for hairstyle previews.

## Proposed architecture

1. Face analysis: landmarks give face shape and proportions; the user states hair type.
2. Recommender: rules from barber knowledge map face shape + hair type to suitable cuts.
3. Preview: hair-region inpainting on the user photo (clearly labelled as an approximation).
4. Brief + barber view: a shareable card with measurements and reference images; barbers keep each client's history.

## Tech stack (proposed)

- React web app (mobile first)
- MediaPipe Face Landmarker (in browser)
- Diffusion inpainting API
- Supabase for barbers and client profiles

## Roadmap

- v0.1 — Face-shape analysis + rule-based recommendations.
- v0.2 — Structured haircut brief and share link.
- v0.3 — AI preview on the user photo.
- v0.4 — Barber dashboard with client history.

---

## For LLM agents & contributors continuing this project

This repo is a **scaffold**: README + standard files, no implementation yet. If you are an AI agent asked to "continue developing", read this section first.

- Validate with 5 barbers in Oujda before building the preview: the brief alone may be the product.
- Photos are biometric data: process in the browser where possible and never keep them without consent.

**Ground rules:** keep this README in sync with reality as you build; prefer forking/reusing the bases above over greenfield code; write tests for anything correctness-critical; never commit secrets (see `.gitignore`); follow Conventional Commits (see `CONTRIBUTING.md`).

## Getting started

```bash
# nothing to run yet — this is a scaffold.
```

## License

[MIT](LICENSE) — © 2026 Oussama EL HADJI
