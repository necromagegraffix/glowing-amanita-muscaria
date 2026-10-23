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
| T8 | Feed 2-3 owner style-reference PNGs + one character image; generate 3 shots in that style at 16:9, 9:16, 1:1 | refs | style fidelity + aspect-ratio handling |
| T7 | Extend/chain to 15-20s | any | long-clip workflow |

## Scoring (1-5 each), weighted for owner priorities
consistency x3, motion quality x3, style fidelity to owner's PNG references x2, controllability x1, audio x1, artifacts x1.
Tests T3 (consistency) and T2/T8 below carry the most weight.
Also record: credits consumed, wall-clock time, resolution delivered, license/commercial terms.

## Record format (`results/<model>__<test-id>.md`)
```
model, plan/tier, date, prompt (verbatim), settings, scores, credits_used, notes, output_link
```

## Decision rule
Generate all scored outputs on the paid tier with commercial rights (a watermark-free export is not automatically a licence; free-tier outputs may stay watermarked). Pick the cheapest plan (or 2-plan combo) under $100/mo that scores >=4 on the owner's ranked must-haves. If none exists, report the trade-off and the cheapest upgrade path.

## v3 revisions (priority use cases)
- Run ALL tests at 9:16. Test durations: 3-6s (app entry) and 5-10s (story). Drop T7 (long chaining) to optional.
- Pass/fail gate before scoring: **brand fidelity**. Compare each output frame-by-frame against the approved keyframe/style PNG (palette, linework, texture, proportions, no added elements). Fail = model is out, regardless of other scores.
- New test T9 (money test): take one real app-entry brief (3-6s) and one story brief (5-10s); start frame = approved still, optional end frame; 5 generations each; record how many are usable without rework (usable-take rate). Cost per usable second = credits spent / usable seconds.
- Record take-to-usable ratio; it drives real monthly cost more than list price.
