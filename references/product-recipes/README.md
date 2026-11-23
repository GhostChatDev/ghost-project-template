# Product recipes

Optional product patterns for apps built from this template. They sit next to `references/design-kit/` and `references/motion-stack/` and follow the same rule: read them only when asked, and do not install anything unless `PRODUCT.md` asks.

A recipe is not a dependency, a framework, or a product that ships with every project. The files in this folder do not authorize packages, services, workflows, or implementation by themselves.

## When to read one

1. Read `PRODUCT.md` and `DESIGN.md` first. They win over every recipe.
2. Open a recipe only when `PRODUCT.md` explicitly selects it by name.
3. If `PRODUCT.md` does not name a recipe, ignore this folder.
4. If `PRODUCT.md` or `DESIGN.md` is missing, follow the repository briefing process and stop. Do not fill those files from a recipe.

## What a recipe may and may not do

- It may describe jobs, screens, data contracts, and acceptance checks for a product that chose it.
- It may name outside projects as patterns. Those links are not permission to copy code or to add a package.
- It must not replace `PRODUCT.template.md`, `DESIGN.template.md`, or the briefing stop rule.
- It must not install dependencies, enable external services, or start a build merely because the file exists.

Review the licence of any component before reuse. Recheck licences at the time of use.
