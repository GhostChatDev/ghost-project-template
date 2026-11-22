---
name: motion-qa
description: Verify animation with frames and seeks rather than still screenshots.
---

# Motion QA

- Stills cannot prove motion.
- Check subject width in pixels against the brief.
- Two consecutive frames must differ unless the brief named a hold.
- Seek check: draw frame N cold and after frame N−1. They must match. Use no `Date.now()`, unseeded `Math.random()`, infinite repeats, or timers that cannot seek.
- FFmpeg `freezedetect` is a clue, not the verdict. Play the loop seam.
- The pass that wrote the animation must not grade its own shot.
- Stop after three failed looks. Do not restyle the whole project.
- Record each lesson in `references/motion-stack/LESSONS.md` as:

  Lesson: …
  Rule: …
  Applies to: web | game | both
