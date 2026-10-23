# Evaluation Plan

Goal: same tests, every candidate, scored identically, using free tiers/trials first.

## Fixed test set (run each on every model)
| ID | Test | Input mode | What it checks |
|---|---|---|---|
| T1 | Cinematic dolly shot, 8s, with ambient sound | text | realism, audio |
| T2 | Animate one of the owner's own stills, 5s | image | fidelity to source |
| T3 | Same character in 3 different shots | image refs | consistency |
| T4 | Start frame + end frame, 5s | frames | motion control |
| T5 | Restyle a 5s reel clip | video | video-to-video |
| T6 | Animated logo/type, 5s loop | text/image | motion-graphics quality |
| T7 | Extend/chain to 15-20s | any | long-clip workflow |

## Scoring (1-5 each)
fidelity to prompt, motion quality, consistency, audio quality, artifacts, controllability.
Also record: credits consumed, wall-clock time, resolution delivered, license/commercial terms.

## Record format (`results/<model>__<test-id>.md`)
```
model, plan/tier, date, prompt (verbatim), settings, scores, credits_used, notes, output_link
```

## Decision rule
Pick the cheapest plan (or 2-plan combo) under $30/mo that scores >=4 on the owner's ranked must-haves. If none exists, report the trade-off and the cheapest upgrade path.
