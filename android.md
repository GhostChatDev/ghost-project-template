# Android platform brief

Fill this form for an Android project. Use the versions and architecture already in the project unless a requirement justifies a change.

## Audience and purpose
- Who is it for?
- What user problem or outcome defines success?
- What must not change?

## Runtime and delivery
- App or library; minimum and target Android/API levels:
- Phone, tablet, foldable, TV, or other form factors:
- Existing Gradle wrapper, modules, language, and UI architecture:
- Required permissions, features, services, and hardware capabilities:
- Storage, networking, accounts, privacy, and approved dependencies:
- Build, unit-test, and device-test commands:

## First screen
- Primary user action and observable result:
- Navigation, system back, and process-restoration behavior:
- Required loading, empty, error, offline, permission-denied, and success states:
- Rotation, resizing, backgrounding, interruption, and persistence expectations:

## Devices and accessibility
- Target screen sizes, densities, orientations, insets, and window modes:
- Touch targets, font scaling, TalkBack, focus, keyboard or controller support:
- Contrast, reduced animation, haptics, audio, and non-sensory alternatives:

## Acceptance checks
- The wrapper builds the debug variant and runs the relevant unit tests without signing secrets.
- The primary flow works across expected navigation and lifecycle changes.
- Permission denial, process restoration, and connectivity changes are handled where relevant.
- Layout and accessibility work at agreed sizes and font scales.
- Actual emulator/device checks and untested configurations are recorded.
