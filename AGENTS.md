# Shared instructions for future work

These instructions apply to apps and games built from this template. They define a way of working, not a product, technology stack, or visual style.

## Before starting

1. Read `PRODUCT.md` to understand the audience, purpose, platform, and constraints.
2. Read `DESIGN.md` to understand the visual direction and interaction or gameplay rules.
3. If either file is missing, use its corresponding `*.template.md` file to gather the missing decisions before implementation. Do not silently substitute preferences from another project.
4. Treat explicit product and design decisions as constraints. Ask before changing anything listed as must not change.

## Work in small, reviewable slices

- Work on one screen or one game system at a time.
- Finish a coherent slice—including its navigation, feedback, and relevant states—before starting another.
- Keep changes focused on the requested slice. Avoid unrelated redesigns, cleanup, or refactors.
- Reuse existing patterns and components where they fit the current project.
- Do not add dependencies, frameworks, services, assets, or workflows that were not requested. If one seems necessary, explain why and ask first.
- Do not add speculative features or placeholder screens.

## Preserve the project's direction

- Follow `DESIGN.md`; do not impose a default theme, component style, font, color palette, or motion treatment.
- For apps, support the platforms, orientations, input methods, and accessibility needs named in the project documents.
- For games, preserve the intended controls, game feel, timing, readability, and gameplay rules.
- Prefer the simplest implementation that satisfies the current slice and is consistent with the existing codebase.

## Motion stack

Before animating a screen, game, or film, read `references/motion-stack/README.md` and fill the matching brief. Do not install a listed repository unless `PRODUCT.md` asks for it. A screenshot is not proof of motion.


## Design kit

Before designing a screen, read `references/design-kit/README.md`. Put exact values in the tokens at the top of `DESIGN.md` (Google's DESIGN.md format) before writing interface code, and review each finished screen against `references/design-kit/design-floor.md` on the rendered result. Pick icons, styling, chart and data tools only from `references/design-kit/CATALOG.md` `references/design-kit/DATA.md` and `references/design-kit/MOBILE.md`, and only when `PRODUCT.md` asks for them; respect the licence notes there. `DESIGN.md` wins over the design kit.

## Product recipes

Consult a file in `references/product-recipes/` only when `PRODUCT.md` explicitly selects that recipe by name. A recipe does not authorize dependencies, services, or implementation by itself. If `PRODUCT.md` names none, ignore the folder. See `references/product-recipes/README.md`.

## Check the result

Before calling a slice complete, check what is relevant to that slice:

- **States:** loading, empty, populated, error, disabled, success, and partial or interrupted states where applicable.
- **Layout:** the supported phone, tablet, desktop, console, or other target sizes; narrow and wide layouts; long content; and safe areas where applicable.
- **Interaction:** every visible control works; keyboard, pointer, touch, and controller behavior where supported; focus and navigation remain understandable.
- **Games:** gameplay timing, input response, pause/resume, restart, win/loss, and interruption behavior where applicable.
- **Motion:** transitions and animations match the design; reduced-motion behavior is provided where needed.
- **Verification:** run the project's existing relevant build, tests, or preview. Report what was checked and what could not be checked.

Do not mark work complete merely because it builds. Review the resulting screen or play the resulting system when the available tools allow it.

## Handoff

Summarize the completed slice, any assumptions, and the checks performed. Call out unresolved decisions or behavior separately. Stop for review when requested rather than continuing into another screen or system.
