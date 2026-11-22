---
name: screen-review
description: Review one implemented screen or game system against its brief. Use after implementation and before calling work finished, especially for responsive, accessibility, motion, and state checks.
---

# Screen and system review

Review the actual result, not just a successful build. Limit the pass to the current screen or game system and the files it depends on.

## Process

1. Re-read the relevant requirements in `PRODUCT.md`, `DESIGN.md`, and the selected platform brief.
2. Run the project's existing build and tests. Inspect the rendered screen or running system when tooling allows it.
3. Exercise every visible control and the primary flow. Check keyboard, controller, pointer, or touch input where supported.
4. Inspect relevant loading, empty, error, disabled, success, paused, and resumed states. Do not manufacture states the product does not need.
5. Check the agreed screen, device, viewport, orientation, and output sizes. Look for clipping, sideways scrolling, unreadable text, unreachable controls, and unsafe-area conflicts.
6. Check contrast, labels, focus, text scaling, reduced motion, and non-audio cues as relevant to the platform.
7. For games, also inspect frame pacing, input latency, scene transitions, pause/resume, and behavior after interruption or lost focus. Do not require a browser game technique in a native project.
8. Report concrete failures with reproduction steps, fix root causes, and rerun the affected checks. Do not remove or weaken a test to obtain a pass.

## Completion checks

- Every acceptance criterion is marked verified or explicitly not checked.
- Visual claims are backed by actual rendered inspection.
- Remaining limitations name the device, state, or tooling that prevented verification.
- One useful project-specific lesson can be appended to `lessons/lessons.md` without imposing a universal style.
