# Project Template

A documentation-only starting point for apps and games. Each project defines its own audience, behavior, and visual direction; this repository does not prescribe a theme.

## Use this repository as a template

1. On the repository's GitHub page, choose **Use this template**, then **Create a new repository**.
2. Clone the new repository to your computer.
3. In its root, copy the two project templates:

   ```sh
   cp PRODUCT.template.md PRODUCT.md
   cp DESIGN.template.md DESIGN.md
   ```

4. Fill in both files for the project before implementing a screen or game system.
5. Keep `AGENTS.md` at the root so future contributors and coding agents follow the shared workflow.
6. Keep `PRODUCT.md` and `DESIGN.md` updated when project decisions change. Revise or remove template prompts that do not apply.

No feature code, dependency manifest, or application workflow is included.

## Optional motion references

The `references/motion-stack/` directory is a documentation-only reading list for apps, games, 3D scenes, and video. It is based on the [Fable 5.2 Motion Playbook](https://www.ai.joaoqueiros.com/blog/fable-5-2-motion-playbook-flxrnc-prompts-15-repos).

These entries are **optional references**, not included tools. Nothing here installs a dependency, runs external code, or requires an agent to use a library.

Before using a reference:

1. Read the project's `PRODUCT.md` and `DESIGN.md`, and choose a technique only when it serves those decisions.
2. Read `references/motion-stack/README.md`, then open the linked repository and inspect its current documentation, examples, release status, and license.
3. Verify platform compatibility and any asset, trademark, or platform terms at the time of use.
4. Apply the simplest suitable technique to one screen or game system, then check its relevant states, sizes, inputs, and accessibility settings.

Reference directory:

- `CATALOG.md`: fifteen repositories with links, roles, platform fit, prompting starters, cautions, and license notes.
- `skills/`: three opt-in instruction skills, each in a folder containing `SKILL.md`.
- `forms/`: five briefs for recording constraints before implementation.
- `lessons/lessons.md`: project-specific lessons added after observed results.

Do not clone these repositories into this template, add package manifests or lockfiles for them, or vendor their source or assets without confirming the project's requirements and the source's license. Project documents always take priority over a reference.

---
<img src="https://ghostchat.tech/icons/ghost-code-dev.png" width="20" height="20" alt="" align="top"> Built by [Ghost Code Dev](https://ghostchat.tech)