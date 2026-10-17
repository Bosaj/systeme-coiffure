# 1. Architecture

1. Face analysis: landmarks give face shape and proportions; the user states hair type.
2. Recommender: rules from barber knowledge map face shape + hair type to suitable cuts.
3. Preview: hair-region inpainting on the user photo (clearly labelled as an approximation).
4. Brief + barber view: a shareable card with measurements and reference images; barbers keep each client's history.

## Proposed stack
- React web app (mobile first)
- MediaPipe Face Landmarker (in browser)
- Diffusion inpainting API
- Supabase for barbers and client profiles

## Open bases to fork
- [google-ai-edge/mediapipe](https://github.com/google-ai-edge/mediapipe) — Face Landmarker for face-shape measurements.
- [huggingface/diffusers](https://github.com/huggingface/diffusers) — Inpainting pipelines for hairstyle previews.
