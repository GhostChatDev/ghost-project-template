# Fifteen-repository catalog

Use this catalog to choose a reference, not to prescribe a stack. The prompt starters are starting points for a project-specific brief, not instructions to reproduce another product. License notes are observations, not legal advice; follow the linked repository's current terms.

## Interface sketching and illustration

### 1. Excalidraw

- **Repository:** [excalidraw/excalidraw](https://github.com/excalidraw/excalidraw)
- **Role:** Collaborative virtual whiteboard with a hand-drawn feel; useful for sketching flows and interface studies.
- **Platform fit:** Web-first. Treat embedding, mobile behavior, persistence, and collaboration as separate integration decisions.
- **Prompt starter:** "Sketch this screen's hierarchy and interaction states as a low-fidelity diagram before choosing production components."
- **Cautions:** Do not make the final product look hand-drawn unless `DESIGN.md` asks for it. An embedded whiteboard is a substantial dependency, not a drawing icon.
- **License note:** The root `LICENSE` read during research states MIT. Recheck before reuse, including fonts and other assets.

### 2. Rough.js

- **Repository:** [rough-stuff/rough](https://github.com/rough-stuff/rough)
- **Role:** Generates sketchy, hand-drawn-style vector graphics; useful for diagrams, illustration, and deliberately informal rendering.
- **Platform fit:** JavaScript environments with Canvas or SVG. A native app needs an explicit bridge or a different rendering choice.
- **Prompt starter:** "Use irregular vector strokes only for the specified illustration layer, while keeping labels and controls crisp and readable."
- **Cautions:** Check visual noise, contrast, rendering cost, and whether random-looking output remains stable enough for snapshots and accessibility.
- **License note:** The root `LICENSE` read during research states MIT. Recheck before reuse.

## Programmatic and educational motion

### 3. Manim Community

- **Repository:** [ManimCommunity/manim](https://github.com/ManimCommunity/manim)
- **Role:** A community-maintained Python framework for programmatic mathematical and explanatory animations.
- **Platform fit:** Python content-production workflows that render media for later playback; not a drop-in browser, iOS, or Android UI animation library.
- **Prompt starter:** "Storyboard one explanation as timed visual beats, then define the narration, equations, transitions, and final video format."
- **Cautions:** Budget for scene rendering and media storage. Keep source scenes, generated video, and app runtime responsibilities separate.
- **License note:** The root `LICENSE` read during research states MIT. Check third-party media and font terms too.

### 4. Huashu Motion

- **Repository:** [alchaincyf/huashu-motion](https://github.com/alchaincyf/huashu-motion)
- **Role:** Motion-design guidance and examples to study when planning expressive interface movement.
- **Platform fit:** Use as a design and implementation reference; confirm the actual language and runtime in the repository before targeting web or native UI.
- **Prompt starter:** "Define the purpose, trigger, duration, easing, interruption behavior, and reduced-motion alternative for each movement."
- **Cautions:** Do not copy effects without checking their context, performance, input model, and relevance to the current design.
- **License note:** The root `LICENSE` read during research states MIT. Recheck before copying examples or assets.

### 12. GSAP

- **Repository:** [greensock/GSAP](https://github.com/greensock/GSAP)
- **Role:** JavaScript animation tooling for timelines, UI motion, and scroll-linked sequences.
- **Platform fit:** Browser and JavaScript-driven interfaces. Native mobile use requires an appropriate web layer or a native alternative.
- **Prompt starter:** "Create one interruptible timeline for this component, with explicit initial, active, exit, and reduced-motion states."
- **Cautions:** Avoid scroll hijacking, motion without a user benefit, and animations that block input. Check plugin-specific terms as well as the core terms.
- **License note:** GitHub's license endpoint returned 404 during research; the root listing includes `README.md` but no root license file. Read the current license information in the repository before use and check individual plugins.

## Interface design and web motion guidance

### 5. Magic UI

- **Repository:** [magicuidesign/magicui](https://github.com/magicuidesign/magicui)
- **Role:** Animated interface components and effects for web projects; useful for studying component-level motion patterns.
- **Platform fit:** Web projects whose existing framework and styling approach match the component's current requirements.
- **Prompt starter:** "Evaluate one effect against this screen's content and design tokens; implement only the needed behavior and states."
- **Cautions:** Do not import a whole component collection for one effect. Check framework compatibility, accessibility, bundle impact, and reduced-motion behavior.
- **License note:** The root `LICENSE.md` read during research states MIT. Component examples may involve additional assets or dependencies.

### 6. UI UX Pro Max Skill

- **Repository:** [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill)
- **Role:** Agent-oriented UI/UX guidance for turning product requirements into structured design decisions.
- **Platform fit:** Cross-platform planning and review. Apply only guidance relevant to the target platform and existing project constraints.
- **Prompt starter:** "Review this brief for hierarchy, interaction states, accessibility, responsive behavior, and platform conventions before implementation."
- **Cautions:** A design checklist does not replace user research, platform guidelines, or testing the real interface.
- **License note:** The root `LICENSE` URL checked during research returned 404. No reuse permission is inferred; inspect the current repository terms before copying content.

### 7. Taste Skill

- **Repository:** [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill)
- **Role:** Design-review guidance for visual hierarchy, composition, interface detail, and motion choices.
- **Platform fit:** Primarily useful for web interface direction and critique; adapt any suggestions to native platform conventions.
- **Prompt starter:** "Critique the current screen against its own brief and identify specific hierarchy, spacing, readability, and motion issues."
- **Cautions:** Do not let generic 'taste' rules override the project's visual direction, evidence from users, or accessibility needs.
- **License note:** The root `LICENSE` read during research states MIT. Recheck before reproducing instruction text.

### 8. Impeccable

- **Repository:** [pbakaus/impeccable](https://github.com/pbakaus/impeccable)
- **Role:** Interface-quality guidance focused on making digital products clearer and more polished.
- **Platform fit:** Use for design critique and implementation review, especially on the web; confirm the repository's current supported environments.
- **Prompt starter:** "Find concrete usability and finish problems in this implemented screen, then propose the smallest changes that address them."
- **Cautions:** Polish should follow working behavior, not conceal missing states or introduce an unrelated visual system.
- **License note:** A root license was located during research. Read the current `LICENSE` before reuse rather than relying on this summary for its terms.
## 3D scenes and spatial interaction

### 9. Three.js

- **Repository:** [mrdoob/three.js](https://github.com/mrdoob/three.js)
- **Role:** WebGL-based 3D rendering for scenes, models, cameras, lighting, and interactive spatial experiences.
- **Platform fit:** Web and web views. Native iOS or Android projects should evaluate web embedding versus native 3D frameworks explicitly.
- **Prompt starter:** "Define the scene's camera, interaction, loading state, fallback, performance budget, and mobile controls before adding visual effects."
- **Cautions:** Large models and effects can hurt startup time, thermals, battery, and accessibility. Provide useful fallback content and test touch input.
- **License note:** The root `LICENSE` read during research states MIT. Models, textures, and example assets can have separate terms.

### 10. MCP for Blender

- **Repository:** [ahujasid/mcp-for-blender](https://github.com/ahujasid/mcp-for-blender)
- **Role:** Connects Blender with MCP-compatible tools for assisted 3D scene creation and editing.
- **Platform fit:** Desktop content production with Blender; output assets can target web, mobile, games, or video after platform-specific optimization.
- **Prompt starter:** "Build a small editable scene with named objects, a documented camera, export settings, and a target polygon and texture budget."
- **Cautions:** Review generated scenes before running further actions. Keep source assets and exports reproducible; do not grant unnecessary file or network access.
- **License note:** The root `LICENSE` read during research states MIT. Connected services and Blender assets have their own terms.

## Video composition and post-production

### 12. Hyperframes

- **Repository:** [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes)
- **Role:** A video-generation and editing reference to investigate for programmatic motion content and compositing workflows.
- **Platform fit:** Content-production pipelines. Confirm supported runtimes, rendering environment, and export formats before integration.
- **Prompt starter:** "Define a short video composition from explicit scenes, timing, assets, captions, audio, and output constraints."
- **Cautions:** Do not assume browser playback, native rendering, or a particular AI capability without checking the current project. Media generation may incur external costs.
- **License note:** The root `LICENSE` read during research states MIT. Inputs, generated media, fonts, and external services can have separate terms.

### 11. Remotion

- **Repository:** [remotion-dev/remotion](https://github.com/remotion-dev/remotion)
- **Role:** Creates videos programmatically with React components and web rendering techniques.
- **Platform fit:** Web/React-based authoring and server or desktop rendering workflows, depending on the selected Remotion components.
- **Prompt starter:** "Express this video as deterministic scenes with a fixed frame rate, dimensions, duration, assets, and render command."
- **Cautions:** Separate interactive previews from final rendering. Test long renders, missing assets, fonts, audio sync, and resource usage.
- **License note:** The root `LICENSE.md` describes Remotion's license terms, including conditions that may require a company license. Read the full current terms before commercial use.

### 13. Remotion Skills

- **Repository:** [remotion-dev/skills](https://github.com/remotion-dev/skills)
- **Role:** Agent instructions and supporting material for working with Remotion video projects.
- **Platform fit:** Development and content-production workflows that already use or are evaluating Remotion.
- **Prompt starter:** "Use the relevant Remotion guidance to inspect this composition's timing, assets, rendering setup, and failure states."
- **Cautions:** These instructions do not themselves provide a renderer. Keep the Remotion version and guidance aligned; avoid installing unrelated tooling.
- **License note:** GitHub's license endpoint returned 404 during research, and the root listing showed no license file. Inspect current repository terms before copying or redistributing content.

### 14. FFmpeg

- **Repository:** [FFmpeg/FFmpeg](https://github.com/FFmpeg/FFmpeg)
- **Role:** Command-line tools and libraries for recording, converting, inspecting, and streaming audio and video.
- **Platform fit:** Cross-platform media tooling, typically used in a controlled production or server environment rather than embedded casually in a UI.
- **Prompt starter:** "Define the source, target codec and container, dimensions, frame rate, audio behavior, metadata, and validation for this media conversion."
- **Cautions:** Pin and document commands, handle failures and large files safely, and do not pass untrusted input to a shell. Distribution and codec patent obligations need review.
- **License note:** The root `LICENSE.md` says most files are LGPL v2.1 or later, some files use other licenses, and optional GPL parts change the combination's terms. Review the exact build configuration.

## Selection order

1. Start with product behavior and platform constraints.
2. Choose the smallest relevant technique: CSS or native motion may be enough.
3. Use a reference to answer a specific question, then test the implementation on the target devices.
4. Record useful project-specific findings in `lessons/lessons.md` without turning one result into a universal style rule.
