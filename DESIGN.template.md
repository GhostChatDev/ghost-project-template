---
# Design tokens: exact values any agent can use. Format: Google's DESIGN.md specification
# (https://github.com/google-labs-code/design.md). When you copy this file to DESIGN.md, replace the name,
# uncomment the groups you decide on and fill in real values. Leave a group commented until it is decided;
# don't guess values. Check the result with: npx @google/design.md lint DESIGN.md
name: Project name
# colors:              # roles, not swatches; any CSS color (hex, rgb(), oklch())
#   background: ""
#   surface: ""
#   text: ""
#   text-muted: ""
#   border: ""
#   primary: ""        # the accent: main actions, links, focus
#   on-primary: ""     # text and icons on primary
#   success: ""
#   warning: ""
#   danger: ""
# typography:          # one entry per step of the type scale
#   body-md:
#     fontFamily: ""
#     fontSize: 1rem
#     fontWeight: 400
#     lineHeight: 1.5
#   label-md: {}
#   heading-lg: {}
#   display: {}
# spacing:             # the only spacing steps used
#   xs: 4px
#   sm: 8px
#   md: 16px
#   lg: 24px
#   xl: 40px
# rounded:
#   sm: ""
#   md: ""
# motion:              # in the spec; linter 0.4.0 still warns "not a recognized schema key"
#   feedback:
#     duration: 120ms
#     timingFunction: ease-out
#   state: {}
#   view: {}
# components:          # one entry per component and state, values may reference tokens like "{colors.primary}"
#   button-primary:
#     backgroundColor: "{colors.primary}"
#     textColor: "{colors.on-primary}"
#     rounded: "{rounded.md}"
#   button-primary-pressed: {}
---

# Design direction

Copy this file to `DESIGN.md` at the start of a project. Replace the prompts with decisions suited to this project. This template intentionally does not prescribe a visual style. Sections follow the order of the DESIGN.md specification so other agents and its linter can read them; extra sections (games, review, things that must not change) are kept as they are.

## Overview

- **Design goal:** How should the experience look and feel?
- **References and inspiration:** Which references are useful, and which specific qualities should be borrowed—not copied?
- **Personality:** Is the direction quiet or expressive, dense or spacious, playful or serious, familiar or experimental?
- **Composition:** What layout principles, hierarchy, grid, density, and use of imagery suit the project?
- **Platform conventions:** Which native patterns should be followed, and where may the project deliberately differ?

## Colors

- **Palette and roles:** Define background, surface, text, muted text, border, primary (the accent), success, warning, and danger colors as needed. Put the exact values in the `colors` tokens above and explain each role here.
- **Light and dark appearances:** Which appearances are supported, and how do color roles change between them?
- **Contrast and meaning:** What contrast standards apply? How will meaning remain clear without relying on color alone?
- **Game readability:** If relevant, how are players, hazards, objectives, teams, and interactive objects distinguished?

## Typography

- **Typefaces:** Which typefaces or system stacks are used, and where may their files come from?
- **Type scale:** What sizes, weights, line heights, and letter spacing apply to body text, labels, headings, and numeric displays? Record them in the `typography` tokens.
- **Content behavior:** How should wrapping, truncation, localization, long values, and dynamic type be handled?
- **Icons and illustrations:** What family, weight, level of detail, and usage rules apply?

## Layout

- **Spacing system:** What base unit and spacing steps are used (the `spacing` tokens)? Where are exceptions allowed?
- **Layout measurements:** What content widths, gutters, breakpoints, safe areas, and control sizes apply?

## Shapes

- **Shape language:** What corner radii (the `rounded` tokens), borders, shadows, elevation, and separators are used?

## Motion & Micro-interaction

- **Interaction principles:** How should navigation, selection, input, feedback, and confirmation behave?
- **Motion purpose:** Which movements explain hierarchy, provide feedback, or support game feel? Which are decorative?
- **Timing and easing:** Define useful duration and easing ranges for transitions, feedback, and repeated effects (the `motion` tokens).
- **One feeling in five words:** What single feeling should the motion communicate?
- **One motion idea:** Which single movement should carry that feeling?
- **One clock:** Which clock drives the timing? If BPM is used, state the frame rate too.
- **Named spring damping:** Which spring and damping value are used, and what landing behavior is intended?
- **Pixel sizes:** What pixel sizes must the subject and important elements meet?
- **Seek check:** How will a cold seek to a frame be compared with reaching that frame sequentially?
- **Interruption:** What happens when an action, page change, pause, or app interruption occurs during motion?
- **Reduced motion:** Which system setting is respected? Replace nonessential movement with instant changes, opacity, or other low-motion feedback. Do not remove information, controls, or essential state changes. Avoid forced camera movement, parallax, flashing, and large zooms when reduced motion is enabled.

## Components

- **Components:** Which shared components exist, and what variants does each need? Record their values in the `components` tokens.
- **Component and screen states:** Document relevant default, hover, focus, pressed, selected, disabled, loading, empty, error, and success states.

## Additional guidance for games

Complete this section for games; remove it for non-game projects.

- **Presentation and camera:** What perspective, framing, HUD placement, visual priority, and camera behavior are intended?
- **Gameplay timing:** Specify the timings that affect play: input buffering, cooldowns, animation windows, telegraphs, invulnerability, spawn intervals, round pacing, and any fixed simulation step. Use values appropriate to the game rather than a universal preset.
- **Input and feedback:** How do controls, animation, sound, particles, and haptics confirm actions? Which cues must remain understandable without sound or vibration?
- **Frame-rate independence:** Which movement and timers use elapsed time or a fixed simulation step? Which behaviors must remain consistent across supported frame rates?
- **Pause and interruption:** Which timers and motion stop on pause, focus loss, or interruption, and how does play resume?
- **Reduced motion in gameplay:** Preserve mechanics, timing windows, collision rules, and critical telegraphs. Reduce or replace camera shake, screen flashes, parallax, excessive particles, and nonessential animation without hiding threats or changing difficulty.
- **Accessibility options:** Which separate controls are needed for motion intensity, flashes, camera shake, contrast, text, audio cues, and input?

## Review

- **Target views:** List the screen sizes, orientations, input modes, and platforms that must be reviewed.
- **Review criteria:** How will the team decide whether a screen or game system matches this direction while remaining readable and usable? `references/design-kit/design-floor.md` is the minimum.

## Do's and Don'ts

- **Avoid:** Which styles, effects, layouts, or assets do not fit? If the project wants something `design-floor.md` lists as a sign of a generated look, say so here; this file wins.

## Things that must not change

List approved design decisions that require review before alteration: identity elements, layout principles, gameplay cues, timing rules, accessibility commitments, or reference assets. Keep this list project-specific.
