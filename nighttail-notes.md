# Nighttail Motion Study Notes

The post is Florence’s list of 18 design and motion repos. The supplied study reads the skill files that actually decide timing, color, and what counts as slop, then builds one page that follows them.

- **Feeling:** copper ink settling on paper.
- **3D:** no. The motion is CSS, SVG, and one canvas. No three.js.
- **System:** one custom system, not shadcn. shadcn would fight the brief. Hallmark’s floor plus frontend-design’s “one idea” rule won.
- **Assumptions:** the page is a study of those skills, for Bernard. The one action is “copy the motion brief.” No invented metrics. Ghost Chat stays out of the copy.

Open `nighttail-motion.html`, drag across the ink field, and try the four states.

## What the post actually is

Florence (@flxrnc), 20 Nov 2026, 77.7K views: 18 GitHub repos, ordered style, then layout, then color, then sketch, then motion.

| Step | Repo | What was taken |
|---|---|---|
| Style | ui-ux-pro-max | 44px targets, 4.5:1 text, one duration per job |
| Style | frontend-design | One moment. No fade-up kit. No italic word in a headline |
| Style | Impeccable | Motion explains state. Hover moves a child, not the hit area |
| Style | Hallmark | Tokens only. No tracked labels, no invented numbers, no arrow on a link |
| Layout | DESIGN.md | Named tokens plus the reason, so the next screen cannot drift |
| Layout | Astryx, stitch, Figma MCP, shadcn, Tailwind | Agent tooling. Not used in a single HTML file |
| Color | Leonardo | Contrast first, then the hue |
| Sketch | Excalidraw, tldraw, Rough.js | Left out. A hand-drawn frame would fight the ink |
| Motion | Magic UI | Border-beam and marquee are decoration. Skipped |
| Motion | Lucide | No icon row. The states are the pictures |
| Motion | WebGL Fluid | Smoke that answers the pointer, stopped off-screen |
| Cutout | rembg | Needs a photo. There is no photo |

## Motion thesis

Premium, from the LottieFiles skill: 350–600ms for authored moves, no bounce as a reflex, one signature curve. Impeccable’s arrive curve is `cubic-bezier(0.16, 1, 0.3, 1)`. Press is 140ms, arrive 280ms, draw 420ms, settle 320ms. Exit is faster than enter.

## Contrast, measured

- Ink on paper: 15.0:1.
- Muted on paper: 5.1:1.
- Paper on deep copper: 8.1:1.
- Copper `#9A3E24` on paper is 5.8:1, so it can be a large mark, not body text.
- Muted on the wash is 4.5:1, so captions stay on paper.

## What was not done

The 18 repos were not installed. stitch, Figma MCP, Astryx, and rembg need a project, a file, or a photo. The fluid here is a small wake shader in the spirit of PavelDoGreat’s simulation, not a port of it.
