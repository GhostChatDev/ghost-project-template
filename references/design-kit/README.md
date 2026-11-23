# Design kit

Optional references for how apps and games built from this template look, read and behave. They sit next to `references/motion-stack/` and follow the same rule: read them, don't install anything unless `PRODUCT.md` asks.

**Pipeline: brief → tokens → one screen → review → next screen.**

1. Read `PRODUCT.md` and `DESIGN.md`. They win over everything in this folder.
2. Fill the tokens at the top of `DESIGN.md` (colors, typography, spacing, rounded, motion, components) before writing interface code. The format is Google's open [DESIGN.md](https://github.com/google-labs-code/design.md) specification, so any agent can read it.
3. Build one screen or one game system.
4. Review it against `design-floor.md`, on the real rendered result at the sizes the project ships at.
5. Pick tools only from `CATALOG.md`, and only when the project needs them. Charts and data tools are in `DATA.md`.

Optional check, when Node is available: `npx @google/design.md lint DESIGN.md` validates the tokens and reports contrast problems as JSON.

## Where the rules come from

`design-floor.md` is written in our own words. Its ideas are the points where several public design skills for coding agents agree (Anthropic's frontend-design skill, Impeccable, Hallmark and ui-ux-pro-max; links and licences in `CATALOG.md`). No text was copied from them; where they disagree, `DESIGN.md` decides.

Licences were read from the public repositories on 22 November 2026. Recheck before reusing any code or text from them.
