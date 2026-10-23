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

## Update v2 (owner answers)
Priorities: consistency > motion quality. Client + studio marketing work => commercial licence required. Inputs: own source images + style PNGs, varying aspect ratios. Budget now < $100/mo, so a 2-plan combo is viable.
Likely shape: one reference-strong model for hero storytelling shots (Seedance / Kling / Runway, to be decided by tests) + optionally Veo or a cheap model for audio/drafts.

## Update v3
Brand fidelity is exact and non-negotiable. Priority outputs: 9:16 app entry videos (3-6s) and app story videos (5-10s, reused for marketing). Short clips remove the long-clip problem; the deciding factors are style lock via keyframes, 9:16 support, usable-take rate and commercial licence.
Recommended workflow: approved still keyframe -> image-to-video (start frame, optionally end frame) -> light grade/typography in editor.

## Update v4: roles and scope (from owner)
- OWNER writes all prompts and does the creative motion work. Claude does NOT write prompts or evaluate motion taste.
- Claude's role = ops/analyst: shortlist tools and access platforms, check legitimacy of evidence, track pricing/licence, keep these files current, and do only simple motion tasks when asked.
- New files: `platforms.yaml` (where to access models under $100), `evidence-log.md` (tiered real-user evidence; flags vendor/affiliate content).
- `evaluation-plan.md`: any prompt-writing steps are superseded; the owner runs trials with their own prompts, Claude records results and costs.

## Key tension in the requirements (v1, partly superseded)
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
