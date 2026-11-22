# __name__

One sentence that says what __name__ does.

The following example greets a user by name.

```lus nocheck
local __name__ = require("https://atmosp.here/__line__/__name__.lus")
print(__name__.greet("Ada"))
```

## Development

Run these commands from the root of the repository.

```sh
lus test
atmos check
```

A signed commit on `main` publishes to `unstable`. Once `@version` reaches 1.0.0, `atmos publish` tags and pushes a release for Lus __line__. Versions below 1.0.0, such as the starting version 0.1.0, publish to `unstable` only.
