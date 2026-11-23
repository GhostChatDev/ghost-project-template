# Design catalog

All entries are optional. Licences were read from the public repositories on 22 November 2026; recheck before reuse. Entries already in `references/motion-stack/CATALOG.md` (Excalidraw, Rough.js, Magic UI, ui-ux-pro-max, Impeccable) are listed there and not repeated, except where this kit uses them differently.

## Read, do not vendor (design rules for coding agents)

| Name and GitHub URL | Licence | What to take | Install? |
|---|---|---|---|
| [DESIGN.md format](https://github.com/google-labs-code/design.md) (Google) | Apache-2.0 | The file format used by `DESIGN.template.md`: YAML tokens plus prose sections. Its CLI lints tokens and contrast. | No. `npx @google/design.md lint DESIGN.md` only as a check. |
| [frontend-design skill](https://github.com/anthropics/skills/tree/main/skills/frontend-design) (Anthropic) | Apache-2.0 (licence file in that folder) | Plan the palette, type and layout before code; spend boldness in one place; copy that names the action. | No. |
| [Impeccable](https://github.com/pbakaus/impeccable) | Apache-2.0, with a NOTICE file | Review vocabulary, the quality floor, iOS and Android notes, hardening tests (long names, RTL, slow network). Reusing its text means carrying its NOTICE. | No. Its CLI downloads a binary and fetches from its own site. |
| [Hallmark](https://github.com/Nutlope/hallmark) | MIT | The most concrete checklist of generated-page tells, and per-state control rules. Aimed at marketing pages. | No. Its scripts need Node and Chrome; its image generator calls a paid API. |
| [ui-ux-pro-max](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | MIT | Its plain-text rule lists (quick reference, mobile rules). Its style and palette picks live in CSV files behind a Python script. | No. |
| [Astryx](https://github.com/meta/astryx) (Meta) | MIT | An open design system built to be read by agents; useful as a reference for component states and tokens. | Only if `PRODUCT.md` adopts it. |
| [stitch-skills](https://github.com/google-labs-code/stitch-skills) (Google) | Apache-2.0 | Skills for Google's Stitch service. | No. They need the Stitch MCP server. |

## Install only when the project asks

| Name and GitHub URL | Licence | Use for | Notes |
|---|---|---|---|
| [Lucide](https://github.com/lucide-icons/lucide) | ISC | One consistent icon family. | Keep its licence notice. Copy only the icons used, or use its package. |
| [Tailwind CSS](https://github.com/tailwindlabs/tailwindcss) | MIT | Styling web apps from the `DESIGN.md` tokens. | Map tokens into its theme; don't use its default palette as the design. |
| [shadcn/ui](https://github.com/shadcn-ui/ui) | MIT | Accessible React components that live in the project's own code. | React projects only. Restyle to `DESIGN.md`. |
| [Leonardo](https://github.com/adobe/leonardo) (Adobe) | Apache-2.0 | Generating color scales that meet a target contrast ratio. | A design-time tool; the result goes into `DESIGN.md` tokens. |
| [WebGL Fluid Simulation](https://github.com/PavelDoGreat/WebGL-Fluid-Simulation) | MIT | One fluid or smoke effect, when the design asks for it. | Last updated 2024. Needs WebGL; show the plain screen if it can't start. |
| [rembg](https://github.com/danielgatis/rembg) | MIT | Removing image backgrounds, server side or as a one-off asset step. | Python with large model files; never inside a browser or phone app. |

## Know the terms before using

| Name and GitHub URL | Licence | Why |
|---|---|---|
| [tldraw](https://github.com/tldraw/tldraw) | tldraw's own licence | Production use needs a licence from tldraw. Fine to read; don't ship it in a product without one. |
| [Figma Context MCP](https://github.com/GLips/Figma-Context-MCP) | MIT | Lets an agent read Figma files, but needs the person's own Figma access token and an MCP-capable agent. Not available in Ghost Code's sandbox. |
