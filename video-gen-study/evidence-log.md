# Evidence Log: what real users report
Rule: every claim gets a tier. A = independent hands-on with shown outputs/workflow; B = creator anecdote; C = vendor/affiliate/promotional; R = research paper.
Captured 2026-10-23. Access limits: X pages and most sites could not be opened directly from this environment (only search snippets); Reddit blocks the crawler; LinkedIn search returned nothing relevant. So X/LinkedIn evidence below is thin and must be supplemented by the owner's own feed review (see "Owner help needed").

## Workflow patterns that recur
1. Locked start frame + end frame, then interpolate (B, X creator): build a strong first frame in an image model, generate an end frame, animate between. Reported control over composition, camera angle, motion direction, continuity. Seedance used for dynamic motion, Kling for camera refinement.
2. Short image-to-video prompts (B, Medium): ~50-80 words, motion only; long prompts erode the reference and let text override the image. Add "preserve composition and colors".
3. Use a style-anchor image; simplify background / lower contrast in the anchor if tone shifts (B).
4. Fix drifting shots one at a time instead of regenerating everything (B).
5. Runway's own flow: style frame in Runway -> animation elsewhere -> final render (C, vendor post).

## Style fidelity (matters most for exact brand)
- R: 2026 stylization paper: Seedance 2.0 struggles with high-frequency stylistic detail (oil/ink styles) and style decoupling between subject/background. Kling-O1 scored higher on style similarity (0.815 vs 0.792); Seedance higher on content preservation (0.889 vs 0.833). Kling-O1 weak on complex scenes.
- C: Seedance developer benchmark rates Seedance 2.0 top, source-image preservation 3.31 vs Kling 3.0 3.18. Authors are the vendor.
- GAP: no independent test found of exact brand-style preservation for flat/illustrated styles. This must be tested by the owner on real brand assets.

## Platform experience
- B/C: Higgsfield credit burn (60-90 credits per cinematic generation; 42% of monthly credits in 3 days on Ultra), "unlimited" is metered, expiring credits, billing complaints. Praised for camera control and multi-model access.
- C: Runway added Seedance 2.0 (Unlimited/Enterprise), Kling 3.0 Pro, Veo 3.1, Aleph 2.0.

## Legitimacy check on sources
Most "best AI video generator" posts are SEO/affiliate/vendor-run; a number of X posts are paid promos (#ad). Not usable as proof. Only tier A/B/R items should drive the decision.

## Owner help needed (X/LinkedIn)
Please share 5-10 posts/threads you trust (links or screenshots) showing outputs + workflow for brand-consistent vertical video. Prefer posts with: the tool/plan used, the input still, the final clip, and number of attempts.
