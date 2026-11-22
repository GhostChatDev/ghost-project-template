# iOS platform brief

Fill this form for an iOS or iPadOS project. Keep platform-native alternatives in the comparison before adding packages.

## Audience and purpose
- Who is it for?
- What user problem or outcome defines success?
- What must not change?

## Runtime and delivery
- App or library; minimum iOS/iPadOS version:
- iPhone, iPad, or both; supported orientations:
- Existing Xcode project, package, shared scheme, and build command:
- Language and UI architecture already in use:
- Required capabilities, permissions, background modes, and usage strings:
- Storage, networking, accounts, privacy, and approved dependencies:

## First screen
- Primary user action and observable result:
- Navigation structure and expected back behavior:
- Required loading, empty, error, offline, permission-denied, and success states:
- Interruption, backgrounding, restoration, and data-persistence expectations:

## Devices and accessibility
- Target device sizes and safe-area requirements:
- Dynamic Type, VoiceOver, keyboard or controller support as relevant:
- Touch targets, contrast, Reduce Motion, and other accessibility settings:
- Motion, haptics, audio, and non-sensory alternatives:

## Acceptance checks
- The shared scheme builds for the generic iOS Simulator without signing.
- The primary flow works with intended inputs and survives expected lifecycle changes.
- Layout remains usable at agreed sizes and text scales.
- Permission requests occur only in context and denial has a usable path.
- Relevant tests and UI checks pass; untested devices or states are named.
