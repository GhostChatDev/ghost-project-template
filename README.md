# Project Template

A documentation-only starting point for future apps and games. It helps each project define its own product and design direction without prescribing a technology stack, feature set, dependency, or visual style.

## Included files

- `AGENTS.md` — shared working instructions for future implementation.
- `PRODUCT.template.md` — prompts for the audience, purpose, platform, scope, and fixed constraints.
- `DESIGN.template.md` — prompts for visual direction, color, typography, spacing, interaction, and motion, including game-specific timing and reduced motion.
- `LICENSE` — the repository license.

## Use this repository as a template

### On GitHub

1. Open this repository and choose **Use this template**, then **Create a new repository**.
2. Name the new repository and create it.
3. Clone the new repository to your computer.
4. In its root folder, copy the templates to their project-specific names:

   ```sh
   cp PRODUCT.template.md PRODUCT.md
   cp DESIGN.template.md DESIGN.md
   ```

   On Windows PowerShell, use:

   ```powershell
   Copy-Item PRODUCT.template.md PRODUCT.md
   Copy-Item DESIGN.template.md DESIGN.md
   ```

5. Replace the prompts in `PRODUCT.md` and `DESIGN.md` with decisions for the new project.
6. Keep `AGENTS.md` at the root so future work reads the shared instructions.

If GitHub's template option is unavailable, create a new repository and copy these files into it instead.

### In an existing project

Copy `AGENTS.md`, `PRODUCT.template.md`, and `DESIGN.template.md` into the project root, then create `PRODUCT.md` and `DESIGN.md` as above. Review existing project conventions before replacing or merging any files with the same names.

## Start a screen or game system

Before implementation, make sure `PRODUCT.md` and `DESIGN.md` contain enough detail to guide the work. Then request one screen or game system at a time. Future work should follow `AGENTS.md`, avoid unrequested additions, and check the states, layouts, inputs, and target sizes relevant to that slice.

The `*.template.md` files are reusable prompts. Keep them unchanged for future projects; record project decisions in the copied `PRODUCT.md` and `DESIGN.md` files.

---
<img src="https://ghostchat.tech/icons/ghost-code-dev.png" width="20" height="20" alt="" align="top"> Built by [Ghost Code Dev](https://ghostchat.tech)
