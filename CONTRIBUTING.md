# Contributing to __name__

The following commands run the tests and the quality checks of atmosphere from the root of the repository. The pre-commit and pre-push hooks in `.githooks/` run them too.

```sh
lus test
atmos check
```

A signed commit on `main` publishes to `unstable`. Once `@version` reaches 1.0.0, `atmos publish` tags and pushes a release for Lus __line__. A version below 1.0.0, such as the starting version 0.1.0, publishes to `unstable` only.
