# Video Generation Model Study

Purpose: choose which AI video model(s) to subscribe to for motion video projects.
Audience: the project owner AND other AI models/agents that will write prompts, run tests, or update this study.

## How to use this folder (for AI agents)
1. Read `requirements.yaml` first. It is the source of truth for what the owner needs.
2. Read `models.yaml` for candidate models. Every row has `confidence` and `verified_on`. Treat anything `unverified` as a lead, not a fact. Pricing changes often: re-check vendor pricing pages before advising a purchase.
3. Run the tests in `evaluation-plan.md` and record results in `results/` (one file per model per test, named `<model>__<test-id>.md`).
4. Update the recommendation section below only from recorded results.

## Status
- Phase 1 (requirements + landscape scan): done, 2026-10-23.
- Phase 2 (hands-on tests on free tiers/trials): not started.
- Phase 3 (final recommendation): not started.

## Key tension in the requirements
The owner wants long clips, native audio, character consistency, 1080p-4K, and all four input modes, on under $30/month. No single plan covers all of it. Expect to prioritize:
- Rank the must-haves vs nice-to-haves (open question in `requirements.yaml`).
- Long clips are usually made by chaining/extending 5-10s shots, not one generation.
- 4K is typically upscaled or a premium tier; 1080p is the realistic target at this budget.

## Preliminary shortlist (UNVERIFIED, from secondary sources; to be tested)
| Role | Candidate | Why |
|---|---|---|
| Cinematic + native audio | Google Veo 3.1 (via Google AI plan) | Strong realism, audio always on |
| Character/story, value | Kling 3.0 | Reputation for character-driven shots, cheap per second |
| Edit / VFX / video-to-video | Runway Gen-4.5 | Editing-oriented tooling |
| Cheapest iteration | Wan, Seedance Fast, Hailuo Fast | Low per-second cost |
| Multi-model aggregator | Higgsfield and similar | One plan, many models; check credit limits |

## Sources (secondary, vendor/affiliate blogs: verify on official pages)
- https://www.teamday.ai/blog/best-ai-video-models-2026
- https://www.atlascloud.ai/blog/tips/best-ai-video-generation-models-2026
- https://higgsfield.ai/blog/best-affordable-ai-video-generators
- https://aitoolsbakery.com/blog/ai-video-generator-pricing-compared/
