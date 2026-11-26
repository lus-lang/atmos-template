# __name__

This repository is a Lus package published on atmosphere, the package registry of Lus.

- The main module is `__name__.lus`. Its first doc comment is the package header. Keep `@version`, `@lus`, `@license`, every `@permission`, and every `@flag` accurate.
- Other modules are under `__name__/` and load with `require("__name__.NAME")`.
- Run `lus fmt --write .`, `lus check .`, `lus test`, and `atmos check` before every commit. The pre-commit and pre-push hooks run them too.
- A package declares the permissions it needs with `@permission` and never calls `pledge` itself. Only the program that loads the package grants and seals permissions.
- After the first release on a Lus line, every later release on that line keeps the major and minor version of the first release and raises the patch version.
- Dependencies are copied into the package with `atmos add URL`, so the package loads no code over the network.
- The README holds only the name, one sentence, the link to the package page, and the license. Usage goes in the doc comments, which the package page renders. Instructions for contributors go in `CONTRIBUTING.md`.
- Prose in the README, the doc comments, and the changelog follows the `lus-writing` skill, which `lus agents init` installs and https://lus.dev/agents/skills/lus-writing/SKILL.md serves.
