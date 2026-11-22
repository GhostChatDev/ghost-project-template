# Game platform brief

Fill this form for a game on any engine or runtime. Do not import web-game rules into native games or assume a particular engine.

## Audience and purpose
- Who is the game for, and what is the intended experience?
- What is the core player fantasy and smallest playable objective?
- What must not change?

## Runtime and delivery
- Target platforms, devices, engine/runtime, and existing versions:
- Rendering approach, project structure, and build/test commands:
- Required resolution, aspect ratio, orientation, and performance targets:
- Approved engines, packages, assets, fonts, audio, and their licenses:
- Save data, networking, accounts, privacy, and platform-service constraints:

## First playable system
- One bounded mechanic, scene, or gameplay system:
- Player inputs, observable feedback, success, and failure:
- Entities, rules, resources, and edge cases:
- Required start, pause, resume, game-over, restart, and interrupted states:

## Timing, camera, and accessibility
- Simulation model: fixed, variable, or hybrid timestep:
- Frame pacing, input buffering, cooldowns, animation and transition timing:
- Camera behavior, hit feedback, particles, audio, and intensity limits:
- Reduced-motion options, non-audio/non-color cues, remapping, and text scaling:

## Acceptance checks
- The core loop is playable with every intended input method.
- Rules behave consistently at agreed frame rates and after pause or focus changes.
- Target resolution and performance are measured rather than assumed.
- All essential information has an accessible cue and reduced-motion behavior is checked.
- Assets have suitable provenance; tests and actual play checks are recorded.
