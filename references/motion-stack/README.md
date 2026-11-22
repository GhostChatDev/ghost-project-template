# Motion stack reference

A documentation-only reading list for apps, games, 3D scenes, and video. It is based on the [Fable 5.2 Motion Playbook](https://www.ai.joaoqueiros.com/blog/fable-5-2-motion-playbook-flxrnc-prompts-15-repos).

These entries are **optional references**, not included tools. Nothing here installs a dependency, runs external code, or requires an agent to use a library.

## Before using a reference

1. Read `PRODUCT.md` and `DESIGN.md`; choose the technique from the project's needs.
2. Open the linked repository and inspect its current documentation, examples, and release status.
3. Read its license and any asset, trademark, or platform terms at the time of use.
4. Verify that it supports the chosen platform and can be added without unrelated dependencies.
5. Build one screen or game system first; test its states, sizes, input methods, and accessibility settings.

## Directory

- `CATALOG.md`: fifteen repositories with links, roles, platform fit, prompting starters, cautions, and license notes.
- `skills/`: three opt-in instruction skills. A skill is a folder containing `SKILL.md`; use only one relevant skill for a task, or combine skills when the task spans design, motion, and production.
- `forms/`: five briefs for recording constraints before implementation.
- `lessons/lessons.md`: project-specific lessons added after observed results.

## Keep boundaries clear

- Do not clone these repositories into this template.
- Do not add package manifests, lockfiles, submodules, generated apps, or vendored source.
- Do not treat visual polish as a substitute for product behavior.
- Do not apply one repository's style, timing, or technology to every project.
- Do not assume that a public repository permits every use; check its license each time.

If this reference conflicts with a project's `PRODUCT.md` or `DESIGN.md`, the project documents win.