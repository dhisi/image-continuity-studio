# Migrate and stabilize NarrativeWeaver

## Build
- Replace the starter with the complete public GitHub project while preserving its script parsing, prompt pipeline, ten-lane Pixazo rendering, retry controls, saved progress, panel review, and video export.
- Keep every provider credential server-only and store the supplied values in Lovable’s encrypted secret store.

## Image quality and continuity
- Replace the saturated American print-comic direction with a light, clean vertical webtoon look matching the screenshots: soft colors, restrained saturation, crisp line art, natural light, and detailed but uncluttered settings.
- Build a deterministic scene ledger before prompt generation. Each continuing scene gets one reusable location fingerprint covering architecture, layout, materials, colors, fixed furniture, landmarks, lighting, and spatial anchors.
- Inject that exact fingerprint into every panel in the scene, while retaining the existing character bible, timestamp fidelity, cast resolution, action, environment, and anatomy rules.
- Remove prompt rules that invent magical decoration or force unwanted color and texture.

## Reliability and verification
- Fix the known populated-scene classification path so a supplied character sheet never turns a people scene into an empty setting.
- Add focused tests for scene/location carryover and prompt composition, then verify the live mobile experience and provider calls without exposing keys.
- Keep a migration ledger covering code, data, providers, secrets, and verification status.

## Technical details
- Preserve TanStack Start and server-only provider modules.
- Use `PIXAZO_API_KEY`, `PIXAZO_API_KEY_1` through `_9`, and `ZAI_API_KEY` only from server runtime environment variables.
- Keep Z.ai on its configured free-model chain and Pixazo as the image renderer; no provider replacement.
