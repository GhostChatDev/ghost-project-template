# Mobile kit

Skills and tools for iPhone and Android apps. All optional. Licences were read from the public repositories on 23 November 2026; recheck before reuse.

Ghost Code builds iPhone apps in SwiftUI (iOS 17 by default, built on GitHub's Macs or the owner's own Mac) and Android apps in Kotlin with Jetpack Compose (built on GitHub's Linux machines). Its own rules for both already draw on the first two entries below.

## Native apps: read these

| Name and GitHub URL | Licence | What to take |
|---|---|---|
| [SwiftUI Pro](https://github.com/twostraws/SwiftUI-Agent-Skill) (Paul Hudson) | MIT | Modern SwiftUI: `@Observable`, `NavigationStack`, current modifiers, accessibility, performance. It assumes iOS 26 or 27; keep this project's deployment target and put newer APIs behind `#available`. |
| [Android skills](https://github.com/android/skills) (Google, official) | Apache-2.0 | AGP 9 and Gradle, edge-to-edge, runtime permissions, Compose performance, testing setup, Navigation 3. Pick one toolchain line and keep it. |

## Other ways to build apps (only if `PRODUCT.md` chooses them)

| Name and GitHub URL | Licence | For |
|---|---|---|
| [Expo skills](https://github.com/expo/skills) | MIT | Apps built with Expo (React Native). |
| [React Native skills](https://github.com/callstackincubator/agent-skills) (Callstack) | MIT | React Native apps. |
| [Flutter agent plugins](https://github.com/flutter/agent-plugins) | BSD-3-Clause | Flutter apps. |
| [Software Mansion skills](https://github.com/software-mansion-labs/skills) | No licence file found | Animation ideas for React Native only. With no licence, read for ideas; don't copy its text. |

## Testing and running apps

| Name and GitHub URL | Licence | Notes |
|---|---|---|
| [Maestro](https://github.com/mobile-dev-inc/maestro) | Apache-2.0 | End-to-end tap tests written as simple flows. Runs Android tests on Linux CI and iOS tests on a Mac. |
| [Mobile MCP](https://github.com/mobile-next/mobile-mcp) | Apache-2.0 | Lets an agent drive an iOS Simulator or Android emulator. Needs a Mac or an emulator next to the agent; not available in Ghost Code's cloud sandbox. |
| [MobileBuildMCP](https://github.com/getsentry/MobileBuildMCP) (Sentry) | MIT | Build-and-run tools for an agent on a Mac. Same limit as Mobile MCP. |

## Shipping

| Name and GitHub URL | Licence | Notes |
|---|---|---|
| [App Store Connect skills](https://github.com/rorkai/app-store-connect-cli-skills) (Rork) | MIT | Automating App Store Connect: TestFlight, metadata, submissions. Needs the owner's Apple Developer account and an App Store Connect API key, which stay with the owner and never go in this repository. |
