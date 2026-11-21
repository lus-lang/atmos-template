# __name__

This repository is a Lus package published on atmosphere, the package registry of Lus.

- The main module is `__name__.lus`. Its first doc comment is the package header. Keep `@version`, `@lus`, `@license`, every `@permission`, and every `@flag` accurate.
- Other modules live under `__name__/` and load with `require("__name__.NAME")`.
- Run `lus fmt --write .`, `lus check .`, `lus test`, and `atmos check` before every commit. The pre-commit and pre-push hooks run them too.
- A package declares the permissions it needs with `@permission` and never calls `pledge` itself. Only the program that loads the package grants and seals permissions.
- A release on a Lus line may only raise the patch version of the first release on that line.
- Dependencies are copied into the package with `atmos add URL`, so the package loads no code over the network.
