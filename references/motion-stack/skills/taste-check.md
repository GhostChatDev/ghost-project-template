---
name: taste-check
description: Review one implemented screen against the project design and responsive states.
---

# Taste check

- Use the one visual system named in `DESIGN.md`; do not invent a second style.
- Use one section per screen.
- Phone first. Text must fit at 390 px wide.
- Use type sizes only if `DESIGN.md` named them. If it did not, ask; do not silently use 14 / 20 / 32.
- Space only in the steps `DESIGN.md` named.
- Use paper, ink, and one accent only if `DESIGN.md` says so.
- Every screen needs loading, empty, and error states.
- Every button needs hover, pressed, and disabled states.
- Use WebGL only if the user asked for 3D. Use one region, HTML text over the canvas, never painted in the scene. Cap pixel ratio at 1.5 on a phone and 2 on desktop. On unmount, stop the loop and dispose geometries, materials, textures, and the renderer.
- If WebGL cannot start, show the HTML screen, not a blank page.
- Review widths: 1440, 1024, 768, and 390 px.
- Use at most three fix rounds.
