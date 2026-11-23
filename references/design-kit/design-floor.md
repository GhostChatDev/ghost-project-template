---
name: design-floor
description: The minimum a screen or game menu must meet before it is handed back. Checked on the rendered result.
---

# Design floor

`DESIGN.md` and the person's own words win over every line here. If `DESIGN.md` asks for something this file warns against, do what `DESIGN.md` says.

## Tokens, not one-off values

- Every color, font, size, spacing step, radius and duration comes from the tokens in `DESIGN.md`. No raw hex values or stray pixel sizes inside components.
- Colors are roles (background, surface, text, muted text, border, accent, success, warning, danger), not a list of swatches.
- Dark mode, if supported, is designed with its own tones and checked on its own. It is not an inverted light mode.

## Readable

- Text contrast at least 4.5:1; large text, icons, control edges and focus rings at least 3:1. Meaning never relies on color alone.
- Body text at least 16px on the web (the platform's default size on iOS and Android, with Dynamic Type or sp units). Lines about 45 to 75 characters.
- One or two type families. A type scale with named steps in `DESIGN.md`; no sizes outside it.
- Spacing on a 4-based scale. More space above a heading than below it.

## Every control and every data area has its states

- Controls: default, hover (only where hover exists), focus-visible, pressed, disabled, loading, and error or success where it applies. Pressed feedback is immediate and doesn't move the layout.
- Data areas: loading, empty (with the action that fills it), error (with the cause and a way to recover) and full.
- Destructive actions are confirmed or can be undone.

## Usable everywhere it ships

- Touch targets at least 44×44pt on iOS, 48×48dp on Android, and at least 24×24px for a pointer on the web.
- Keyboard: visible focus ring, tab order matches what you see.
- No horizontal scroll from 320px up; respect safe areas; never disable zoom.
- Review at the sizes `DESIGN.md` lists; if it lists none, 390px and 1280px wide for the web.

## Motion with a purpose

- Animate transform and opacity, not width, height or position.
- One deliberate motion moment per screen rather than every section fading in. Exits are quicker than entries.
- Animations can be interrupted, never block input, and have a reduced-motion version that keeps the feedback.

## Honest content

- No invented numbers, testimonials, customer logos or reviews. No success message for a form that isn't connected.
- Buttons say what happens ("Save changes", not "Submit"). One name per action everywhere. Errors say the cause and the fix.
- Real material: the product's own screens, the person's images, or credited images with a licence that allows the use.

## Signs of a generated look (avoid unless `DESIGN.md` asks for them)

- A small all-caps label above every heading.
- One italic or colored word inside a heading.
- A big-number hero with a small label and a gradient accent.
- 01 / 02 / 03 markers on content that isn't a sequence.
- A grid of identical cards, or a card inside a card.
- Gradient text, decorative glass or glow blobs, purple-to-blue gradients.
- Monospace used as decoration rather than for code or data.
- Emoji or unicode symbols as icons. Use one icon family with one stroke width.
- Middle-dot meta strings and arrows glued to link text.

## Apps on iOS and Android

- Prefer the platform's own controls and navigation (a tab bar for two to five sections; system back always works).
- Use the system's semantic colors and text styles where `DESIGN.md` doesn't say otherwise.
- On tablets, restructure the layout instead of stretching the phone one.

## Games

- The HUD never covers the player, hazards or objectives, and stays readable at the smallest supported screen.
- Every action confirms itself through more than one cue (animation and sound, or animation and haptics), and the game stays understandable with sound off.
- Menus work with every input the game supports (touch, keyboard, controller), with a visible focus.
- Pause stops gameplay timers; options include motion intensity, flashes and camera shake.

## How to review

Look at the rendered screen, at each listed size, in each supported appearance. Fix what fails, at most three rounds, then report what was checked and what could not be.
