# Shared instructions for future work

1. Read `PRODUCT.md` and `DESIGN.md` before building or changing a screen. If either is missing, copy its `.template.md` counterpart and confirm the project decisions with the user.
2. Work on one screen or game system at a time. Make it usable before starting another.
3. Avoid unrequested dependencies. Use the platform and tools already in the project where possible; ask before adding a package, framework, or service.
4. Check the relevant states for the work: loading, empty, error, success, disabled, pause, or interruption as applicable.
5. Check relevant screen sizes and input methods for the target platform. Include phone, tablet, and desktop sizes only when the product supports them.
6. Respect accessibility and performance constraints in `PRODUCT.md` and `DESIGN.md`, including reduced-motion preferences where applicable.
7. Do not impose one visual style on every project. Follow each project's own product and design documents.

## Optional reference material

References under `references/` are reading material, not included tools or libraries. Do not install, import, clone, vendor, or run their code unless the user specifically asks for that in a project.

Before using a motion reference, confirm it fits the chosen platform and inspect its current documentation, examples, release status, and license. Choose techniques that serve the project's `PRODUCT.md` and `DESIGN.md`; do not impose a reference's visual style on the project.

Use no more than one relevant reference skill for a task. Complete the applicable platform brief and record only evidence actually observed during the work.